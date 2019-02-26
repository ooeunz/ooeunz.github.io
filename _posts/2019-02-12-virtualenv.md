---
title: "pyenv 가상환경 +수정중"
date: 2019-02-12 08:26:28 -0400
categories: ComputerScience
tags: machinelearning
---


### Pyenv
* no module _tkinter일 경우
`$ brew install tcl-tk`
또는
`$ brew reinstall tcl-kr` 이후
pyenv 파이썬 설치

* 설치목록
`$ pyenv install —list`

* 파이썬 목록
`$ pyenv versions`

* 특정버전 삭제
`$ pyenv uninstall <버전 이름>`

* 파이썬 설치
`$ pyenv install <파이썬 버전>`
안될시엔
```
$ CFLAGS="-I$(brew --prefix readline)/include -I$(brew --prefix openssl)/include -I$(xcrun --show-sdk-path)/usr/include" \
LDFLAGS="-L$(brew --prefix readline)/lib -L$(brew --prefix openssl)/lib" \
PYTHON_CONFIGURE_OPTS=--enable-unicode=ucs2 \
pyenv install -v 3.7.1
```
* 파이썬 글로벌 설정
`$ pyenv global <파이썬 버전>`

### virtualenv 가상환경
*  가상환경 : 생성
`$ pyenv virtualenv <version> <가상환경 이름>`
`$ pyenv virtualenv <가상환경 이름>`
* 가상환경 : 삭제
`$ pyenv uninstall <가상환경 이름>`
* 가상환경 실행
`$ source activate <가상환경 이름> `
* 가상환경 나가기
`$ source deactivate`


### matplotlib

* x와 y에 데이터를 입력한 후, plt.plot(x, y)를 이용해 그래프를 그렸습니다.
 `plt.plot(x, y)`



* 말 그대로 x축 label과 y축 label의 이름을 지정해주는 함수 입니다. x축에는 'Numbers'를 y축에는 'Counting'을 입력했습니다.

`plt.xlabel(), plt.ylabel()`

* 그래프의 메인 제목을 입력하는 함수 입니다.
`plt.title()`

* 그래프를 보여줌
`plt.show()`

-그래프를 보여주는 창을 띄워주는 코드입니다. plt.show()를 입력하지 않고 코드를 실행 시키면 아무것도 뜨지 않습니다.

R(R Studio)의 경우, 따로 plt.show()와 같은 코드 없이 plot 함수를 실행하면 바로 그래프가 나타나 어색했지만, 쉽게 얘기하면 앞에까지의 코드들이 다 뒷배경에 그리는 역할이라면, 이거를 앞으로 들고 나오는 역할이 plt.show() 입니다.


### pandas
[판다스 기본문법](https://ordo.tistory.com/34?category=732886)
