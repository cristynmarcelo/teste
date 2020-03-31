<!DOCTYPE html>
<html>
<head>
	<title>CRIADOR DE MEMES</title>
	<link href="https://fonts.googleapis.com/css?family=Luckiest+Guy|Spicy+Rice&display=swap" rel="stylesheet">
</head>
<body>

	<style type="text/css">
		
		*{
	padding: 0;
	margin: 0;
	box-sizing: border-box;
}

.center{
	max-width: 1280px;
	width: 100%;
	margin: 0 auto;}

.head{
	background-color: black;
	width: 100%;
	height: 100px;
	text-align: center;
}

.head h2{
	padding-top: 16px;
	font-size: 50px;
	color: orange;
	letter-spacing: 8px;
	font-family: 'Luckiest Guy', cursive;
}

input[type='file'] {
  display: none
}

label {
	background-color: orange;
	font-family: cursive;
	font-size: 20px;
	font-weight: bold;
 	border-radius: 5px;
	color: black;
	cursor: pointer;
	padding: 20px 20px;
	box-shadow:0 5px 0 #cc7e00;
}

label:active{
	position: relative;
	top: 5px;
	box-shadow:none;}

.fundo-painel{
	border-radius: 15px;
	margin-left: calc( 50% + -280px);
	text-align: center;
	margin-top: 20px;
	float: left;
	position: static;
	width: 560px;
	height: 700px;
	background-color: #A538C5;
	
}


.bg{
	width: 100%;
	height: 900px;
	background-image: url('emojis.jpg');
}

textarea{
	padding: 12px 10px 8px 10px;
	max-width: 520px;
	min-width: 520px;
	max-height: 180px;
	min-height: 40px;
	font-size: 25px;
	margin-left: calc( 50% + -280px);
	text-align: left;
	margin-top: 20px;
	position: static;
	width: 540px;
	height: 90px;
	border: 4px solid black;	
}

.icones{
	align-items: center;
	text-align: center;
	margin: 5px;

}
.icones img{
	padding-bottom: 7px;
	align-items: center;
	text-align: center;
	margin: 15px;
	width: 75px;
	height: 75px;
}

.propaganda{
	border-radius: 15px;
	margin-left: calc( 50% + -280px);
	margin-top: -35px;
	width: 560px;
	height: 150px;
	background-color: #A538C5;
}

img{
	margin-top: -6px;
	margin-bottom: 30px;
	margin-left: calc( 50% + -280px);
	border: 4px solid black;	
	width: 520px;
	height: 400px;
}

@media screen and (max-width: 600px){
	.head{
		height: auto;
		width: 100%;
		padding:15px 0;
		text-align: center;
	}
	.head h2{
		padding-top: 10px;
		font-size: 38px;
	}

	.fundo-painel{
	border-radius: 15px;
	margin-left: calc( 50% + -220px);
	text-align: center;
	margin-top: 10px;
	float: left;
	position: static;
	width: 440px;
	height: 800px;
	}

	textarea{
	padding: 12px 10px 8px 10px;
	max-width: 420px;
	min-width: 420px;
	max-height: 180px;
	min-height: 40px;
	font-size: 25px;
	margin-left: calc( 50% + -220px);
	text-align: left;
	margin-top: 10px;
	position: static;
	width: 420px;
	height: 90px;
	border: 4px solid black;	
}

img{
	margin-top: -8px;
	margin-bottom: 30px;
	margin-left: calc( 50% + -220px);
	border: 4px solid black;	
	width: 420px;
	height: 340px;
}
.propaganda{
	margin-left: calc( 50% + -220px);
	margin-top: -20px;
	width: 420px;
	height: 140px;
	background-color: #A538C5;}
}

</style>

	<div class="head">
		<div class="logo">
			<h2>CRIADOR DE MEMES</h2>
		</div>
	</div>

	<div class="fundo-painel">
		<textarea cols="30" rows="5" placeholder="Escreva seu MEME aqui..."></textarea>
		<img src="cenario.png">
		<label for="imagem">Escolha uma imagem do PC &#187;</label>
		<input type="file" name="imagem" id="imagem" onchange="previewImagem()">
		<div class="propaganda"></div>
	</div>
		
	<div class="bg"></div>

	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>

	<script>
			function previewImagem(){
				var imagem = document.querySelector('input[name=imagem]').files[0];
				var preview = document.querySelector('img');
				
				var reader = new FileReader();
				
				reader.onloadend = function () {
					preview.src = reader.result;
				}
				
				if(imagem){
					reader.readAsDataURL(imagem);
				}else{
					preview.src = "cenario.png";
				}
			}
		</script>
				
</body>
</html>
