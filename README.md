# jsaboard
주소아 센서보드를 파이썬에서 사용하기

다음 링크의 코드를 주소아 센서보드에 맞게 수정하였습니다.
<pre>https://sites.google.com/site/helloboardwiki/software/python-library</pre>

테스트 환경
<pre>Python 3.7
pyserial 3.4</pre>

파일 목록
<pre>jsaboard.py : 주소아 센서보드 구형(스크래치 1.4)
jsaboard2.py : 주소아 센서보드 신형(스크래치 2.0)</pre>

사용법
<pre>>>> s = ScratchBoard('COM4')
COM4
>>> s.start()
>>> s.sensorValues
[1023, 1023, 1023, 1023, 1023, 210, 1, 27]
>>> s.stop()
>>> s.sensorValues
[0, 0, 0, 0, 0, 0, 0, 0]
>>> s.restart()
Helloboard started to read sensors...
>>> s.stop()
>>> s.sensorValues
[0, 0, 0, 0, 0, 0, 0, 0]
>>> s.restart()
Helloboard started to read sensors...
>>> s.sensorValues
[1023, 1022, 1023, 1023, 1023, 228, 1, 28]
>>> s.readButton()
False
>>> s.readLight()
28
>>> s.readResistanceA()
1023
>>> s.readResistanceB()
1023
>>> s.readResistanceC()
1023
>>> s.readResistanceD()
1023
>>> s.readSlide()
27
>>> s.readSound()
4</pre>
