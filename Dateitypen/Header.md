---
title: "Header File"
---
# Header
Eine Header Datei ist eine Datei, welche in der Regel [Typdefinitionen](Datentypen/Typdefinition.md) beinhaltet, als auch Funktionsdefinitionen, welche in [Source](Dateitypen/Source.md) Dateien definiert werden, aber auch direkt im Header definiert werden können.
## Headerguards
Headerguards sind dazu da um Linkerprobleme durch mehrfache definierung von Typen, Strukturen, Funktionen zu verhindern, wenn mehrere Dateien ``included`` werden.
### pragma once
Dies ist eine moderne und simple Art und Weise Linker Probleme zu verhindern, jedoch ist es nicht garantiert, dass ältere C/C++ standards diesen auch unterstützen.
Es wird jedoch von den meisten Compilern unterstützt und ist z.B.: seit einer Weile in dem C++ Standard enthalten.
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
### alte Headerguardformat
Dies ist die alte Methode um Headerguards zu erstellen um Linker Probleme zu umgehen.
#### ``Student.h``
```c
#ifndef STUDENT_HEADER_GUARD
#define STUDENT_HEADER_GUARD

typedef struct{
	char Name[128];
	unsigned char Alter;
	char Fakultät[128];
	char Studiengang[128];
	unsigned char Semester;
}Student;

void printHelloWorld();
#endif
```
#### ``Student.c``
```c
#include "Student.h"
void printHelloWorld(){
	printf("Hello World!\n");
}
```
### \#import
Obwohl man ``#import`` verwenden kann, ist es nicht empfohlen, da es unklare Versprechungen macht und nicht unbedingt von jedem Compiler unterstützt wird.
Ebenso ist es nicht part von dem C Standard, Deprecated und gehört eigentlich zu Objective-C, dies ist Apple's alternative zu C++ und ist im Vergleich zu C ein deutlicher Unterschied.

> Es ist Objective-C nicht C, das ist ein deutlicher unterschied.
#### ``Student.h``
```c
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
#import "Student.h"
void printHelloWorld(){
	printf("Hello World!\n");
}
```