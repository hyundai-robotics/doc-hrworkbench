
[__SOURCE](README.md)
# Hi6/Hi7 제어기 기능설명서 - HRWorkBench

[__SOURCE](0-about-this-manual/README.md)
# 이 설명서에 대하여


[__SOURCE](0-about-this-manual/precautions.md)
# 사전 주의사항

{% include file="ko/precautions.md" %}

[__SOURCE](0-about-this-manual/safety-notice.md)
# 안전 주의 사항

{% include file="ko/safety-notice.md" %}

[__SOURCE](1-preface/README.md)
# 1. 개요


[__SOURCE](1-preface/1-intro.md)
## 1.1 HRWorkBench의 소개

HRWorkBench는 HD현대로보틱스 Hi6/Hi7 제어기의 교시를 지원하기 위한 윈도우PC용 소프트웨어입니다. HRWorkBench는 이더넷 통신으로 연결된 Hi6/Hi7 제어기에 대해 아래와 같은 기능들을 지원합니다.  
(Hi5a 제어기에서 사용하던 HRView, HRHistoryViewer 소프트웨어의 후속 제품입니다.)

| 구  분 | 설   명 |
|---|---|
| 파일 백업과 복원 | 프로젝트 폴더 전체와 이력 폴더 전체를 PC에 백업하고 제어기로 다시 복원할 수 있습니다. |
| job 파일 관리 | 제어기 내의 job 목록을 확인하고, PC - 제어기 간 일부 JOB 파일을 복사하거나 삭제할 수 있습니다. |
|job 파일 편집|제어기의 job파일을 더블클릭하여 열고 편집할 수 있습니다. syntax coloring와 smart indent 기능을 지원하여 가독성 있는 편집을 지원합니다.|
|job 파일 문법검사|실행 전 job파일에 대한 기본적인 문법 검사를 원격으로 수행할 수 있습니다.|
|전역변수 모니터링과 값 편집|전역변수 전체의 값을 모니터링할 수 있으며, 원하는 변수의 값을 수정하거나 변수를 삭제할 수 있습니다.|
|로봇언어 실행|job파일의 대입문 등을 원격으로 실행할 수 있습니다. move문이나 flow제어문은 지원하지 않습니다.|
|제어기 이력 모니터링, 확인|제어기에서 발생한 에러, 경고 등의 이력을 원격으로 모니터링 합니다. 혹은 PC에 백업한 프로젝트의 이력을 확인합니다.|
|스코프 로그 (scope log) 확인|로봇 충돌 등 치명적인 오류 시에 생성되는 스코프 로그의 데이터 파형을 읽어들여 그래프로 표시해줍니다. 데이터 파형을 .csv 파일로 export할 수도 있습니다.|
|설정의 확인과 포팅|제어기의 설정이나 변수의 일부를 다른 제어기에 동일하게 반영할 수 있습니다.|


{% hint style="warning" %}
본 프로그램은 job 프로그램이나 변수 값을 원격으로 변경하므로, 로봇 동작에 영향을 줄 수 있습니다. 본 설명서를 숙지하시고 충분한 주의를 기울여 신중하게 사용해주십시오!
{% endhint %}

* HRWorkBench는 HD현대로보틱스 웹사이트(https://www.hd-hyundairobotics.com/) - 고객지원 - 응용소프트웨어 화면에서 다운로드 받으실 수 있습니다.

[__SOURCE](1-preface/2-install-exec.md)
## 1.2 HRWorkBench의 설치와 실행

설치파일을 실행하십시오.

![](../_assets/preface/installer1.png)


Next 버튼을 계속 누르면, 설치할 위치 등 선택화면이 진행됩니다. 라이선스에 동의하고 마지막으로 Install 버튼을 클릭하면 설치가 진행됩니다.

![](../_assets/preface/installer2.png)
![](../_assets/preface/installer3.png)

설치가 완료되면 Finish 버튼을 클릭해, Installer를 종료하십시오.

![](../_assets/preface/installer4.png)


윈도우 시작버튼을 클릭하고 최근에 추가한 앱, 혹은 HHI Robotics 그룹에서 HRWorkBench를 선택하면 응용프로그램이 실행됩니다.

![](../_assets/preface/exec-icon.png)

[__SOURCE](1-preface/3-ui.md)
## 1.3 HRWorkBench의 사용자 인터페이스 구성

아래 그림은 HRWorkBench를 구성하는 사용자 인터페이스의 명칭입니다.
각각의 기능에 대해서는 작업 순서에 따라 차례로 설명하겠습니다.

![](../_assets/preface/ui1.png)


사용자 인터페이스 요소들은 작업에 편리한 레이아웃으로 재배치할 수 있습니다.
툴 막대의 좌측 가장자리와 창들의 제목부분을 마우스 좌버튼으로 끌어 도킹(docking) 상태에서 떼어내거나 다시 가장자리에 붙여 도킹 시킬 수 있습니다. 도킹상태에서는 창들을 나란히 배치하거나, 겹쳐서 탭(tab)으로 선택하는 페이지로 만들 수도 있습니다.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/preface/ui2.png" width="20%">
  <img src="../_assets/preface/ui3.png" width="80%">
</div>

주 메뉴의 '도움말 - Change Language (언어 변경)'을 선택하면 사용자 인터페이스의 언어를 전환할 수 있습니다. 언어를 선택한 후, HRWorkBench를 다시 실행하십시오.

![](../_assets/preface/ui4.png)

[__SOURCE](2-setting/README.md)
# 2. 기본 설정


[__SOURCE](2-setting/1-ethernet.md)
# 2.1 이더넷 연결

HRWorkBench와 Hi6/Hi7로봇제어기는 같은 이더넷 네트워크로 연결되어야 합니다.
연결해야 할 Hi6/Hi7 제어기가 2대인데, 각각의 IP주소가 192.168.1.150과 192.168.1.151이고, PC의 IP 주소는 192.168.1.100 이라고 가정하겠습니다. (허브를 통해 서로 연결된 장치들은 모두 같은 서브네트워크인 192.168.1.XXX 여야 합니다.)

HRWorkBench의 메인 메뉴에서 `통신 - 주소관리자`를 선택하거나 툴 버튼 <img src='../_assets/tool-btn/tb-addrmng.png'/>를 클릭하면 아래와 같은 IP주소 관리 대화상자가 열립니다.

`[추가]` 버튼을 클릭할 때마다 입력 행이 1개씩 새로 추가됩니다. 2개의 행을 추가한 후, 그림과 같이 이름과 IP주소를 입력하십시오.
`[위로]`와 `[아래로]` 버튼을 클릭하면 현재 행을 위 아래로 이동시켜 순서를 조정할 수도 있습니다.

![](../_assets/setting/addrmng.png)


이제 통신창의 IP주소 콤보박스를 열어보면 입력한 2개의 IP주소를 선택할 수 있게 됩니다.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/comm/cb-ipaddr.png" width="30%" height="30%">
  <img src="../_assets/comm//bt-connect.png" width="50%">
</div>

`[연결]` 버튼을 눌러 버튼이 노란색으로 바뀌면 연결된 것입니다.
연결에 성공하면 좌측 탐색창에 로봇제어기 노드가 나타납니다. 오른쪽 마우스 버튼을 클릭한 후 팝업 메뉴에서 '로봇제어기 정보 표시' 메뉴를 클릭하십시오. 아래와 같이 Hi6/Hi7 제어기의 소프트웨어 버전, 로봇 모델, 축 수 등을 수신받아 표시해줍니다.


<div style="display: flex; gap: 20px;">
  <img src="../_assets/explorer/pmenu-rc-info.png" width="55%" height="55%">
  <img src="../_assets/explorer/dlg-rc-info.png" width="30%">
</div>

[__SOURCE](2-setting/2-pc-path.md)
# 2.2 PC경로 선택

로봇제어기의 파일을 백업하거나 편집할 때 PC로 복사해야 하므로, PC측 폴더의 경로를 지정해야 합니다. 이 경로를 현재 PC 홈 경로(current PC home path), 혹은 줄여서 `PC경로(PC path)`라고 합니다. PC경로는 아래의 방법으로 지정할 수 있습니다.

### 방법1

윈도우 탐색기에서 폴더의 아이콘을 마우스 왼쪽 버튼으로 드래그(drag)하여 통신창 위에 드롭(drop)하십시오.

![](../_assets/pcpath/pcpath1.png)
![](../_assets/pcpath/pcpath2.png)


통신창에 지정한 PC경로가 표시됩니다. 이제 PC로 복사한 파일들은 이 폴더에 저장될 것입니다.
 
![](../_assets/pcpath/pcpath3.png)

여러 로봇제어기에 대해 각기 다른 PC 폴더로 관리할 경우에는 이와 같은 드래그 & 드롭 방법으로 폴더를 바꿔가면서 작업하십시오.
표시된 경로 우측의 <img src="../_assets/pcpath/bt-folder.png"> 버튼을 클릭하면, 해당 경로가 윈도우 탐색기로 열립니다.


### 방법2

우측의 <img src="../_assets/pcpath/bt-dot3.png"> 버튼을 클릭하면 폴더 선택 대화상자가 열립니다. 폴더를 선택한 후, `[폴더 선택]` 버튼을 클릭하면 경로가 입력됩니다.

![](../_assets/pcpath/pcpath3.png)


### 방법3

탐색창의 PC 노드에 마우스 우클릭하여 팝업 메뉴를 열고 `PC 백업 경로 설정`을 선택하면, 대화상자가 열립니다. 대화상자에 경로를 타이핑 혹은 윈도우 탐색기의 경로를 복사/붙여넣기 한 후 `확인` 버튼을 클릭하십시오.

![](../_assets/pcpath/pcpath4.png)
![](../_assets/pcpath/pcpath5.png)

PC경로의 폴더 구조는 아래 그림과 같이 구성됩니다.
만일 PC 경로에 전에 백업해둔 job들이 있다면 탐색창의 PC 노드에 그림과 같이 표시됩니다.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/pcpath/pcpath10.png" width="55%" height="55%">
  <img src="../_assets/pcpath/pcpath11.png" width="40%">
</div>

[__SOURCE](2-setting/3-hrwb-file.md)
# 2.3 Workbench 파일의 저장과 불러오기

설정해놓은 작업환경을 확장자 `.hrwb`인 workbench 파일로 저장하고, 불러올 수 있습니다.
아래와 같은 항목들이 저장됩니다.

*	IP 주소 관리자에 작성된 목록
*	PC 경로 설정

workbench를 저장해보겠습니다. 기본설정을 한 후, 주 메뉴에서 `파일 - WorkBench 저장`를 선택하십시오. 원하는 경로를 선택하고 파일명을 입력한 후 저장 버튼을 클릭하십시오.

![](../_assets/file/wbfile-save.png)


Workbench 파일의 불러오기를 해 보겠습니다. HRWorkBench를 종료한 후 다시 실행한 다음, 주 메뉴에서 `파일 - WorkBench 열기`를 선택하십시오. 저장했던 파일을 선택하면, 기존의 설정들이 복원되는 것을 확인할 수 있습니다.

![](../_assets/file/wbfile-open.png)


최근 불러오기 한 경로파일명들은 주 메뉴의 File에 열거되므로, 이를 클릭하여 신속하게 파일을 열 수도 있습니다.

![](../_assets/file/wbfile-list.png)

혹은 윈도우 탐색기에서 .hrwb 파일의 아이콘을 드래그 & 드롭하여 열 수도 있습니다.

![](../_assets/file/drag-drop-hrwb.png)

[__SOURCE](3-backup-restore/README.md)
# 3. 백업과 복원


[__SOURCE](3-backup-restore/1-backup-restore.md)
# 3.1 백업과 복원

Hi6/Hi7 제어기의 파일들을 백업하거나 복원할 수 있습니다.
먼저 연결 버튼을 눌러, 제어기에 원격 접속하십시오. 탐색창에서 '로봇제어기' 노드에 마우스 우버튼으로 팝업 메뉴를 열어 'PC로 전부 백업'을 선택하면, 백업 대화상자가 나타납니다.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/backup/backup1.png" width="40%" height="40%">
  <img src="../_assets/backup/backup2.png" width="50%">
</div>

백업할 대상을 체크한 후 `[시작]` 버튼을 누르면 제어기 내의 파일들이 PC 경로로 백업됩니다. 백업이 완료되면 완료 대화상자가 표시되며, 탐색창의 PC 노드의 파일 목록이 갱신됩니다.
 
![](../_assets/backup/backup3.png)


복원방법도 이와 유사합니다.
탐색창에서 'PC' 노드에 마우스 우버튼으로 팝업 메뉴를 열어 '로봇제어기로 전부 복원'을 선택하면, 복원 대화상자가 나타납니다.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/backup/restore1.png" width="40%" height="40%">
  <img src="../_assets/backup/restore2.png" width="50%">
</div>


복원할 대상을 체크한 후 `[시작]` 버튼을 누르면 PC 경로의 파일들이 로봇제어기로 복원되고, 완료 대화상자가 표시됩니다.

{% hint style="warning" %}
복원을 수행할 때는 Hi6/Hi7 제어기는 모터off 상태여야 합니다. 모터on 상태에서 수행하면 불가 메시지가 출력됩니다.
{% endhint %}

[__SOURCE](3-backup-restore/2-job-copy-del.md)
# 3.2 job 파일 복사와 삭제

제어기 파일 전체가 아니라 일부 job파일만 복사할 수 있습니다.
먼저 로봇제어기에서 PC로 복사해 보겠습니다.
탐색창의 `로봇제어기/jobs/` 경로 밑에서 원하는 job파일들을 클릭하여 선택합니다.
여러 개의 파일을 선택하려면 아래 방법들을 사용하십시오.

<table>
<tr>
  <td><img src="../_assets/backup/job1.png"/></td>
  <td>좌 버튼을 누른 채 드래그하여 여러 파일 선택.</td>
</tr>
<tr>
  <td><img src="../_assets/backup/job2.png"/></td>
  <td>하나의 파일을 선택한 후, Shift키를 누른 채 다른 파일을 클릭하여 그 사이의 파일들을 선택.</td>
</tr>
<tr>
  <td><img src="../_assets/backup/job3.png"/></td>
  <td>ctrl키를 누른 채 여러 파일들을 각각 선택.</td>
</tr>
</table>

선택된 job 파일들에 우 버튼을 클릭한 후, `PC로 백업` 팝업 메뉴를 선택하십시오. 이력창에 복사 결과가 표시되고, 복사된 파일명들은 `PC/jobs` 노드에 표시됩니다.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/backup/job4.png" width="40%">
  <img src="../_assets/backup/job5.png" width="30%" height="30%">
</div>

다음으로 PC에서 로봇제어기로 복사해보겠습니다. 방법은 유사합니다.
탐색창의 PC/jobs/ 경로 밑에서 원하는 job파일들을 클릭하여 선택합니다.
선택된 job 파일들에 우 버튼을 클릭한 후, '로봇제어기로 복원' 팝업 메뉴를 선택하십시오.

<div style="display: flex; gap: 20px;">
  <img src="../_assets/backup/job10.png" width="40%">
  <img src="../_assets/backup/job11.png" width="30%" height="30%">
</div>

<br/>

로봇제어기의 job파일이나 PC의 job파일들은 '삭제' 팝업 메뉴로 삭제할 수 있습니다.

![](../_assets/backup/job-del.png)

[__SOURCE](4-job-var/README.md)
# 4. job과 변수의 편집


[__SOURCE](4-job-var/1-job-edit/README.md)
# 4.1 Job 파일 편집

PC로 복사된 job파일은 선호하는 텍스트 편집기로 편집해도 되지만, HRWorkBench도 편집기를 제공합니다.

[__SOURCE](4-job-var/1-job-edit/1-job-edit-wnd.md)
# 4.1.1 편집 창 열기와 배치

먼저 PC로 복사된 job 파일을 열어 편집해 보겠습니다.
탐색창의 원하는 PC측 job파일을 더블클릭하면 편집기가 열립니다. 0001.job, 0005.job, 0006.job, 0007.job의 4개의 job파일을 차례로 열어보겠습니다. 아래와 같이 마지막으로 연 0007.job의 편집 창이 공간을 채우고 있고, 파일명들은 tab에 표시되고 있습니다.
 
![](../../_assets/job-edit/job-tab01.png)


Tab을 선택하여 원하는 job을 편집할 수 있습니다. 2개의 파일을 비교하고자 할 때는 `윈도우 - 영역 나누기` 메뉴 혹은 툴 버튼으로 영역을 최대 2개로 나눌 수 있고, 한번 더 클릭하면 영역이 다시 합쳐집니다.
  
![](../../_assets/job-edit/job-tab02.png)
![](../../_assets/job-edit/job-tab03.png)

각 tab은 마우스 좌버튼으로 드래그하여 순서를 바꿀 수 있으며, `윈도우 - 다른 영역으로 탭 이동` 메뉴, 혹은 툴 버튼으로 다른 영역으로 옮길 수 있습니다.

주 메뉴의 '윈도우' 혹은 툴 막대에서 '타일' 혹은 '캐스캐이드'를 선택하면, 영역 내에서 여러 개의 job 편집 창을 나란히 배치할 수 있습니다.

![](../../_assets/job-edit/job-tab04.png)
![](../../_assets/job-edit/job-tab05.png)

편집 창은 <img src="../../_assets/job-edit/job-min.png">  버튼으로 최소화하고, <img src="../../_assets/job-edit/job-max.png"> 버튼으로 최대화 할 수 있습니다. <img src="../../_assets/job-edit/job-close.png"> 버튼을 클릭하거나 ctrl+F4를 누르면 닫힙니다.

[__SOURCE](4-job-var/1-job-edit/2-encoding.md)
# 4.1.2 인코딩 변환하여 다시 불러오기

job 파일을 열었을 때, 영어가 아닌 글자(한글, 중문 등) 주석이나 문자열이 깨져 보이는 경우가있습니다. Hi6/Hi7제어기의 job파일은 utf-8 인코딩으로 저장되어야 하는데, 다른 인코딩(가령, EUC-KR이나 GB2312)으로 저장되어 있으면 HRWorkBench와 티치펜던트에 제대로 표시되지 않습니다.

![](../../_assets/job-edit/encoding1.png) 

가령 job 파일이 확장완성형으로 되어 있다면 주 메뉴의 `Job - 인코딩 : 다른 언어로 다시 불러오기 - 한국어(ko-KR)`을 선택하십시오. job 파일이 utf-8로 변환되어 편집 창에 열리므로 글자가 제대로 표시될 것입니다. 이 상태에서 저장하면 utf-8 인코딩 파일로 저장됩니다.
(영어만으로 작성된 파일의 경우, ascii 파일과 utf-8파일은 동일하므로, 이러한 조작이 필요없습니다.)

![](../../_assets/job-edit/encoding2.png) 

[__SOURCE](4-job-var/1-job-edit/3-syntax-coloring.md)
# 4.1.3 syntax coloring과 자동 다단 들여쓰기 (smart indent)

편집 창은 가독성을 위해 기본적인 syntax coloring을 제공합니다. 주요 명령어와 문자열, 숨은 포즈, 주석, job 헤더가 고유의 색상으로 표시됩니다.

![](../../_assets/job-edit/syntax-color.png)


flow제어문의 구조를 파악하기 쉽도록, 자동 다단 들여쓰기 (smart indent) 기능도 제공됩니다. 주 메뉴 Job 혹은 툴 막대에서 '자동 들여쓰기'를 클릭하면 현재 편집 창의 job 프로그램 전체가 자동 들여쓰기 됩니다. 
     
![]()


<div style="display: flex; gap: 20px;">
  <img src="../../_assets/job-edit/smart-indent1.png" width="20%" height="20%">
  <img src="../../_assets/job-edit/smart-indent2.png" width="50%">
</div>

[__SOURCE](4-job-var/1-job-edit/4-undo-redo.md)
# 4.1.4 Undo/Redo와 저장

편집 창은 단축키로 `Ctrl+Z`와 `Ctrl+Y`로 Undo와 Redo를 제공합니다.

제목 tab 혹은 제목 막대의 파일명에 아래와 같이 `*` 표시가 있으면 편집 후 아직 저장되지 않는 내용이 있다는 의미입니다.
주 메뉴의 `파일 - 저장`, 혹은 `파일 - 다른 이름으로 저장`을 선택하여 편집 내용을 파일에 저장할 수 있습니다. 혹은 단축키 `Ctrl+S`를 누르거나 툴 막대의 <img src="../../_assets/tool-btn/tb-save.png"> 버튼을 클릭하십시오.

![](../../_assets/job-edit/title-star.png)


주 메뉴의 'Job - 저장 후 RC로 복사'를 선택하거나 툴 막대의 <img src="../../_assets/tool-btn/tb-upload2rc.png"> 버튼을 클릭하면, 저장 후 로봇제어기로 복사하여 즉시 반영까지 해줍니다.

[__SOURCE](4-job-var/1-job-edit/5-find-replace.md)
# 4.1.5 찾기/바꾸기/찾아가기

주 메뉴의 '편집 - 찾기와 바꾸기'를 선택하거나 단축키 Ctrl+F 혹은 Ctrl+F3을 눌러 찾기/바꾸기 대화상자를 열 수 있습니다. 특정한 텍스트를 선택한 상태였으면, 그 텍스트가 자동으로 '찾을 내용'에 입력됩니다. 
 
![](../../_assets/find-replace/find01.png)

대화상자의 각 옵션의 기능은 아래와 같습니다.

<table>
<tr>
  <th>이름</th>
  <th colspan=2>기능</th>
</tr>
<tr>
  <td rowspan=2>찾는 위치</td>
  <td>현재 문서</td>
  <td>현재 선택한 job 편집창 내에서만 수행.</td>
</tr>
<tr>
  <td>현재 프로젝트</td>
  <td>프로젝트의 PC 노드 아래의 모든 job에 대해 수행.</td>
</tr>
<tr>
  <td>대/소문자 구분</td>
  <td colspan=2>선택하면 대소문자를 구분</td>
</tr>
<tr>
  <td>단어 단위로</td>
  <td colspan=2>선택하면 완전한 단어에 대해서만 검색</td>
</tr>
</table>


`[이전 찾기]` 혹은 `[다음 찾기]` 버튼을 클릭하면 이전 혹은 다음 일치하는 문자열로 커서 선택이 이동합니다. `[바꾸기]` 버튼을 누르면 현재 선택된 문자열을 '바꿀 내용:'에 입력된 문자열로 교체한 후, 다음 일치하는 문자열로 이동합니다.
`[모두 찾기]` 버튼을 클릭하면, `찾는 위치`에 지정한 범위 전체를 대상으로 검색하여, 하단의 `찾기 결과` 창에 검색된 항목들을 경로파일명(행번호): 문자열의 형식으로 열거해줍니다. 특정한 항목에 대해 더블클릭하면, 해당하는 파일이 열리면서, 일치한 위치로 커서가 이동합니다.
(`찾기/바꾸기` 대화상자를 닫은 상태에서도, `Shift+F3 (이전 찾기)`과 `F3 (다음 찾기)` 단축키를 사용할 수 있습니다.)

![](../../_assets/find-replace/find02.png)


`[모두 바꾸기]` 버튼을 클릭하면, `[찾는 위치]`에 지정한 범위 전체를 대상으로 검색하여, 일치한 문자열을 `바꿀 내용:`에 입력된 문자열로 교체하면서, 하단의 `찾기 결과` 창에 검색된 항목들을 열거해줍니다.

주 메뉴의 `Job - 줄 이동`을 선택하거나 단축키 `Ctrl+G`를 눌러 찾아가기 대화상자를 열 수 있습니다. 행 번호를 입력하면 해당 행 번호로 커서가 이동합니다.

![](../../_assets/find-replace/dlg-goto.png)

[__SOURCE](4-job-var/1-job-edit/6-etc.md)
# 4.1.6 기타 기능

*	글자 크기 조정: `ctrl+마우스 휠`을 조작하면 Job 편집 화면의 글자 크기를 크거나 작게 조정할 수 있습니다. 
[__SOURCE](4-job-var/2-syntax-check.md)
# 4.2 로봇언어 문법 검사

현재 편집 중인 job파일에 대한 기본적인 문법 검사를 원격으로 수행할 수 있습니다.
아래와 같이 검사할 job파일이 열려 있는 상태에서 `주 메뉴 - Job`, 혹은 툴 막대의 `문법 검사`를 클릭하십시오.
 
![](../_assets/job-edit/syntax-check1.png)
 
![](../_assets/job-edit/syntax-check2.png)

`문법 검사` 창에 문법 에러가 있는 경로파일명과 행번호, 에러 메시지가 표시됩니다. 에러 항목을 더블클릭하면 해당 위치로 커서가 이동합니다.
 
![](../_assets/job-edit/syntax-check3.png)

이 문법 검사는 job을 실행하지 않고 수행하기 때문에, 수행 시 발생할 모든 에러를 검지하지 못합니다. 위 그림에서 예시한 job파일에서 var을 val로 잘못 표기한 것과 `move`문 `accu`의 범위 0~7을 초과한 것은 검지했습니다. 그러나 `wait`문의 I/O 변수 `do31`을 `DO31`로 잘못 표기한 것과 `tno=2`를 `tn=2`로 잘못 표기한 것은 검지하지 못했습니다. 실행 중 `DO31`와 `tn`이라는 변수가 생성될 가능성도 있기 때문에 이를 에러로 간주하지 않는 것입니다.

[__SOURCE](4-job-var/3-exec-roblang.md)
# 4.3 로봇언어 명령문 실행

job파일의 로봇언어 명령문을 원격으로 실행할 수 있습니다. 
move문이나 flow제어문은 지원하지 않으며 대입문 등 단일하게 수행될 수 있는 일부 명령만 지원합니다.
결과 확인을 위해 연결된 Hi6/Hi7 제어기의 티치펜던트에서 전역변수 창을 열어 두십시오.
Job 편집 창에 시험적으로 아래와 같은 프로그램을 작성했습니다.

![](../_assets/job-edit/exec-roblang01.png)


커서를 global msg="Hello, "에 두고 주 메뉴 Job, 혹은 툴 막대에서 '현재 행 실행'을 클릭하십시오.
 
![](../_assets/job-edit/exec-roblang02.png)


원격 실행이 성공하면 이력 창에 성공 메시지가 표시됩니다. 티치펜던트의 전역변수 창에서도 msg 변수가 생성되었음을 확인할 수 있습니다.
     
![](../_assets/job-edit/exec-roblang03.png)
![](../_assets/job-edit/exec-roblang04.png)

 
주 메뉴 Job, 혹은 툴 막대에서 'Job 실행'을 클릭하면, print문을 포함해 현재 선택된 Job 전체가 실행됩니다.

![](../_assets/job-edit/exec-roblang05.png)
![](../_assets/job-edit/exec-roblang06.png)


[__SOURCE](4-job-var/4-gvar-mon.md)
# 4.4 전역변수 모니터링과 값 설정

연결 버튼이 눌린 온라인 상태에서는 전역 변수 창이 현재 전역변수 값들을 표시해줍니다. 전역변수 창의 기능은 Hi6/Hi7 티치펜던트(TP630)의 전역변수 창과 거의 동일합니다. 
아래 링크의 사용법을 참조하십시오.

https://hrbook-hrc.web.app/#/view/doc-hi6-operation/ko-tp630/6-monitoring/3-job/3-global-variable/README?cont_model=Hi7


![](../_assets/var-edit/gvar01.png)


*	동일한 내용 : 변수 찾기, 변수 타입/이름/값 변경, 변수 생성/삭제, 배열 생성, 배열요소값 확인/변경, 객체 속성값 확인/변경, 고정 토글, 전부 불러오기/저장하기의 기능이 모두 동일합니다.
*	다른 내용 : 포즈/시프트 값에 대한 속성 편집 창은 지원되지 않고, 다른 객체형과 동일하게 펼쳐집니다.


![](../_assets/var-edit/gvar02.png)

*	<img src="../_assets/var-edit/gvar03.png"> 버튼으로 이전, 다음, 상위 경로로 이동할 수 있습니다.

[__SOURCE](4-job-var/5-gvar-copy-del.md)
# 4.5 전역변수 파일의 복사와 삭제

{% hint style="info" %}
v1.4.2 이전의 전역변수 export 기능은 이 기능으로 대체되었습니다.
{% endhint %}

변수 창에서 전역변수의 모니터링과 값 설정이 가능하지만 대량의 변수목록을 편집하기에는 한계가 있습니다.
전역변수는 Hi6/Hi7 제어기 내의 `vars.json` 파일에 저장되고, 이 중 최상위 배열 변수는 `.csv` 파일들에 저장됩니다. 이들은 모두 텍스트 파일들이기 때문에, PC로 전송받으면 쉽게 편집할 수 있습니다.

변수 파일을 백업, 복원하는 방법은 job 파일과 유사합니다. 로봇제어기의 `vars/` 폴더, 혹은 일부 파일들을 선택한 후 마우스 우클릭으로 팝업 메뉴를 여십시오. `PC로 백업 메뉴`를 선택하면 이력창에 복사 결과가 표시되고, 복사된 파일명들은 `PC/vars` 노드에 표시됩니다.

![](../_assets/var-edit/var-backup1.png)
![](../_assets/var-edit/var-backup2.png)
![](../_assets/var-edit/var-backup3.png)

다음으로 PC에서 로봇제어기로 복사해보겠습니다. 방법은 유사합니다.
탐색창의 `PC/vars/` 경로 밑에서 원하는 변수 파일들을 클릭하여 선택합니다.
선택된 변수 파일들에 우 버튼을 클릭한 후, `로봇제어기로 복원` 팝업 메뉴를 선택하십시오.

![](../_assets/var-edit/var-restore1.png)
![](../_assets/var-edit/var-restore2.png)

로봇제어기나 PC의 변수 파일들은 '삭제' 팝업 메뉴로 삭제할 수 있습니다. 로봇제어기의 변수 파일을 삭제하면 해당 변수 또한 삭제됩니다.

![](../_assets/var-edit/var-del.png)

{% hint style="warning" %}
변수 복원이나 삭제를 수행할 때는 Hi6/Hi7 제어기는 재생 정지 상태여야 합니다.재생 중 수행하면 불가 메시지가 출력됩니다.
{% endhint %}

PC에서 변수 파일은 더블클릭하면 텍스트 편집 윈도우가 열립니다. 로봇제어기의 변수 파일을 더블클릭하면 PC/vars/로 일단 백업을 한 후 PC측의 파일을 엽니다.

![](../_assets/var-edit/csv-edit.png)

[__SOURCE](5-log/README.md)
# 5. 제어기 이력 확인


[__SOURCE](5-log/1-event-log/README.md)
# 5.1 제어기 이벤트 이력 모니터링


[__SOURCE](5-log/1-event-log/1-event-log-mon.md)
# 5.1.1 이벤트 이력 모니터링 창

하단에 `이벤트 이력 - RC`와 `이벤트 이력 - PC`의 2개의 탭을 볼 수 있습니다.
`이벤트 이력 - RC`는 Hi6/Hi7 제어기가 이더넷으로 연결된 상태에서 제어기 내의 이벤트 이력과 새로 발생하는 이벤트들을 모니터링하는 창입니다.
`이벤트 이력 - PC`는 PC경로의 `log/` 폴더에 있는 이벤트 이력 파일들을 읽어들여 보여주는 창입니다. (Hi6/Hi7 제어기 V60.05-04 및 이후 버전에서 지원됩니다.)

이 창은 Hi6/Hi7의 티치펜던트에서 제공하는 U/I와 유사한 기능을 제공합니다. 이벤트 이력들은 발생 시점의 역순으로 표시되며, 새로 발생한 이벤트들은 노란 바탕색으로 표시됩니다.

![](../../_assets/log/evlog01.png)


창의 상단에는 이벤트 타입 필터 버튼들이 있으며, 눌려있는 타입의 이벤트만 표시됩니다. 가령 위 그림에서는 에러(E)와 경고(W), 알림(N) 타입만 표시되고 있습니다. (필터 버튼 조작 후엔 필터 우측의 업데이트 버튼(<img src="../../_assets/log/evlog-bt-update.png">)을 클릭해야 화면이 갱신됩니다.)

<table>
<tr>
  <th>분류</th>
  <th>U/I</th>
  <th>설명</th>
</tr>
<tr>
	<td rowspan=9>필터</td>
  <td>전부</td>
  <td>모든 이력 종류 켜기 혹은 끄기 (토글)</td>
</tr>
<tr>
  <td>E (Error)</td>
  <td>에러 이력 표시</td>
</tr>
<tr>
  <td>W (Warning)</td>
  <td>경고 이력 표시</td>
</tr>
<tr>
  <td>N (Notice)</td>
  <td>알림 이력 표시</td>
</tr>
<tr>
  <td>ST (Start/Stop)</td>
  <td>기동/정지 이력 표시</td>
</tr>
<tr>
  <td>P (Periodic)</td>
  <td>주기적 상태 이력 표시</td>
</tr>
<tr>
  <td>OP (Operation)</td>
  <td>조작 이력 표시</td>
</tr>
<tr>
  <td>IO (I/O)</td>
  <td>I/O 이력 표시</td>
</tr>
<tr>
  <td>H (History)</td>
  <td>실행 이력 표시</td>
</tr>
<tr>
  <td>업데이트</td>
  <td><img src="../../_assets/log/evlog-bt-update.png"></td>
  <td>선택된 필터 적용</td>
</tr>
<tr>
  <td></td>
  <td><img src="../../_assets/log/evlog-cb-cnt.png"></td>
  <td>창에 몇 개의 이력을 표시할 지 선택한 후, 화면 갱신</td>
</tr>
<tr>
  <td>다시 로드 후 업데이트</td>
  <td><img src="../../_assets/log/evlog-bt-update.png"></td>
  <td>제어기 혹은, 파일로부터 이력을 다시 읽어 테이블에 표시.</td>
</tr>
<tr>
  <td rowspan=2><img src="../../_assets/log/bt-dot3.png"><br>(팝업 메뉴)</td>
  <td>이력 파일들로 저장</td>
  <td>제어기 메모리에 쌓인 현재까지의 이력들을 제어기의 log 파일로 저장.</td>
</tr>
<tr>
  <td>이력 파일들 클리어</td>
  <td>제어기의 메모리와 log 파일의 이력들을 모두 클리어.</td>
</tr>
<tr>
  <td rowspan=2></td>
  <td><img src="../../_assets/log/bt-lock.png"></td>
  <td>새로운 이력 모니터링을 중단</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-trash.png"></td>
  <td>이력 창의 항목들을 클리어</td>
</tr>
<tr>
  <td rowspan=2></td>
  <td><img src="../../_assets/log/bt-aux.png"></td>
  <td>이벤트 보조 데이터 창 열기</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope.png"></td>
  <td>스코프 열기</td>
</tr>

</table>


[__SOURCE](5-log/1-event-log/2-event-find.md)
# 5.1.2 이벤트 찾기

이벤트 이력 창에서 `편집 - 찾기와 바꾸기` 메뉴를 선택하거나, `Ctrl+F` 키를 누르면, 이벤트 찾기 대화상자가 열립니다.
`찾을 내용:`에 찾을 코드나 메시지, 날짜 시간, 혹은 프로그램 카운트를 입력하고 `다음 찾기(N)` 혹은 `이전 찾기(P)`를 클릭하면, 현재 선택된 행부터 검색하여 해당 문자열을 포함하는 다음 혹은 이전 행을 선택해줍니다.

![](../../_assets/log/evlog-find.png) 

대화상자의 각 옵션의 기능은 아래와 같습니다.

<table>
<tr>
  <th>이름</th>
  <th>기능</th>
</tr>
<tr>
  <td>찾는 위치</td>
  <td>이벤트 이력-RC와 이벤트 이력-PC 중, 어느 이력창에서 검색을 수행할 지를 표시해줍니다. 클릭하여 선택할 수는 없습니다.<br>
  (이벤트 이력-RC 창과 이벤트 이력-PC 창의 이벤트 찾기 대화상자는 따로 존재합니다. 해당 이력 창에서 대화상자를 연 후 찾기를 수행하십시오.)
</td>
</tr>
<tr>
  <td>대/소문자 구분</td>
  <td>선택하면 대소문자를 구분</td>
</tr>
<tr>
  <td>단어 단위로</td>
  <td>선택하면 완전한 단어에 대해서만 검색</td>
</tr>
</table>


[__SOURCE](5-log/1-event-log/3-event-text-copy.md)
# 5.1.3 이벤트 텍스트 복사

선택한 이벤트 이력에 우버튼을 클릭하면 팝업 메뉴가 열립니다.

![](../../_assets/log/evlog-text-copy.png) 

*	셀 텍스트 복사 : 선택한 행, 열의 텍스트를 클립보드에 복사합니다.
*	행 텍스트 복사 : 선택한 행의 모든 열의 텍스트를 클립보드에 복사합니다. 각 열의 텍스트들은 `|` 문자로 구분됩니다.

[__SOURCE](5-log/2-aux-data/README.md)
# 5.2 보조 데이터

<img src="../../_assets/log/bt-aux.png"> 버튼을 클릭하면 총 5가지의 이벤트 보조 데이터 창들이 열립니다.

![](../../_assets/log/evlog-aux-panel.png) 

<table>
<tr>
  <th>panel명</th>
  <th>내용</th>
  <th>지원 이벤트 타입</th>
</tr>
<tr>
  <td>aux.pose</td>
  <td>프로그램카운터와 포즈 데이터</td>
  <td>에러/경고/기동/정지</td>
</tr>
<tr>
  <td>aux.sin</td>
  <td>시스템입력</td>
  <td>에러/경고/기동/정지</td>
</tr>
<tr>
  <td>aux.sout</td>
  <td>시스템출력</td>
  <td>에러/경고/기동/정지</td>
</tr>
<tr>
  <td>aux.din</td>
  <td>범용입력</td>
  <td>주기적 상태/IO</td>
</tr>
<tr>
  <td>aux.dout</td>
  <td>범용출력</td>
  <td>주기적 상태/IO</td>
</tr>
</table>

[__SOURCE](5-log/2-aux-data/1-aux-pose.md)
# 5.2.1. 포즈데이터 (aux.pose)

에러/경고/기동/정지 이벤트 행을 클릭하면, 이벤트 발생 시점의 프로그램카운터와 각 축 값(mm|deg)가 표시됩니다.
프로그램카운터와 포즈데이터 보조 데이터는 에러와 경고 이벤트에만 기록되기 때문에, 다른 종류의 이벤트 행을 클릭하면 데이터가 희미하게 표시됩니다. 이는 해당 이벤트 바로 전에 기록된 에러/경고/기동/정지 이벤트의 보조데이터를 그대로 보여주는 것으로서 정확하지 않을 수 있습니다.


![](../../_assets/log/evlog-aux-pose1.png)
![](../../_assets/log/evlog-aux-pose2.png)

[__SOURCE](5-log/2-aux-data/2-aux-sio.md)
# 5.2.2 시스템 입출력 (aux.sin/sout)

에러/경고/기동/정지 이벤트 행을 클릭하면, 이벤트 발생 시점의 시스템 입력과 출력이 표시됩니다.
시스템 입출력 보조정보는 에러와 경고 이벤트에만 기록되기 때문에, 다른 종류의 이벤트 행을 클릭하면 데이터가 희미하게 표시됩니다. 이는 해당 이벤트 바로 전에 기록된 에러/경고/기동/정지 이벤트의 보조데이터를 그대로 보여주는 것으로서 정확하지 않을 수 있습니다.

![](../../_assets/log/evlog-aux-sin.png)

[__SOURCE](5-log/2-aux-data/3-aux-dio.md)
# 5.2.3 범용 입출력 (aux.din/dout)

주기적 상태나 IO 이벤트 행을 클릭하면, 범용 입력과 출력이 표시됩니다.

![](../../_assets/log/evlog-aux-dout.png)


상단의 콤보박스로, 표시할 신호 그룹 `fb0~fb9`을 선택할 수 있습니다. IO 이벤트는 임의의 `dio`값이 변경될 때에만 해당 변경(differential) 정보만 담아 발생합니다. 그리고, 주기적 상태 이벤트는 Hi6/Hi7 제어기에서 1분마다 `fb` 그룹 1개씩만 전체 `dio` 정보를 담아 발생합니다. HRWorkBench는 이 정보들을 누적하여 각 이벤트 행에 대해 범용 입출력 창에서 모든 `fb` 그룹의 모든 `dio` 정보를 보여줍니다.
따라서, `dio` 정보가 충분히 누적되지 않은 과거의 이벤트 행을 클릭하면 아래 그림과 같이 데이터가 표시되지 않고 `?` 기호로 나타납니다.

![](../../_assets/log/evlog-aux-dout2.png)

[__SOURCE](5-log/3-scope-log/README.md)
# 5.3 스코프 이력 (Scope log)

(본 기능은 Hi6/Hi7 제어기 V60.05-04 및 이후 버전에서 지원됩니다.)

[__SOURCE](5-log/3-scope-log/1-scope-log-intro.md)
# 5.3.1 스코프 이력이란?

Hi6/Hi7 제어기는 `E160 충돌검지`와 같은 중대 에러나 경고가 발생할 때, 각 축의 위치/속도/가속도/상태코드 등 분석에 필요한 5ms의 샘플링 주기, 30초간의 (발생 전 25초 + 발생 후 5초) 데이터를 파일로 저장하는데 이를 스코프 이력이라고 합니다.
스코프 이력은 제어기의 `log/` 폴더에 .json과 .bin 파일 쌍으로 저장됩니다. (용량이 크기 때문에 일정 개수만 저장되고 이전 데이터는 삭제됩니다.)
원격의 로봇제어기와 PC경로에 저장되어 있는 스코프 이력들은 탐색 창의 `log/` 폴더에 표시되는데, 노드의 이름은 년월일_시분초의 형식의 파일 저장 시점입니다.

![](../../_assets/log/scopelog01.png)

[__SOURCE](5-log/3-scope-log/2-scope-log-open.md)
# 5.3.2 스코프 열기

![](../../_assets/log/scopelog02.png)

중대 에러나 경고 이벤트 행을 선택하고 우상단의 <img src="../../_assets/log/bt-scope.png"> 버튼을 클릭하면 스코프 창이 열립니다.

(해당 이벤트 시점의 스코프 이력 파일이 없으면 열리지 않습니다.)

(탐색 창의 `log/` 폴더의 스코프 이력 항목을 더블클릭해서 열 수도 있습니다.)

![](../../_assets/log/scopelog03.png)

좌상단의 <img src="../../_assets/log/bt-scopelog-field.png"> 버튼을 클릭하면, 필드(항목) 선택 창이 열립니다.

![](../../_assets/log/scopelog04.png)

필드 선택 창의 각 항목은 이름과 단위, 설명을 표시하고 있습니다.


<table>
<tr>
  <th>버튼</th>
  <th>기능</th>
  <th>비고</th>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-trash.png"></td>
  <td>모든 체크를 해제합니다.</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-check.png"></td>
  <td>선택한 행들을 한번에 체크합니다.<br>
		(마우스 좌버튼으로 드래그하거나, Ctrl+좌버튼, 혹은 Shift+좌버튼으로 여러 항목 행을 선택할 수 있습니다.)
	</td>
  <td><img src="../../_assets/log/scopelog07.png"></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-uncheck.png"></td>
  <td>선택한 행들을 한번에 체크 해제합니다.</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-csv.png"></td>
  <td>.csv 파일로 익스포트(export)합니다.</td>
  <td>외부 소프트웨어에서 활용하기 위한 용도입니다.</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-ok.png"></td>
  <td>필드 선택 창을 닫고, 체크된 항목의 그래프를 표시합니다.</td>
  <td></td>
</tr>
</table>

가령 qr[0]~qr[5]는 단위가 mm 혹은 rad이며, 1~6축의 `joint position (축 위치)` 데이터입니다. 

충돌이 발생했을 때의 1축~3축의 데이터를 확인하고자 한다면 qr[0]~qr[2]를 체크한 후 `[확인]` 버튼을 클릭합니다. 

![](../../_assets/log/scopelog05.png)


몇 초 후 그래프가 열립니다.

![](../../_assets/log/scopelog06.png)

[__SOURCE](5-log/3-scope-log/3-graph.md)
# 5.3.3 그래프의 조작

<table>
<tr>
  <th>버튼</th>
  <th>기능</th>
  <th>그래프 상에서의 조작 법</th>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-adddel.png"></td>
  <td>그래프를 추가하거나 선택된 그래프를제거합니다.</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-field.png"></td>
  <td>항목(필드) 선택 창을 엽니다.</td>
  <td><img src="../../_assets/log/scopelog07.png"></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-arrow.png"></td>
  <td>normal 커서 모드를 선택합니다.<br>(마커 이동)</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-zoom-t.png"></td>
  <td>T(시간) 축으로 영역을 선택하여 확대합니다.</td>
  <td>마우스 좌 버튼 누른 채 드래그하여 확대할 영역 선택</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-zoom-yt.png"></td>
  <td>Y(수직) 축, T(시간) 축으로 영역을 선택하여 확대합니다.</td>
  <td>마우스 좌 버튼 누른 채 드래그하여 확대할 영역 선택</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-zoom-out.png"></td>
  <td>확대하기 이전 상태로 한 단계 축소합니다.</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-pan-t.png"></td>
  <td>확대된 상태에서 T(시간) 축으로 이동(pan)합니다.</td>
  <td>마우스 좌 버튼 누른 채 좌우 이동</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-pan-yt.png"></td>
  <td>확대된 상태에서 Y(수직) 축, T(시간) 축으로 이동(pan)합니다.</td>
  <td>마우스 좌 버튼 누른 채 상하좌우 이동</td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scopelog-marker.png"></td>
  <td>마커(marker) 테이블을 열고 닫습니다. (토글)</td>
  <td></td>
</tr>
<tr>
  <td><img src="../../_assets/log/bt-scope-csv2.png"></td>
  <td>.csv 파일로 저장합니다.</td>
  <td></td>
</tr>
</table>

------------------

하단에 그래프를 하나 더 추가해 봅시다.

<img src="../../_assets/log/bt-scopelog-add.png"> 버튼을 클릭하면 하단에 그래프가 하나 더 추가됩니다. 하단 그래프의 녹색 테두리는 현재 선택된 그래프임을 의미합니다. (normal 커서로 그래프 표면을 좌 클릭하여 선택할 수 있습니다.)

![](../../_assets/log/scopelog11.png)

<img src="../../_assets/log/bt-scopelog-field.png"> 버튼을 클릭한 후, dqm[0]~dqm[2]를 체크하여 1~3축의 속도 그래프를 함께 표시해봅시다.

![](../../_assets/log/scopelog12.png)

<img src="../../_assets/log/bt-scopelog-zoom-yt.png"> 를 클릭한 후 그래프 일부를 드래그하여 확대해 봅니다.

![](../../_assets/log/scopelog13.png)
![](../../_assets/log/scopelog14.png)

<img src="../../_assets/log/bt-scopelog-pan-yt.png"> 를 클릭한 후 그래프에 마우스 좌버튼으로 드래그하면 Y(값)축과 T(시간)축으로 이동(pan)할 수 있습니다. 두 개의 그래프는 T(시간)축이 항상 동기화되어 이동합니다.

[__SOURCE](5-log/3-scope-log/4-marker.md)
# 5.3.4 마커(marker)

<img src="../../_assets/log/bt-scopelog-marker.png">  버튼을 클릭하면 마커 테이블이 열립니다. (한번 더 클릭하면 닫힙니다.)

좌측의 <img src="../../_assets/log/bt-marker-add.png"> 버튼을 클릭하면 테이블에 마커 행 M0이 추가되면서 그래프 상에 M0 마커 선(수직의 점선)이 표시됩니다.

(확대된 영역 밖에 있을 경우에는 보이지 않습니다. 다시 축소한 후 찾아보십시오.)
 
 ![](../../_assets/log/scopelog21.png)

마우스 좌버튼으로 마커 선을 드래그하여 이동시킬 수 있습니다. 마커 선이 위치한 시점(timepoint)과 절대 시간(시:분:초.usec), 그리고 해당 시점의 각 항목(field)의 값이 테이블에 표시됩니다.

<img src="../../_assets/log/bt-marker-add.png"> 버튼을 클릭할 때마다 마커 선과 테이블 행이 추가됩니다. (M1, M2,...)

<img src="../../_assets/log/bt-marker-del.png"> 버튼을 클릭하면 마커 테이블의 선택된 행의 마커가 제거됩니다.

[__SOURCE](5-log/3-scope-log/5-export2csv.md)
# 5.3.5 .csv 파일로 익스포트 (export)

스코프 이력 데이터를 마이크로소프트 엑셀(Excel)이나 MATLAB 등 다른 소프트웨어로 분석하려 한다면, .csv (comma-separated values) 표준 형식 파일로 저장하면 됩니다.
그래프를 선택한 후, <img src="../../_assets/log/bt-scope-csv.png">  버튼을 클릭하면 파일 저장 대화상자가 열립니다. 경로 파일명을 지정하고 저장 버튼을 클릭합니다.


![](../../_assets/log/scopelog31.png)
<br><br>
![](../../_assets/log/scopelog32.png)

아래 그림은 저장된 파일을 Excel에서 열어 차트 도구로 시각화 해 본 예입니다.

![](../../_assets/log/scopelog33.png)

[__SOURCE](6-rc-setting/README.md)
# 6. 제어기 설정의 확인과 포팅


[__SOURCE](6-rc-setting/1-rc-set-view.md)
# 6.1 제어기 설정의 확인

PC로 복사된 설정 파일들의 내용을 확인할 수 있습니다.
탐색창에서 `PC/project/` 폴더 안에는, 설정을 담고 있는 .json 파일들이 있습니다. 원하는 `.json` 파일에 대해 마우스 우버튼 팝업 메뉴에서 트리뷰를 선택하면 json 트리뷰 대화상자가 열립니다.

![](../_assets/rc-setting/rcset-01.png)
![](../_assets/rc-setting/rcset-02.png)

계층적인 속성 구조와 설정값들을 확인할 수 있습니다. 값을 편집할 수는 없습니다.

속성명이나 값을 검색하고 싶다면, Ctrl+F 키로 찾기 대화상자를 열어 검색을 수행하십시오.

![](../_assets/rc-setting/rcset-find.png)

[__SOURCE](6-rc-setting/2-rc-set-porting/README.md)
# 6.2. 제어기 설정의 포팅


[__SOURCE](6-rc-setting/2-rc-set-porting/1-intro.md)
# 6.2.1. 개요

가령 A 로봇제어기의 특정 `.json` 설정파일을 B 로봇제어기로 복사하고 전원을 재투입하면, 해당 A 제어기의 해당 설정을 B 제어기에 동일하게 적용할 수 있습니다.
그러나, 만일 `.json` 파일의 일부 설정(혹은 전역변수)만을 다른 제어기에 동일하게 적용하고 싶다면, A 제어기의 `.json` 파일의 해당 부분 문자열을 복사하여, B 제어기 `.json` 파일의 같은 부분에 덮어씌우는 작업을 해야 합니다. 이러한 수작업은 손이 많이 가며, 실수로 `.json` 형식을 손상시켜 자칫 제어기의 부팅 불능이나 오동작을 유발할 수 있기 때문에 주의해야 합니다.
HRWorkbench의 설정 포팅 기능을 사용하면 비교적 쉽고 안전하게 이러한 작업을 할 수 있습니다. 가령 작업장 내에 4개의 아크용접 작업셀 C1~C4가 있는 상황을 가정해 봅시다. 작업셀 C1의 아크용접 설정과 교시를 완료한 상태에서, 용접조건 `cnd_1000` 이상 `cnd_1100` 미만을 C2~C4에 수평 전개해야 한다면, C1의 해당 설정을 익스포트(export)하여 C2~C4에 각각 임포트(import)하면 됩니다. 이를 수행하는 절차를 예시로 포팅 기능을 설명하겠습니다.

![](../../_assets/rc-setting/rcset-port-concept.png)

[__SOURCE](6-rc-setting/2-rc-set-porting/2-export-import.md)
# 6.2.2  익스포트와 임포트

PC에 C1~C4 제어기 각각의 백업 폴더가 있고, 각 제어기가 전체 백업된 상황에서 실습을 시작하겠습니다.

![](../../_assets/rc-setting/rcset-port-01.png)

먼저, C1 제어기의 PC경로를 선택합니다.
 
 ![](../../_assets/rc-setting/rcset-port-02.png)

`PC/project/arc_weld.json` 파일에 대해 트리뷰를 열고, cnd_1001 ~ cnd_1092를 선택합니다. (SHIFT, Ctrl키 조합으로 여러 개의 항목을 선택할 수 있습니다.)

![](../../_assets/rc-setting/rcset-port-03.png)
![](../../_assets/rc-setting/rcset-port-04.png)

선택 항목에 대해 마우스 우클릭으로 팝업 메뉴를 열어 익스포트를 선택합니다.
 
![](../../_assets/rc-setting/rcset-port-05.png)

적당한 json 파일명을 입력하고 저장을 클릭합니다. (부분 json 파일은 `.part.json` 확장자를 붙이도록 합시다.)
 
 ![](../../_assets/rc-setting/rcset-port-06.png)

탐색창의 `PC/project/`에 `cnd_1000.part.json` 파일이 저장된 것을 볼 수 있습니다. (이 파일의 내용도 트리뷰로 열어 볼 수 있습니다.) 팝업 메뉴로 생성된 파일을 복사합니다.

![](../../_assets/rc-setting/rcset-port-07.png)

C2 제어기의 PC경로를 선택하고, `PC/project/` 에 붙여넣기를 수행합니다.
(HRWorkBench 대신, 윈도우 탐색기 등 다른 수단으로 복사해도 됩니다.)
 
![](../../_assets/rc-setting/rcset-port-08.png)

붙여넣어진 `cnd_1000.part.json` 파일의 트리뷰를 엽니다.

![](../../_assets/rc-setting/rcset-port-09.png)

트리뷰의 내용을 확인하고 최상위 노드인 `cnd_1000.part.json`에 팝업 메뉴를 열어 `임포트 -> arc_weld.json` 을 실행합니다.
 
![](../../_assets/rc-setting/rcset-port-10.png)
![](../../_assets/rc-setting/rcset-port-11.png)

C3과 C4에 대해서도 동일하게 수행합니다.
(각 폴더의 `cnd_1000.part.json`은 임포트 후 삭제해도 무방합니다.)

참고로, 전역변수도 설정과 동일한 방법으로 익스포트, 임포트를 할 수 있습니다.

![](../../_assets/rc-setting/rcset-port-12.png)

[__SOURCE](6-rc-setting/2-rc-set-porting/3-export-freq-path.md)
# 6.2.3 자주 사용하는 경로들의 익스포트

여러 경로들의 설정을 익스포트하는 조작을 반복적으로 자주 수행할 경우에는, 매번 해당 경로들을 선택하는 것이 번거로울 수 있습니다.

자주 사용하는 경로들의 목록을 미리 파일로 작성해놓고, 이를 트리뷰에 적용하여 선택을 쉽고 빠르게 할 수 있습니다.

간단한 예제로서, `arc_weld.json`의 `arc_conds/` 이하 4개의 항목, `lvs_tracking/` 이하 4개의 항목을 이 방법으로 선택해 보겠습니다.

![](../../_assets/rc-setting/rcset-freq-1.png)
![](../../_assets/rc-setting/rcset-freq-2.png)

텍스트 편집기를 이용하여 PC의 임의의 폴더에 아래와 같은 .json 파일을 작성합니다. 파일 형식은 json 문법(https://www.json.org/json-ko.html)을 준수해야 하지만, 파일명은 중요하진 않습니다. 

- often_used_path.json
	```json
	{
		"lvs gains": [
			"lvs_tracking.d_gain_0",
			"lvs_tracking.d_gain_1",
			"lvs_tracking.p_gain_0",
			"lvs_tracking.p_gain_1"
		],
		"arc.cond 1001~1004" : [
			"arc_conds.cnd_1001",
			"arc_conds.cnd_1002",
			"arc_conds.cnd_1003",
			"arc_conds.cnd_1004"
		]
	}
	```

위 예를 보면 `lvs gains`와 `arc.cond 1001~1004`는 콤보박스에 열거할 그룹명입니다. 각 그룹의 값은 경로 문자열 배열, 즉 `[ ]` 안에 열거된 형태로 작성해야 합니다.

(특정 항목의 경로는 아래 그림과 같이 항목을 선택한 상태에서 트리뷰 대화상자 상단의 콤보박스를 보면 확인할 수 있습니다.)

![](../../_assets/rc-setting/rcset-freq-3.png)

윈도우 탐색기에서 작성된 `.json` 파일을 드래그하여 트리뷰 상단 콤보박스 위에 드롭합니다.
 
![](../../_assets/rc-setting/rcset-freq-4.png)

콤보박스를 열어보면, 작성한 그룹명들이 보입니다. 가령 `lvs gains`를 선택하면 해당하는 경로들이 자동으로 선택됩니다.
 
![](../../_assets/rc-setting/rcset-freq-5.png)

좌상단의 <img src="../../_assets/rc-setting/bt-export.png"> (익스포트) 버튼을 클릭하면 선택한 그룹의 항목들이 익스포트 됩니다.

![](../../_assets/rc-setting/rcset-freq-6.png)
