---
title: "error: ImportError: No module named _tkinter"
date: 2019-03-04 08:26:28 -0400
categories: ComputerScience
tags: [error, matplotlib]
---

### backend 변경해보기
mac이나 linux으로 matplotlib를 실행시켰을때 종종 tkinter error가 날때가 있다.

mac에서의 경우 기본 backend가 TkAgg로 설정되어있지 않아서 에러가 난다. 그럴 경우에 스크립트상에 다음 코드를 추가해준다.
```
import matplotlib
matplotlib.use(“TkAgg”)
```

매번 코드를 추가하기 귀찮으므로 bash상에 설정을 바꾸어주는 방법도 있다.
```
echo "backend: TkAgg" >> ~/.matplotlib/matplotlibrc
```



### tkinter 설치
tkinter는 기본적으로 matplotlib를 설치하면 같이 설치가되나, 간혹 설치가 되지 않은 경우 다음과 같은 코드로 명시적으로 install 해준다.

* Linux
리눅스의 경우 패키지 관리 툴 apt로 손쉽게 설치할 수 있다.
```
sudo apt-get install python3-tk
```

* mac
mac의 경우 apt가 없기 때문에 homebrew를 이용하여 설치해준다.
```
$ brew install tcl-tk
```
또는
`$ brew reinstall tcl-kr`

하지만 주의할 점이 있는데, pyenv가상환경 내에서 matplotlib를 사용할 경우, **반드시 tkinter를 먼저 설치한 이후에 pyenv 파이썬 환경을 설치해야한다.** 필자는 이 문제로 거의 하루를 보냈다ㅠㅠ. 가상환경의 경우 path가 꽤나 꼬여있기 때문에 _설치 순서가 중요하다._

# etc
### backend란?
python에서 graph등을 그릴때 실행하는 환경을 지원하는 환경이다. 사용자에 따라 콘솔에 그리고나 툴에 그리거나 등등 여러가지 환경을 지원한다.

* 다양한 backend 확인

[Usage — Matplotlib 2.0.2 documentation](https://matplotlib.org/faq/usage_faq.html)
