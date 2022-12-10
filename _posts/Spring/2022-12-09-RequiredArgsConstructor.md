---
layout: single
title:  "@RequiredArgsConstructor"
categories: SpringBoot
tag: [RequiredArgsConstructor]
toc: true
toc_sticky: true
author_profile: true
sidebar:
  nav: "docs"
---


의존성주입의 종류는`Constructor(생성자)`,`Setter`,`Field` 타입이 존재한다.

그 중 생성자를 활용하여 의존성 주입을 하는 것을 보면 아래와 같이 코드를 구현한다.

<br/>
1️⃣ `Constructor(생성자)` 사용

```java
@Repository
public class MemberRepository{
    private final EntityManager em;

    @Autowired
    public MemberRepository(EntityManager em){
    	this.em = em;
    }
}
```

생성자주입의 단점은 위의 Constructor(생성자) 코드처럼 생성자를 만들기 번거롭다는 것이다. 하지만 이를 보완하기위해 `롬복`을 사용하여 간단한 방법으로 생성자 주입 방식의 코딩을 할 수 있다.

<br/>
2️⃣ `@RequiredArgsConstructor` 사용

@RequiredArgsConstructor는 **final 혹은 @NotNull**이 붙은 **필드의 생성자를 자동으로 만들어**
준다. 이를 통해 새로운 필드를 추가할 때 다시 생성자를 만들거나 하는 등의 번거로움을 없앨 수 있다.

```java
@RequiredArgsConstructor
public class MemberRepository{
	private final EntityManager em;
}
```

private final Member member; 라고 final로 선언한 필드가 있다고 했을 때

@RequiredArgsConstructor 어노테이션을 사용하면 클래스에서 final 붙은 필드만 가지고 생성자를 만들어서 알아서 주입해준다.

하지만 자동적으로 생성자가 만들어지기 때문에 내가 예상하지 못한 결과나 오류가 발생할 수 있기 때문에 그런 점도 염두해둬야 한다.