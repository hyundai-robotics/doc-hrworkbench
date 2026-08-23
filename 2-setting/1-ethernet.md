# 2.1 이더넷 연결

HRWorkBench와 ${cont_model}로봇제어기는 같은 이더넷 네트워크로 연결되어야 합니다.
연결해야 할 ${cont_model} 제어기가 2대인데, 각각의 IP주소가 192.168.1.150과 192.168.1.151이고, PC의 IP 주소는 192.168.1.100 이라고 가정하겠습니다. (허브를 통해 서로 연결된 장치들은 모두 같은 서브네트워크인 192.168.1.XXX 여야 합니다.)

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
연결에 성공하면 좌측 탐색창에 로봇제어기 노드가 나타납니다. 오른쪽 마우스 버튼을 클릭한 후 팝업 메뉴에서 '로봇제어기 정보 표시' 메뉴를 클릭하십시오. 아래와 같이 ${cont_model} 제어기의 소프트웨어 버전, 로봇 모델, 축 수 등을 수신받아 표시해줍니다.


<div style="display: flex; gap: 20px;">
  <img src="../_assets/explorer/pmenu-rc-info.png" width="55%" height="55%">
  <img src="../_assets/explorer/dlg-rc-info.png" width="30%">
</div>
