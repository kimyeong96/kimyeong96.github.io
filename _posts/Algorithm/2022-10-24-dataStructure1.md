---
layout: single
title:  "Algorithm - BFS"
categories: Algorithm
tag: [BFS, DFS]
toc: true
toc_sticky: true
author_profile: true
sidebar:
  nav: "docs"
---


## 그래프 탐색 : 어떤것들이 연속해서 이어질때, 모두 확인하는방법

- Graph : Vertex(어떤것) + Edge(이어지는것)

<br/>

### 그래프 탐색 종류
- BFS : Breadth-first-search(너비 우선 탐색) : 자식 탐색 → 자식 탐색(첫 노드에서 손자)
- DFS: Depth-first search(깊이 우선 탐색)

## 너비 우선 탐색(BFS)이란
루트 노드에서 인접한 노드를 먼저 탐색하는 방법

- 시작 정점으로부터 가까운 정점을 먼저 방문하고 멀리 떨어져 있는 정점을 나중에 방문하는 순회 방법이다.
- 즉, 깊게(deep) 탐색하기 전에 넓게(wide) 탐색하는 것이다.
- 두 노드 사이의 최단 경로 혹은 임의의 경로를 찾고 싶을 때 BFS를 사용

![img2.gif](/assets/images/posts/2022-11-20/img2.gif)





## 너비 우선 탐색(BFS)의 특징
- BFS는 시작 노드에서 시작해서 거리에 따라 탐색한다
- BFS는 재귀적으로 동작하지 않는다.
- 어떤 노드를 방문했었는지 여부를 반드시 검사 해야한다.
- Queue를 사용한다



## BFS의 코드 구현
- 시작점에 연결된 Vertex 찾기
- 찾은 Vertext를 Queue에 저장
- Queue의 가장 먼저 것 뽑아서 반복

<br/>








### 시간복잡도

- 알고리즘이 얼마나 오래걸리는지
- BFS : O(V+E)



## 📑 출처
- [개발자 장고](https://www.youtube.com/watch?v=ansd5B27uJM)
- [사진 출처](https://www.codevelop.art/graphs-in-java-breadth-first-search-bfs.html)