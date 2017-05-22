# 레이어 모듈
 특별한 기능 없이 간단한 레이어를 사용할 때 사용해주세요.

# STEP.1 : HTML 파일 정의
<code>
<style type="text/css">
.top_cnts2{width:400px; height:400px;border:0px solid #2bA5B3;position:absolute;z-index:9999;left:100px;top:180px;display:none;}
#closeBox2{position:absolute;left:0px;top:400px;height:20px;width:400px;background-color:#000000;margin-top:0;padding:0;}
#closeBox2 .closeLeft{float:left;padding-left:4px;margin-top:2px;}
/*#closeBox .closeLeft img{}*/
#closeBox2 .closeRight{float:right;padding-right:10px;}
#closeBox2 .closeRight img{margin-top:1px;}
#closeBox2 .closeRight:after{clear:both;content:"";display:block;}

.top_cnts3{width:600px; height:400px;border:0px solid #2bA5B3;position:absolute;z-index:9999;left:530px;top:180px;display:none;}
#closeBox2.add {width:600px}
</style>
<div class="top_cnts2" id="top_cnts">
	<a href="http://realclinic.co.kr/inquiry/notice_view.php?num=18" target="_parent"><img src="./images/popup/spring_pop.jpg"></a>
	<div id="closeBox2">
		<p class="closeLeft">
			<input style='border:0px' type='checkbox' class="nomorepop" name='chkbox' id='chkbox' >
			<a href="#!"><img src="./images/txt.png" alt="오늘하루 안보임?" /></a>
		</p>
		<p class="closeRight closeBtn"><a href="#!;"><img src="./images/exbtn.png" alt="btnclose" /></a></p>
	</div>
</div>
</code>
# STEP.2 : JAVSCRIPT 호출
	var $layer = new layer({
		layerid : 'top_cnts',
		cookie_name : 'popup_1',
		closeBtnClassName : 'closeBtn',
		inputClassName : 'nomorepop'
	})
