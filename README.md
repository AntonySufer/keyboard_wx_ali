# keyboard_wx_ali
H5 模拟支付宝，微信支付键盘
```js
<!DOCTYPE html>
<html>
<head>
	<title>模拟密码输入框效果-练小习-caihong.cc</title>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, user-scalable=no, initial-scale=1.0" />
	<script src="http://code.jquery.com/jquery-2.1.4.min.js"></script>
	<style>
		*{
			margin: 0;
			padding: 0;
			list-style: none;
		}
		body{
		    -webkit-tap-highlight-color: transparent;
		    font-family: "Helvetica Neue",Helvetica,STHeiTi,Arial;
		    font-size: 12px;
		    background-color: #f0f0f0;
		}
		h1{
			font-size: 14px;
			font-weight: 400;
			text-align: center;
			color: #ff6600;
			padding: 0 0 20px;
		}
		.box{
			margin: 20px;
			padding: 20px;
			background: #fff;
			text-align: center;
		}
		input{
			margin: 0;
		    padding: 0;
		    width: 1px;
		    opacity: 0;
		    height: 1px;
		    border: none;
		}
		label{
			display: block;
		}
		ul{
			border: 1px solid #c8c8c8;
		    font-size: 0;
		    display: inline-block;
		    position: relative;
		    font-size: 0;
		}
		ul li{
			display: inline-block;
		    width: 35px;
		    height: 35px;
		    font-size: 24px;
		    font-weight: 700;
		    text-align: center;
		    line-height: 40px;
		    border-left: 1px solid #e6e6e6;
		    vertical-align: middle;
		    overflow: hidden;
		}
		ul li:first-child {
		    border-left: none;
		}
		a{
		    height: 30px;
		    padding: 0 20px;
		    border: 1px solid #0064b6;
		    border-radius: 3px;
		    background: #0071ce;
		    color: #fff;
		    font-size: 14px;
		    line-height: 30px;
		    text-align: center;
		    display: inline-block;
		    outline: 0 none;
		    text-decoration: none;
		    margin-top: 40px;
		}
		.show{
			padding: 20px;
		}
		em{
			font-style: normal;
			color: #ff6600
		}
	</style>
</head>
<body>
	<div class="box">
	<h1>模拟密码输入框</h1>
		<label for="ipt">
			<ul>
				<li></li>
				<li></li>
				<li></li>
				<li></li>
				<li></li>
				<li></li>
			</ul>
		</label>
		<input type="tel" id="ipt" maxlength="6">
		<a href="javascript:void(0);">确认</a>
		<div class="show">您输入的密码：<em></em></div>
	</div>
<script>
	$(document).keyup(function (e){
		var numLen = 6;
		var pw = $('input').val();
		var list = $('li');
		$('em').text($('input').val());
		for(var i=0; i<numLen; i++){
			if(pw[i]){
				$(list[i]).text('*');
			}else{
				$(list[i]).text('');
			}
		}
	});
</script>
</body>
</html>
