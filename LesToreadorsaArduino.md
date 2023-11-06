/*
  Melody FIVE NIGHTS AT FREDDY'S (LES TOREADORS MARCH)
*/

#define NOTE_C4 261.63
#define NOTE_D4 293.66
#define NOTE_E4 329.63
#define NOTE_F4 349.23
#define NOTE_G4 392.00
#define NOTE_A4 440.00
#define NOTE_B4 493.88
#define NOTE_C5 523.25
#define NOTE_D5 587.33
#define NOTE_E5 659.26
#define NOTE_F5 698.46
#define NOTE_G5 783.99
#define NOTE_A5 880.00
#define NOTE_B5 987.77
#define NOTE_GS4 415.30
#define NOTE_AS4 466.16
#define NOTE_DS4 311.13
#define NOTE_AB4 415.30

int melody[] = {
    NOTE_C5, NOTE_D5, NOTE_C5, NOTE_A4,
    NOTE_A4, NOTE_A4, NOTE_G4, NOTE_A4,
    NOTE_B4, NOTE_A4, NOTE_B4, NOTE_A4,
    NOTE_C5, NOTE_A4, NOTE_F4, NOTE_D4,
    NOTE_G4, NOTE_C4
};

int noteDurations[] = {
    4, 8, 8, 4,
    4, 8, 8, 8,
    8, 2, 4, 8,
    8, 2, 4, 8,
    8, 2
};

void setup() {
  
  for (int thisNote = 0; thisNote < 19; thisNote++) {
    /* 
       This for loop is intended to play each note in sequence with a
       specified delay. If you want to add more notes, you should
       increase the limit of the FOR loop.
    */  
    int noteDuration = 1000 / noteDurations[thisNote];
    tone(8, melody[thisNote], noteDuration);
    int pauseBetweenNotes = noteDuration * 1.30;
    delay(pauseBetweenNotes);
    noTone(8);
  }
  
  delay(500); 
}

void loop() {
}
