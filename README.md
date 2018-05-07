ConsoleControl
==============

내 프로그램에서 콘솔 기반의 프로그램을 실행하면 별도의 콘솔창이 떠서 작동한뒤에 종료하는 방식인데, 
이 라이브러리를 사용하면 Winforms나 WPF 창에 콘솔창을 올려놓고 직접 결과를 보거나 직접 명령을 입력할 수 있다. 
즉, 폼 위에 cmd 창을 올려놓는 방법이라고 보면 된다. 


설치 방법
-------------------------

Nuget에서 ConsoleControl을 검색한뒤에 설치하면 된다. 

For WinForms:

````
PM> Install-Package ConsoleControl
````

For WPF:

````
PM> Install-Package ConsoleControl.WPF
````


사용 방법
--------------------
비주얼 스튜디오의 툴박스에서 [항목추가]를 선택하여 ConsoleControl.dll을 추가한다. 
추가한 컨트롤을 폼 위에 올려놓는다. 
아래처럼 사용한다. 

// cmd와 똑같이사용하고 싶을 경우
consoleControl1.StartProcess("cmd", null);

// 직접 명령을 실행하고 결과를 보려고 하는 경우
consoleControl1.StartProcess("ping.exe", "192.168.0.1");

// 단순히 텍스트만 출력하고 싶을때 (출력되는 텍스트는 아무런 기능 없음)
consoleControl1.WriteOutput("Test String", Color.Red);


추가 사용 방법
-------------------------------

아래의 코드프로젝트 링크에서 추가 사용방법을 볼 수 있다. 

http://www.codeproject.com/Articles/335909/Embedding-a-Console-in-a-C-Application

