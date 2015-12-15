# LCD-Keypad-Shield-v1.1
#include <LiquidCrystal.h>

LiquidCrystal lcd(8, 9, 4, 5, 6, 7); //pinagem LCD no Arduino Mega
#define btnRIGHT  0 
#define btnUP     1 
#define btnDOWN   2 
#define btnLEFT   3 
#define btnSELECT 4 
#define btnNONE   5 
int sel;
int tecla_valor;
boolean rele_porta01;
boolean rele_porta02;
boolean rele_porta03;
boolean rele_porta04;
boolean rele_porta05;
boolean rele_porta06;
boolean rele_porta07;
boolean rele_porta08;


void setup() {  
 lcd.begin(16, 2);
 sel = 1;
 rele_porta01=0;
 rele_porta02=0;
 rele_porta03=0;  
 rele_porta04=0;
 rele_porta05=0;
 rele_porta06=0;
 rele_porta07=0;
 rele_porta08=0;
 pinMode(22, OUTPUT);
 pinMode(23, OUTPUT);
 pinMode(24, OUTPUT);
 pinMode(25, OUTPUT);
 pinMode(26, OUTPUT);
 pinMode(27, OUTPUT);
 pinMode(28, OUTPUT);
 pinMode(29, OUTPUT);
 pinMode(30, OUTPUT);
 
 //Inicia Apresentação do Projeto
 lcd.print(" Sequencer");
 delay(3000);
 lcd.clear();
 lcd.print("Desenvolvido por");
 lcd.setCursor(0,1);
 lcd.print("  Rui ");
 delay(5000);
}  
void loop(){
 int tecla_valor = analogRead(0);
 
 if (tecla_valor == 50)
 {
    
 }
 if ((tecla_valor >= 120) && (tecla_valor <= 146))
 {
    
 }
 if ((tecla_valor >= 300) && (tecla_valor <= 350))
 {
   
 }
 if ((tecla_valor >= 500) && (tecla_valor <= 530))
 {
    
 }
 if ((tecla_valor >= 700) && (tecla_valor <= 790))
 {
   
 }
 delay(250);
 if (btnRIGHT == 1)
 {
    sel++;
 }
 if (btnLEFT == 1)
 {
    sel--;
 }
 if (sel <= 0)
 {
    sel=1;
 }  
 if (sel==8)
 {
   sel=1;
 }
 if (sel<=1){
   lcd.clear();
   lcd.setCursor(0,0);
   lcd.print("     Porta01 >> ");
   lcd.setCursor(0,1);
   lcd.print("Estado:");
   if (rele_porta01==1)
      lcd.print("Ligado");
   else
      lcd.print("Desligado");
   if (btnSELECT == 1){
      rele_porta01 = !rele_porta01;
      delay(100);
   }        
 }
 if (sel==2){
    lcd.clear();
    lcd.setCursor(0,0);
    lcd.print("     Porta02 >> ");
    lcd.setCursor(0,1);
    lcd.print("Estado:");
    if (rele_porta02==1)
       lcd.print("Ligado");
    else
       lcd.print("Desligado");
    if (btnSELECT == 1){
        rele_porta02 = !rele_porta02;
        delay(100);
     }        
}
 if (sel==3){
    lcd.clear();
    lcd.setCursor(0,0);
    lcd.print("     Porta03 >> ");
    lcd.setCursor(0,1);
    lcd.print("Estado:");
    if (rele_porta03==1)
       lcd.print("Ligado");
    else
       lcd.print("Desligado");
    if (btnSELECT == 1){
        rele_porta03 = !rele_porta03;
        delay(100);
     }
 }
 if (sel==4){
    lcd.clear();
    lcd.setCursor(0,0);
    lcd.print("     Porta04 >> ");
    lcd.setCursor(0,1);
    lcd.print("Estado:");
    if (rele_porta04==1)
       lcd.print("Ligado");
    else
       lcd.print("Desligado");
     if (btnSELECT == 1){
        rele_porta04 = !rele_porta04;
        delay(100);
     }
 }
 if (sel==5){
    lcd.clear();
    lcd.setCursor(0,0);
    lcd.print("     Porta05 >> ");
    lcd.setCursor(0,1);
    lcd.print("Estado:");
    if (rele_porta05==1)
       lcd.print("Ligado");
    else
       lcd.print("Desligado");
    if (btnSELECT == 1){
        rele_porta05 = !rele_porta05;
        delay(100);
     }
 }

  if (sel==6){
    lcd.clear();
    lcd.setCursor(0,0);
    lcd.print("     Porta06 >> ");
    lcd.setCursor(0,1);
    lcd.print("Estado:");
    if (rele_porta06==1)
       lcd.print("Ligado");
    else
       lcd.print("Desligado");
    if (btnSELECT == 1){
        rele_porta06 = !rele_porta06;
        delay(100);
     }
   }

    if (sel==7){
    lcd.clear();
    lcd.setCursor(0,0);
    lcd.print("     Porta07 >> ");
    lcd.setCursor(0,1);
    lcd.print("Estado:");
    if (rele_porta07==1)
       lcd.print("Ligado");
    else
       lcd.print("Desligado");
    if (btnSELECT == 1){
        rele_porta07 = !rele_porta07;
        delay(100);
     }
 }

  if (sel==8){
    lcd.clear();
    lcd.setCursor(0,0);
    lcd.print("     Porta08 >> ");
    lcd.setCursor(0,1);
    lcd.print("Estado:");
    if (rele_porta06==1)
       lcd.print("Ligado");
    else
       lcd.print("Desligado");
    if (btnSELECT == 1){
        rele_porta08 = !rele_porta08;
        delay(100);
     }
   }
 if (rele_porta01==1){
    digitalWrite(22, HIGH);
 }
 if (rele_porta01==0){
    digitalWrite(22, LOW);
 }
 if (rele_porta02==1){
    digitalWrite(23, HIGH);
 }
 if (rele_porta02==0){
    digitalWrite(23, LOW);
 }
 if (rele_porta03==1){
    digitalWrite(24, HIGH);
 }
 if (rele_porta03==0){
    digitalWrite(24, LOW);
 }
 if (rele_porta04==1){
    digitalWrite(25, HIGH);
 }
 if (rele_porta04==0){
    digitalWrite(25, LOW);
 }
 if (rele_porta05==1){
    digitalWrite(26, HIGH);
 }
 if (rele_porta05==0){
    digitalWrite(26, LOW);
 }
 if (rele_porta06==1){
    digitalWrite(27, HIGH);
 }
 if (rele_porta06==0){
    digitalWrite(28, LOW);
    }
 if (rele_porta07==1){
    digitalWrite(29, HIGH);
 }
 if (rele_porta07==0){
    digitalWrite(29, LOW);
    }
 if (rele_porta08==1){
    digitalWrite(30, HIGH);
 }
 if (rele_porta08==0){
    digitalWrite(30, LOW);
 }
}

