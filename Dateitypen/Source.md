---
title: "Source File"
---
# Source
Eine Source Datei dient zur Implementierung von definierten Funktionen, beziehungsweise der allgemeinen Implementation von Software Logik.
## Beispiel
Dies ist ein Beispiel, das aufzeigt wie man eine Funktion, welche in einem [Header](Dateitypen/Header.md) definiert worden ist, implementiert.
#### ``Student.h``
```c
#pragma once

typedef struct{
	char Name[128];
	unsigned char Alter;
	char Fakultät[128];
	char Studiengang[128];
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