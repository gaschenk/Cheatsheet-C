---
title: "Pointer & Referenzen"
---
# Pointer & Referenzen
Man kann Pointer und Referenzen gleich setzen, da beide die Speicheraddresse eines Speicherbereichs beinhalten.
## Deklaration im Code
### Pointer & Referenzierung
```c
int main(void){
	// Deklaration Datentyp: char pointer
	char* pointer = NULL; // Zuweisung mit der Speicheraddresse 0
	// Deklaration Datentyp: int
	int x = 5; // Zuweisung mit dem Wert 5
	// Deklaration Datentyp: int pointer
	int* pointerToX = &x; // Zuweisung mit der Referenz von der Variable "x"
}
```
### Pointer Dereferenzierung
Dereferenzierung bedeutet den Wert von einer Speicheraddresse zu erhalten, in anderen Worten den Wert aus dem Speicherbereich auszulesen.
```c
int main(void){
	// Deklaration Datentyp: int
	int x = 5; // Zuweisung mit dem Wert 5
	// Deklaration Datentyp: int pointer
	int* pointerToX = &x; // Zuweisung mit der Referenz von der Variable "x"
	// Deklaration Datentyp: int
	int y = *pointerToX; // Zuweisung mit der Dereferenzierung des Pointers
}
```