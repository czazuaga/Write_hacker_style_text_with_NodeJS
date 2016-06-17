fs = require('fs');

var textoObtenido;
var contador = 0;

try{
	textoObtenido = fs.readFileSync('./archivoDeTexto.txt','utf8');
}catch(err){
	console.log('ERROR: '+err);
}

setInterval(function(){
	contador++;
	var textoTroceado = textoObtenido.substring(contador-1,contador);
	process.stdout.write(textoTroceado,'utf8');
},200);


