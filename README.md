let palavra;

function setup() {
  createCanvas(900,600);

  palavra = palavraAleatoria();
  
}

function palavraAleatoria() {
  
  let palavras = ["São Paulo", "Tricolor", "Murunbis", "Tricampeão mundial"];
  
  return random(palavras);
}

function inicializaCores() {
  background("blue");
  fill("red");
  textSize(64);
  textAlign(CENTER, CENTER);
}

function palavraParcial(minimo, maximo) {
  let quantidade = map(mouseX, minimo, maximo, 1, palavra.length);
  let parcial = palavra.substring(0, quantidade);
  return parcial;
}

function draw() {
  
  inicializaCores();

  let parcial = palavraParcial(0, width);
    
  text(parcial, 200, 200);
  
}
