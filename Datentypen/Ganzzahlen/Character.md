# Character
Character ist ein spezieller Datentyp, jedoch grundsätzlich eine Ganzzahl. Warum speziell, weil Character wie sein Name sagt einen "Charakter" ausdrücken kann beziehungsweise einem zugewiesen bekommen kann, aufgrund dessen wird dieser Datentyp auch oft in der Form eines Arrays als String verwendet.

## Wertebereich
* Signiert: -128 bis 127
* Unsigniert: 0 bis 255

## Deklaration im Code
```c
int main(void){
	// Deklaration Datentyp: char 
	char x  = 0; // Zuweisung mit dem Wert 0
	// Deklaration usignierter Datentyp: char 
	unsigned char y  = 0; // Zuweisung mit dem Wert 0
	// Deklaration Datentyp: char
	char z  = 'A'; // Zuweisung mit dem Wert 'A'
}
```