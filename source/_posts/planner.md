---
title: 计划
date: 2020-11-27 23:27:07
tags: 接下来一周要干的事，每一个写一篇博客
---
1. 数据库调用学习-如数据库建立
2. 网络技术 TCP/IP协议，通信协议iot
3. Grundkenntnisse  Client-Management-Systeme Systemadministration 
4. 开发一款针对在几大特定的求职网站上给出关键字获得相应职位并标注出现的次数

openpose-pytorch installation [openpose-pytorch](https://github.com/prasunroy/openpose-pytorch):
introdution:
Window 64bit; python3.6 installed;

Requirement:
let openpose-pytorch project running based on python3.7

Process:
1. python3.7 install
Although x86 was originally a 16-bit architecture, the version in use today is the 32-bit extension. x64 is actually more correctly "x86-64"--the 64-bit extension of x86.
so 64-bit system download x86-64 version

2. cmd:pip install torch==1.7.0+cpu torchvision==0.8.1+cpu torchaudio===0.7.0 -f https://download.pytorch.org/whl/torch_stable.html (in the process numpy etc dependencies installed into file python37)
Attention: the position(should be above the others) of python3.7 in enviroment, while python3.6 and 2.7 installed and being willing to install .whl with 3.7


3. according to the above website to git clone the project into local(running python setup.py, where some dependencies also installed into file python37)

Possible problems:

After Insallation should be continuing according to the Prerequisites(install anaconda) in [website](https://hexo.io/docs/generating.html)? No, because I have python installed by myself and numpy with instructions (pip install torch==1.7.0+cpu torchvision==0.8.1+cpu torchaudio===0.7.0 -f https://download.pytorch.org/whl/torch_stable.html), while with anaconda almost all denpendances can be automatically included. Either of them is ok.

Normally the .whl can not be installed mainly due to the problem of python version  

ModuleNotFoundError: No module named 'pip'
=>Just be sure that you have include python to windows PATH variable, then run [python -m ensurepip]

RuntimeError: The current Numpy installation fails to pass a sanity check due to a bug in the windows runtime [duplicate]
=>The temporary solution is to use numpy 1.19.3.
  pip install numpy==1.19.3

Result:
In my computer installed:
torch-1.7.0%2Bcpu-cp36-cp36m-win_amd64(based on python36, but maybe no connection between the 36s)
torch-1.7.0%2Bcpu-cp37-cp37m-win_amd64(based on python37)

Encapsulation:
Writing a class encapsulation to achieve the function> input:image output: key positions


next step:
openpose尽量找个用pytorch写的，好一点的
可以试试这个：https://github.com/prasunroy/openpose-pytorch
然后以来用pip安装的，不要conda的
这部分就是能实现输入任意图片(分辨率)，输出关键点就行=>测试
你也可以试试其他袋码的，就是越简洁越好(就是不需要太多不相关的功能，不比如训练，测试精度那些)=>找合适项目
https://github.com/CMU-Perceptual-Computing-Lab/openpose




Codesys:port 11743
The CODEsys control PLC allows executing program code with system level access on this maschine.
This may pose as a security threat unless appropriate measures are taken to limit network access to this maschine.

system level access=>the problem? to do: limit network access, should be degraded with windows admin  right?

Solution: I had installed version Codesys V3.5 SP16 Patch3, before instead of that Codesys V3.5 SP16 Patch2 was reinstalled and successfully connecting Control Win systray 64.

what is gateway?


RS232 rs485:
RS232: transmission distance is limited, electrical noise
rs485: half-duplex mode of operation, but easy to connect up to 32 devices on one system

dialog (08-11.12.2020)

07.12.2020 wurde eine gespräch mit Faun Umwelttechnik gefhührt, eigentlich hätte ich kaum Chance ins nächsten Schritt einzutreten, bevor ich meine Familie erwähnte. Als Ergebnis bekommte ich eine Chance, nächste drei Tage nach Bremen zu fahren und Probentage zu führen. Damit habe ich mich davor gar nicht gerechnet, dass deutsche Firma so effizient ist. Na dann musste ich die Chance ergreifen. 

Nach eine Lange Fahrt mit Bahn um 21:00 Uhr war ich in dem Zielort angekommen, und glücklich alles insgesamt
in Ordnung. Der Besizer des Hotel sind ganz freundlich und ließ mich keine Sorge, obwohl ich beim Schlaf noch nicht so Ruhig. Am erste Tag im Unternehmen hatte der Leiter, Herr Leif Börger, einen ganzen Mrogen verbraucht mich zu begleiten im Werk überall zu schauen und mich erzählt, was ist ihre Aufgabe. Endlich mir eine kleine Programmierungsaufgabe abgegeben, "wie viel mal dem Fahrzeug eingetankt wurden, wenn den Maximalwert überschritten geben eine Anmeldung" eine nicht so komplexe aber spannende Aufgabe. Weil der Programmierungssprache nicht wie C++ or Java, welche popülär sind, sondern codesys eine struktuiert text, war. Dafür war ich nicht so zufrieden und der Teamleiter auch eine tatsählich person oft mit fack oder verdammt, was lässt mich  ihn eine reale Person anstatt manche gut audgebildeten Personen betrachten.

Aber wonach ich suche? wie sieht der Aussicht der Arbeit aus? Davor habe ich immer gedacht, dass ich eine reine Software entwickler wäre. Aber jetzt steht ich vor dem Umgang mit dem realen Fahrzeug. Aber das wäre auch cool, wenn mit nicht so komplexe Aufgabe umgehen, würde ich immer mehr Zeit für selben und meine Familie haben. Aber innerhalb mich wohnt ein Person, der starkt Durst nach KarrierenErfolg hat. Ich wünsche mir keinen einfach ergesetzten Person.

Ich muss sagen, der Stadt, wo ´sich der Unternehmen befindet, ist nicht so lebhaft wie Dresden, auch da momentan keine Bekannte und Freunde. Aber ich gerne nehme die neue Herausforderung über und wünsche ich kann viel ernte.


Insgesamt gesagt, dass die Reise wunderbar war und wünsche zusammen alles gut.


1.3D Visualisierung- opengl+python

abschlussarbeit - Kurvenanpassung bei Pfadplannung im matlab(ein variable wurde von zwei anderen Variablen beeinflusst) zur Generierung der Polynomial mit zwei Variablen

Geräteentwicklung  Auslegung von Werkzeug in CAD