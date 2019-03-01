---
title: "가상환경에 대한 이해"
date: 2019-02-12 08:26:28 -0400
categories: ComputerScience
tags: machinelearning
---
### Life is too short, You need Python
인생은 너무 짧으니 파이썬이 필요해.

파이썬은 그 자체로도 간결한 문법과 가독성으로 급성장하고 있는 언어입니다. 여러 _편의성 있는 문법_들을 제공하고 (슬라이싱과 같은) _가독성이 좋기에_ 비전공자들이 처음 프로그래밍 세계에 입문할때 C언어와 같이 입문용으로 많이 배우는 언어중 하나입니다. 하지만 파이썬이 유용한 이유는 사실 그 뿐만이 아닙니다.

파이썬은 강력한 라이브러리들을 많이 가지고 있습니다. (그로 인해 파이썬은 날개를 달았습니다.) 최근에는 pandas와 numpy들과 같은 라이브러리를 통해 데이터 분석에서도 빛을 내고 있으며, R언어와 유사할 정도로 사용률이 올랐습니다.

하지만 파이썬의 많은 라이브러리와 버전들은 그때 그때 컴퓨터에 프로젝트에 맞게 사용하기 어려움으로 가상환경을 사용합니다.

### 가상환경이란?
가상환경이란 컴퓨터안에 독립된 파이썬 공간을 생성하는 것을 의미합니다.
예를들어 A라는 프로젝트에는 python3버전이, B라는 프로젝트에는 python2버전이 사용되었다고 가정하겠습니다. 만약 가상환경이 없다면 우리는 그때그때 프로젝트에 맞게 컴퓨터에 파이썬을 새로 설치해야 했을 것입니다. 하지만 pyenv와 virtualenv를 이용하면 파이썬을 권총에 탄알 장착하듯 필요에 따라 파이썬 버전을 바꿀 수 있습니다.

pyenv는 파이썬 버전을 바꾸는 것, virtualenv는 그 파이썬 버전의 환경에 다양한 라이브러리를 설치 할 수 있는 환경이라고 생각하시면 편할 것 같습니다.
(pyenv 안에 virtualenv가 설치되는 것임.)

### pyenv 설치
본 설치는 맥환경을 대상으로 합니다.

* brew로 설치
`$ brew update`
`$ brew install pyenv`

* 설치 가능 목록 (pyenv로 설치 할 수 있는 python 목록)
`$ pyenv install —list`

* 파이썬 설치
`$ pyenv install <파이썬 버전>`
안될시엔
```
$ CFLAGS="-I$(brew --prefix readline)/include -I$(brew --prefix openssl)/include -I$(xcrun --show-sdk-path)/usr/include" \
LDFLAGS="-L$(brew --prefix readline)/lib -L$(brew --prefix openssl)/lib" \
PYTHON_CONFIGURE_OPTS=--enable-unicode=ucs2 \
pyenv install -v 3.7.1
```

* 설치한 파이썬 목록
`$ pyenv versions`

* 특정버전 삭제
`$ pyenv uninstall <버전 이름>`

* 파이썬 글로벌 설정
`$ pyenv global <파이썬 버전>`



### virtualenv 가상환경 설치
*  가상환경 : 생성
`$ pyenv virtualenv <version> <가상환경 이름>`
`$ pyenv virtualenv <가상환경 이름>`
* 가상환경 : 삭제
`$ pyenv uninstall <가상환경 이름>`
* 가상환경 실행
`$ source activate <가상환경 이름> `
* 가상환경 나가기
`$ source deactivate`
