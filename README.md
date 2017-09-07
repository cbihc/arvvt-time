# arvvt-time
<html>
	<head>
    	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    	<title></title>
    </head>
    <style>
    	p{
			border:gray 1px solid;
			width:300px;
			height:35px;
			border-top:none;
			border-left:none;
			border-right:none;	
		}
		#agg{
			border:2px solid black;
			height:25px;
			width:60px;
			margin-top:-23px;
		}
    </style>
    <script>
    	window.onload = function(){
			var oPr=document.getElementById('price');//价格
			var oMi=document.getElementById('minus');//减少
			var oAm=document.getElementById('am');//数量
			var oPl=document.getElementById('plis');//加多
			var oAgg=document.getElementById('agg');//总金
				oAgg.value=parseFloat(oPr.value);
			oMi.onclick = function(){
					
					if(parseFloat(oAm.value)>1){
					oAm.value=parseInt(oAm.value)-1;
					oAgg.value =parseFloat(oPr.value)*parseFloat (oAm.value);
					}else{
						alert(4);
					}	
				
			}	
			oPl.onclick = function(){
				
			oAm.value=parseInt(oAm.value)+1;
			oAgg.value =parseFloat(oPr.value)*parseFloat (oAm.value);
				
			}
			
		}
    </script>
    <body>
    	<p>价格: <input type="text" value='10.75' id="price" readonly></p>
        <p>数量: <input type="button" value="-" id="minus">
        <input type="text" value='1' id="am" readonly>
        <input type="button" value="+" id='plis'></p>
        总金额:<input stype="text" value='10.5' id="agg">
    </body>
</html>
