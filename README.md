# WP-HW4

<html>
<head>
<meta HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=big5">
</head>

<body>
<h2>選擇學院</h2>
<hr>

<script>
department=new Array();
department[0]=["請選擇"];
department[2]=["會計學系","國際經營與貿易學系","國際經營與貿易學系","國際企業管理全英語學士班","財稅學系","合作經濟暨社會事業經營學系","統計學系","經濟學系","企業管理學系","行銷學系","國際企業管理學士學位學程(英語專班)","商學進修學士學位學程","財經法律研究所","科技管理碩士學位學程","產業碩士專班","商學專業碩士在職學位學程","商學博士學位學程"];	// 商學院
department[1]=["資訊工程學系","電機工程學系","電子工程學系","自動控制工程學系","通訊工程學系","資電不分系榮譽班","資訊電機工程碩士在職學位學程","產業研發碩士專班","生醫資訊暨生醫工程碩士學位學程","視光科技碩士在職學位學程","電機與通訊工程博士學位學程"];	//資電學院
department[3]=["澳洲墨爾本皇家理工大學商學與創新雙學士學位學程",
"美國聖荷西州立大學商學大數據分析雙學士學位學程",
"美國普渡大學電機資訊雙學士學位學程",
"西班牙薩拉戈薩大學物流供應鏈管理與創新創業雙碩士學位學程",
"國際經營管理碩士學位學程"];			// 國際科技與管理學院
department[4]=["機械與電腦輔助工程學系","纖維與複合材料學系","工業工程與系統管理學系", "化學工程學系","航太與系統工程學系","精密系統設計學士學位學程","電聲碩士學位學程", "綠色能源科技碩士學位學程","創意設計碩士學位學程","材料與製造工程碩士在職專班","智能製造與工程管理碩士在職學位學程","機械與航空工程博士學位學程"];				// 工學院

function renew(index){
	for(var i=0;i<department[index].length;i++)
		document.myForm.member.options[i]=new Option(department[index][i], department[index][i]);	
	document.myForm.member.length=department[index].length;	
	
}
</script>

<form name="myForm">
系別：
<select onchange="renew(this.selectedIndex);">
	<option value="">請選擇
	<option value="資電學院">資電學院
	<option value="商學院">商學院
	<option value="國際科技與管理學院">國際科技與管理學院
	<option value="工學院">工學院
</select>

學程：
<select name="member" >
	<option value="">請由左方選取系別
</select>
</form>

<hr>
</body>
</html>
