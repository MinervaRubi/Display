const int btnJ = 2; 
const int btnK = 3; 
const int btnL = 4; 
const int btnM = 5; 

const int ledA = 6;
const int ledB = 7;
const int ledC = 8;
const int ledD = 9;
const int ledE = 10;
const int ledF = 11;
const int ledG = 12;

const int pinesLed[] = {ledA, ledB, ledC, ledD, ledE, ledF, ledG};
// hacer un arreglo para definir los pines 
const bool numeros[16][7] = {
  {HIGH, HIGH, HIGH, HIGH, HIGH, HIGH, LOW},   // 0
  {LOW, HIGH, HIGH, LOW, LOW, LOW, LOW},       // 1
  {HIGH, HIGH, LOW, HIGH, HIGH, LOW, HIGH},    // 2
  {HIGH, HIGH, HIGH, HIGH, LOW, LOW, HIGH},    // 3
  {LOW, HIGH, HIGH, LOW, LOW, HIGH, HIGH},     // 4
  {HIGH, LOW, HIGH, HIGH, LOW, HIGH, HIGH},    // 5
  {HIGH, LOW, HIGH, HIGH, HIGH, HIGH, HIGH},   // 6
  {HIGH, HIGH, HIGH, LOW, LOW, LOW, LOW},      // 7
  {HIGH, HIGH, HIGH, HIGH, HIGH, HIGH, HIGH},  // 8
  {HIGH, HIGH, HIGH, HIGH, LOW, HIGH, HIGH},   // 9
  {HIGH, HIGH, HIGH, LOW, HIGH, HIGH, HIGH},    //A
  {LOW, LOW, HIGH, HIGH, HIGH, HIGH, HIGH},    //b
  {LOW, LOW, LOW, HIGH, HIGH, LOW, HIGH},      //C
  {LOW, HIGH, HIGH, HIGH, HIGH, LOW, HIGH},    //d
  {HIGH, LOW, LOW, HIGH, HIGH, HIGH, HIGH},    //E
  {HIGH, LOW, LOW, LOW, HIGH, HIGH, HIGH}      //F
  };

void setup() {
  pinMode(btnJ, INPUT);
  pinMode(btnK, INPUT);
  pinMode(btnL, INPUT);
  pinMode(btnM, INPUT);
  //darme cuenta que votones estan presionados para poder dar la salida 
  for (int i = 0; i < 7; i++) {
    pinMode(pinesLed[i], OUTPUT);
  }

  pruebaDisplay(); 
}

void loop() {
  //le que estado tienen los botones 
  int estadoJ = digitalRead(btnJ);
  int estadoK = digitalRead(btnK);
  int estadoL = digitalRead(btnL);
  int estadoM = digitalRead(btnM);

  // ver como estan presionados los botones y las salidas que debe dar 
  if (estadoJ == LOW && estadoK == LOW && estadoL == LOW && estadoM == LOW) {
    mostrarNumero(0);
  }
  else if (estadoJ == LOW && estadoK == LOW && estadoL == LOW && estadoM == HIGH) {
    mostrarNumero(1);
  }
  else if (estadoJ == LOW && estadoK == LOW && estadoL == HIGH && estadoM == LOW) {
    mostrarNumero(2);
  }
  else if (estadoJ == LOW && estadoK == LOW && estadoL == HIGH && estadoM == HIGH) {
    mostrarNumero(3);
  }
  else if (estadoJ == LOW && estadoK == HIGH && estadoL == LOW && estadoM == LOW) {
    mostrarNumero(4);
  }
  else if (estadoJ == LOW && estadoK == HIGH && estadoL == LOW && estadoM == HIGH) {
    mostrarNumero(5);
  }
  else if (estadoJ == LOW && estadoK == HIGH && estadoL == HIGH && estadoM == LOW) {
    mostrarNumero(6);
  }
  else if (estadoJ == LOW && estadoK == HIGH && estadoL == HIGH && estadoM == HIGH) {
    mostrarNumero(7);
  }
  else if (estadoJ == HIGH && estadoK == LOW && estadoL == LOW && estadoM == LOW) {
    mostrarNumero(8);
  }
  else if (estadoJ == HIGH && estadoK == LOW && estadoL == LOW && estadoM == HIGH) {
    mostrarNumero(9);
  }
  else if (estadoJ == HIGH && estadoK == LOW && estadoL == HIGH && estadoM == LOW) {
    mostrarNumero(10);
  }
  else if (estadoJ == HIGH && estadoK == LOW && estadoL == HIGH && estadoM == HIGH) {
    mostrarNumero(11);
  }
  else if (estadoJ == HIGH && estadoK == HIGH && estadoL == LOW && estadoM == LOW) {
    mostrarNumero(12);
  }
  else if (estadoJ == HIGH && estadoK == HIGH && estadoL == LOW && estadoM == HIGH) {
    mostrarNumero(13);
  }
  else if (estadoJ == HIGH && estadoK == HIGH && estadoL == HIGH && estadoM == LOW) {
    mostrarNumero(14);
  }
  else if (estadoJ == HIGH && estadoK == HIGH && estadoL == HIGH && estadoM == HIGH) {
    mostrarNumero(15);
  }
  else {
    mostrarNumero(0); 
  }

  delay(300); 
}

// Para mostrar el numero en el display 
void mostrarNumero(int numero) {
  if (numero >= 0 && numero < 16) {
    for (int i = 0; i < 7; i++) {
      digitalWrite(pinesLed[i], numeros[numero][i]);
    }
  }
}
//bucle para ver los numeros en el display 
void pruebaDisplay() {
  for (int i = 0; i < 7; i++) {
    digitalWrite(pinesLed[i], HIGH);
    delay(200);
    digitalWrite(pinesLed[i], LOW);
  }

  for (int i = 0; i <= 9; i++) {
    mostrarNumero(i);
    delay(300);
  }
}
