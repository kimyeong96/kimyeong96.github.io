---
layout: single
title:  "Java 컬렉션 프레임워크(Collection Framework) 1편"
categories: Java
tag: [JAVA, 컬렉션프레임워크, ArrayList, LinkedList, 자바의 정석]
toc: true
toc_sticky: true
author_profile: true
sidebar:
  nav: "docs"
---

# ✍2022-02-02

## 컬렉션 프레임웍(Collections framework) 1편

<!--Quote-->
> *본 내용은 자바의 정석을 바탕으로 작성*

> ❗ 개인이 공부한 내용을 적은 것 이기에 오류가 많을 수도 있음


### 컬렉션 프레임웍의 핵심 인터페이스

1. List : 순서가 있는 데이터 집합, 데이터의 중복 허용
   ex) 대기자 명단, 보통 ArrayList와 LinkedList를 사용
2. Set : 순서가 없는 데이터 집합, 데이터의 중복 허용 금지
   ex) 양의 정수집합
3. Map : 키와 값의 쌍으로 이루어진 데이터의 집합, 순서 유지(X), 키 → 중복 허용 금지, 값 → 중복 허용
   ex) 우편번호, 지역번호 , 키 → ID , 값 → 비밀번호라 생각

## ArrayList

- 데이터의 저장공간으로 배열을 사용

<script src="https://gist.github.com/kimyeong96/847b5d6b2e8afa6baa69a3179ab6c2c6.js"></script>


![arrayList.png](/assets/images/posts/2022-02-02/arrayList.png)

- 1번식으로 하면 성능이 안좋아서 2번식으로 하는게 좋다

## 배열

- 배열은 구조가 간단하고 데이터를 읽는 데 걸리는 시간이 짧다
- 크기를 변경할 수 없다
- 비순차적인 데이터의 추가, 삭제에 시간이 많이 걸린다

## LinkedList

1)장점

- 배열의 단점을 보완 → 배열과 달리 불연속적으로 데이터를 연결
- 데이터의 삭제 : 단 한 번의 참조변경만으로 가능
- 데이터의 추가 : 한번의 Node 객체 생성과 두 번의 참조변경만으로 가능

2)단점

- 데이터 접근성이 나쁨 →  0x200 에서 0x400으로 한번에 못가고 한칸씩 옮겨서 가야한다

![linkedlist.png](/assets/images/posts/2022-02-02/linkedlist.png)




### 더블링크드리스트 (Doubly LinkedList)

- 위의 단방향성의 단점을 개선하고자 나옴
- 접근성이 향상되었지만, 앞 뒤로의 이동만 좋아짐

![double.png](/assets/images/posts/2022-02-02/double.png)



### 더블써큘려링크드리스트

- 더블링크드리스트 (Doubly LinkedList) 보다 접근성을 더 향상시킴
- 더블 링크드리스트의 첫 번째 요소와 마지막 요소를 서로 연결  시킴 → 예를 들면 채널 1에서 아래로 채널을 내리면 99번을 가는 것과 같은 원리

![circular.png](/assets/images/posts/2022-02-02/circular.png)

## ArrayList vs LinkedList

1. 순차적으로 데이터를 추가/삭제  ArrayList가 더 빠름
2. 비순차적으로 데이터를 추가/삭제 LinkedList가 더 빠름
3. 접근시간(access time)은 ArrayList가 더 빠름

## Iterator

<script src="https://gist.github.com/kimyeong96/abab1554b15ec24db7d591a0a2a10519.js"></script>

<details>
<summary>👈Tip</summary>
<div markdown="1">
list와 set은 collection이 자손이다 → 다형성 활용 가능
</div>
</details>


## 📑 출처

 - [자바의 정석 카페](https://cafe.naver.com/javachobostudy)
 - [자바의 정석 유튜브](https://www.youtube.com/user/MasterNKS)