<!DOCTYPE html>
<html>
<head>
	<title>CRIADOR DE MEMES</title>
	<link rel="stylesheet" type="text/css" href="estilos.css">
	<link href="https://fonts.googleapis.com/css?family=Luckiest+Guy|Spicy+Rice&display=swap" rel="stylesheet">
</head>
<body>

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
