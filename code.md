LearningMusicP
==============

Projeto do 6º Semestre

/**
*Projeto do 6º Semestre: Experienciar/vivenciar, 2013.
*Nome do projeto: Learning Music.
*Alunos: Bianca Rosa, João Paulo Barros e Hugo Morseli.
*Professores: Bárbara Dariano e Fernando Fabbrini.
*/

// importa as Bibliotecas e chama a classe tambor
import ddf.minim.*;

Minim minim;
AudioPlayer player;
AudioInput input;

bateria mybateria;

// DISPLAY SETUP
void setup() {
  
  mybateria = new bateria();
  minim = new Minim(this);
  
  size(1024, 768);
  background(0);
    // Isso roda o arquivo "" da pasta data 
  player = minim.loadFile("acompanhamento3.mp3");
  input = minim.getLineIn();
}

// RENDER 
void draw() { 
  mybateria.desenhar();
   player.play();
}



/**
*Classe Bateria
*/


class bateria {
  color cor;
  int savedTime;
  int totalTime;
  int r;
  int g;
  int b;
  color tom1;
  int tom2;
  int caixa;
  int surdo;

  //Propriedades da Bateria
  bateria() {
    totalTime = 200;
    r = 47; 
    g = 175;
    b = 150;
    tom1 = 0;
    tom2 = 0;
    caixa = 0;
    surdo = 0;
    savedTime = millis();
  }

  // Desenha a bateria
  public void desenhar() {
    int passedTime = millis() - savedTime;
    strokeWeight(4);

    //caixa:
    noStroke();
    fill(caixa);
    ellipse (210, 540, 360, 330);


    //surdo:
    noStroke();
    fill(surdo);
    ellipse(760, 520, 380, 380);

    //tom1:
    noStroke();
    fill(tom1);
    ellipse (192, 189, 360, 360);

    //tom2:
    //noStroke();
    //  fill(tom2);
    //    ellipse (725, 240, 375, 348);

    //Timming da batida em Millis

    //    // Primeiro ritmo (lento)
    //    if (passedTime > totalTime) {
    //      tom1 = 255;
    //    }
    //
    //    if (passedTime > totalTime + 500) {
    //      tom1 = 0;
    //    }
    //
    //    if (passedTime > totalTime + 1000) {
    //      tom1 = 255;
    //    }
    //
    //    if (passedTime > totalTime + 1500) {
    //      tom1 = 0;
    //      caixa = 255;
    //    }


    //    //Segundo ritmo (lento)
    //    if (passedTime > totalTime + 2000) {
    //      caixa = 0;
    //    }
    //    if (passedTime > totalTime + 2500) {
    //      tom1 = 255;
    //    }
    //    if (passedTime > totalTime + 3000) {
    //      tom1 = 0;
    //    }
    //    if (passedTime > totalTime + 3500) {
    //      tom1 = 255;
    //    }
    //    if (passedTime > totalTime + 4000) {
    //      tom1 = 0;
    //    }
    //    if (passedTime > totalTime + 4500) {
    //      tom1 = 255;
    //      caixa = 255;
    //    }

    //Terceiro ritmo (lento)

    //    if (passedTime > totalTime) {
    //      tom1 = 255;
    //    }
    //    if (passedTime > totalTime) {
    //      tom1 = 0;
    //    }
    //    if (passedTime > totalTime) {
    //      tom1 = 255;
    //    }
    //    if (passedTime > totalTime) {
    //      tom1 = 0;
    //    }
    //    if (passedTime > totalTime) {
    //      caixa = 255;
    //    }
    //    if (passedTime > totalTime) {
    //      caixa = 0;
    //    }
    //    if (passedTime > totalTime) {
    //      tom1 = 255;
    //    }
    //    if (passedTime > totalTime) {
    //      tom1 = 0;
    //    }
    //    if (passedTime > totalTime) {
    //      surdo = 255;
    //    }
    //    if (passedTime > totalTime) {
    //      surdo = 0;
    //    }


    //Terceiro ritmo
    //x1

    if (passedTime > totalTime + 400) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 800) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 1200 ) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 1600) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 1800) {
      caixa = #FFD700;
    }
    if (passedTime > totalTime + 2200) {
      caixa = 0;
    }

    if (passedTime > totalTime + 2600) {
      tom1 = #FF0000;
    }

    if (passedTime > totalTime + 3000 ) {
      tom1 = 0;
    }

    if (passedTime > totalTime + 3400 ) {
      surdo = #0000FF;
    }

    if (passedTime > totalTime + 3800) {
      surdo = 0;
    }

    //x2

    if (passedTime > totalTime + 4200) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 4600) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 5000 ) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 5400) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 5800) {
      caixa = #FFD700;
    }
    if (passedTime > totalTime + 6200) {
      caixa = 0;
    }

    if (passedTime > totalTime + 6400) {
      tom1 = #FF0000;
    }

    if (passedTime > totalTime + 6800) {
      tom1 = 0;
    }

    if (passedTime > totalTime + 7200) {
      surdo = #0000FF;
    }

    if (passedTime > totalTime + 7600) {
      surdo = 0;
    }

    //x3
    if (passedTime > totalTime + 8000) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 8400) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 8800) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 9200) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 9600) {
      caixa = #FFD700;
    }
    if (passedTime > totalTime + 10000) {
      caixa = 0;
    }

    if (passedTime > totalTime + 10400) {
      tom1 = #FF0000;
    }

    if (passedTime > totalTime + 10800) {
      tom1 = 0;
    }

    if (passedTime > totalTime + 11200) {
      surdo = #0000FF;
    }

    if (passedTime > totalTime + 11600) {
      surdo = 0;
    }

    //x4

    if (passedTime > totalTime + 12000) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 12400) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 12800) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 13200) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 13600) {
      caixa = #FFD700;
    }
    if (passedTime > totalTime + 14000) {
      caixa = 0;
    }

    if (passedTime > totalTime + 14400) {
      tom1 = #FF0000;
    }

    if (passedTime > totalTime + 14800) {
      tom1 = 0;
    }

    if (passedTime > totalTime + 15200) {
      surdo = #0000FF;
    }

    if (passedTime > totalTime + 15600) {
      surdo = 0;
    }

    //x5
    if (passedTime > totalTime + 16000) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 16400) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 16800) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 17200) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 17600) {
      caixa = #FFD700;
    }
    if (passedTime > totalTime + 18000) {
      caixa = 0;
    }

    if (passedTime > totalTime + 18400) {
      tom1 = #FF0000;
    }

    if (passedTime > totalTime + 18800) {
      tom1 = 0;
    }

    if (passedTime > totalTime + 19200) {
      surdo = #0000FF;
    }

    if (passedTime > totalTime + 19600) {
      surdo = 0;
    }

    //x6
    if (passedTime > totalTime + 20000) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 20400) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 20800) {
      tom1 = #FF0000;
    }
    if (passedTime > totalTime + 21200) {
      tom1 = 0;
    }
    if (passedTime > totalTime + 21600) {
      caixa = #FFD700;
    }
    if (passedTime > totalTime + 22000) {
      caixa = 0;
    }

    if (passedTime > totalTime + 22600) {
      tom1 = #FF0000;
    }

    if (passedTime > totalTime + 23000) {
      tom1 = 0;
    }

    if (passedTime > totalTime + 23400) {
      surdo = #0000FF;
    }

    if (passedTime > totalTime + 23800) {
      surdo = 0;
    }
  }
}
