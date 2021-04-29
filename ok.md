void setup ()

  {
  Serial.begin (15000);
  Serial.println ();
}

void loop ()
{  
 
 int InputPin1 = A0; 
 int InputPin2 = A1; 
 int InputPin3 = A2;
 
 int pinx = A3;
 int piny = A4;
 int pinz = A5;  
  
 int randNumber; 

     
  
     int A = analogRead (InputPin1);
     Serial.print (" State 1 = ");
     Serial.print(A);
     int B = analogRead (InputPin2);
     Serial.print (" State 2 = ");
     Serial.print(B);
     int C = analogRead (InputPin3);
     Serial.print (" State 3 = ");
     Serial.print(C);
     Serial.print( " | " );
    int x = analogRead(pinx); 

    int y = analogRead(piny);
      
    int z = analogRead(pinz);
  
  randNumber = random(200, 250);
  Serial.print(randNumber);

  
 if ( (A == 974) && (B == 974) && (C  == 974) )
   {
     Serial.print (" SA ");
     tone(8, 263);
     
     
   }  
 else if ( (A == 974) && (B == 974) && (C  == 54) )
   {
     Serial.print (" RE ");
     tone(8, 294);
    
       
    
   }  
 else if ( (A == 974 ) && (B == 54) && (C  == 974) )
   {
     Serial.print (" GA ");
    
     tone(8, 330);
    
       
    
   }  
 else if ( (A == 974) && (B == 54 ) && (C  == 54) )
   {
     Serial.print (" MA ");
    
     tone(8, 349);
   
    
     
   }  
 else if ( (A == 54) && (B == 974) && (C  == 974) )
   {
     Serial.print (" PA ");
     tone(8, 392);
   
     
   }  
 else if ( (A == 54) && (B == 974) && (C  == 54) )
   {
     Serial.print (" DHA ");
     tone(8, 440);
      
   
     
   }  
 else if ( (A == 54) && (B == 54) && (C  == 974) )
   {
     Serial.print (" NI ");
     tone(8, 494);
     
    
   }  
 else if ( (A == 54 ) && (B == 54) && (C  == 54) )
   {
     Serial.print (" SNA ");
     tone(8, 515);
   }
  
   else if ( x == 0)
   {
     tone(8, randNumber, 200);
     delay(200); 
   }
     
 else if ( y != 0 )
   {
     
     tone(12, abs(y));
     
   }
 else  if ( z != 0 )
   {
     
     tone(7, abs(z));
     
   }
else 
   {
        noTone(8); 
   }
    
Serial.print(" | x acc = ");   
Serial.print(x-322);


Serial.print("|y acc = ");   
Serial.print(y-320);


Serial.print("|z acc = ");   
Serial.print(z-263);

  
 
  
  Serial.println ();
  ;
  }
