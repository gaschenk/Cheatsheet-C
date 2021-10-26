# Source
Eine Source Datei dient zur Implementierung von definierten Funktionen, beziehungsweise der allgemeinen Implementation von Software Logik.
## Beispiel
Dies ist ein Beispiel, das aufzeigt wie man eine Funktion, welche in einem [Header](Dateitypen/Header.md) definiert worden ist, implementiert.
#### ``Student.h``
```c
#pragma once

typedef struct StudentStruktur{
	char[128] Name;
	unsigned char Alter;
	char[128] Fakultät;
	char[128] Studiengang;
	unsigned char Semester;
}Student;

void printHelloWorld();
```
#### ``Student.c``
```c
#include "Student.h"
void printHelloWorld(){
	printf("Hello World!\n");
}
```