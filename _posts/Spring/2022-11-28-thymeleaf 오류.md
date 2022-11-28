
## IntelliJ IDEA - Cannot resolve symbol ${className}

![1.png](/assets/images/posts/2022-11-28/1.png)

❗ 문제 원인

**IntelliJ IDEA**에서 **Gradle**기반의 프로젝트 작성시 가끔 `Cannot resolve symbol ${className}`
 메시지가 등장할 때가 있다. 프로젝트 내 **CLASSPATH**에서 해당 클래스를 찾지 못하여 발생하는 것인데 **External Libraries**탭을 보면 `/build.gradle`의 **dependencies**에 정의한 라이브러리들이 로드되지 않은 것을 확인할 수 있다.

<br/>

💡 해결 방법

- **File → Invalidate Caches / Restart…**를 실행한다. **IntelliJ IDEA**를 재시작한다. 오류가 해결되었는지 확인한다.
- 앞의 방법으로 해결되지 않는다면 **Gradle** → 프로젝트명 우클릭 → **Refresh external project**를 클릭한다. 오류가 해결되었는지 확인한다.

- 기존 코드에서 변경

1) 오류

```java
<html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:th="http://www.thymeleaf.org">
```

2) 오류 해결

```java
<html xmlns="http://www.w3.org/1999/xhtml"
      xmlns:th="http://thymeleaf.org">
```

<br/>

👍 해결

![2.png](/assets/images/posts/2022-11-28/2.png)

<br/>

## 📑 출처
 - [구글링](https://velog.io/@leyuri/IntelliJ-IDEA-Cannot-resolve-symbol-className)
 - [stackoverlflow](https://stackoverflow.com/questions/38710585/spring-boot-thymeleaf-in-intellij-cannot-resolve-vars/44804086)
