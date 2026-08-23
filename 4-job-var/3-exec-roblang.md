# 4.3 로봇언어 명령문 실행

job파일의 로봇언어 명령문을 원격으로 실행할 수 있습니다. 
move문이나 flow제어문은 지원하지 않으며 대입문 등 단일하게 수행될 수 있는 일부 명령만 지원합니다.
결과 확인을 위해 연결된 ${cont_model} 제어기의 티치펜던트에서 전역변수 창을 열어 두십시오.
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

