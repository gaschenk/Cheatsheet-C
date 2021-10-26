# Integer
Integer ist ein Ganzzahlen Datentyp, welcher in der Regel 32 Bit (4 Bytes) groß ist und auf den meisten Betriebssystem ein signiertes Bit beinhaltet und hat somit Werte von „2.147.483.647“ bis „-2.147.483.648“, diese Werte entsprechen „2^31-1“ und „(-1) * 2^31“.

## Wertebereich
* Signiert: -2.147.483.648 bis 2.147.483.647
* Unsigniert: 0 bis 4294967296

## Deklaration im Code
```c
int main(void){
	// Deklaration Datentyp: int
	int x  = 0; // Zuweisung mit dem Wert 0
	
	// Deklaration unsignierter Datentyp: int
	unsigned int y  = 0; //Zuweisung mit dem Wert 0
}
```