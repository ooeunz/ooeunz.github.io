---
title: "python: library설치"
date: 2019-03-05 08:26:28 -0400
categories: ComputerScience
tags: [python]
---

다른 포스팅에서 이야기 했듯이 python에는 많은 라이브러리들이 있다. 라이브러리는 pip를 사용해서 설치할 수 있다.

### 가상환경 설치
1. 먼저 라이브러리를 설치할 가상환경을 실행시킨다.
* Mac, Linux
```
$ source activate <가상환경 이름>
```
* Window
```
$ activate <가상환경 이름>
```
2. pip를 최신 버전으로 업그레이드 시켜준다.
```
pip install --upgrade pip
```
4. 이후 원하는 라이브러리를 다음과 같이 설치할 수 있다.
```
$ pip install <라이브러리 이름>
```

### 주의할 점
pip install과 pip3 install이 있는데,
pip는 python2버전의 라이브러리로 저장이되고, pip3는 python3 버전의 라이브러리로 저장이된다.

즉, python3 버전에서 pip install로 라이브러리를 설치시 path가 달라서 라이브러리를 불러오지 못한다.
