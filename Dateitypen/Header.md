# Header
Eine Header Datei ist eine Datei, welche in der Regel [[Datentypen/Typdefinition|Typdefinition(en)]] beinhaltet, als auch Funktionsdefinitionen, welche in [[Dateitypen/Source|Source]] Dateien definiert werden, aber auch direkt im Header definiert werden können.
## Headerguards
Headerguards sind dazu da um Linkerprobleme durch mehrfache definierung von Typen, Strukturen, Funktionen zu verhindern, wenn mehrere Dateien ``included`` werden.
### pragma once
Dies ist eine moderne und simple Art und Weise Linker Probleme zu verhindern, jedoch ist es nicht garantiert, dass ältere C/C++ standards diesen auch unterstützen.
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
### alte Headerguardformat
Dies ist die alte Methode um Headerguards zu erstellen um Linker Probleme zu umgehen.
#### ``Student.h``
```c
#ifndef STUDENT_HEADER_GUARD
#define STUDENT_HEADER_GUARD

typedef struct StudentStruktur{
	char[128] Name;
	unsigned char Alter;
	char[128] Fakultät;
	char[128] Studiengang;
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
#### ``Student.h``
```c
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
#import "Student.h"
void printHelloWorld(){
	printf("Hello World!\n");
}
```