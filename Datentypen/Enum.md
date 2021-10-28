# Enum
Ein Enum ist eine Möglichkeit für verschiedene Werte von Ganzzahlen Datentypen verschiedene Bezeichner unter einem Begriff zusammen zu fassen, dies ist zum Beispiel sehr nützlich um Zustände eines Programms kompakt und präzise zusammen zu fassen.
## Deklaration im Code
#### ``Ohne Typdefinition``
```c
enum week {
	Mon,
	Tue,
	Wed,
	Thu,
	Fri,
	Sat,
	Sun
} day;
```
In diesem Fall ist ``enum week`` der Datentyp für dieses Enum und ``day`` eine Variable von diesem Datentyp.
#### ``Enum mit Typdefinition``
```c
typedef enum weekday {
	Mon,
	Tue,
	Wed,
	Thu,
	Fri,
	Sat,
	Sun
} week;
```
In diesem Fall ist ``week`` der Datentyp, sowie auch ``enum weekday``, für dieses Enum und es gibt keine Möglichkeit eine Variable wie bei dem Fall ohne Typdefinition direkt zu deklarieren.
#### ``Anonymer Enum mit Typdefinition``
```c
typedef enum {
	Mon,
	Tue,
	Wed,
	Thu,
	Fri,
	Sat,
	Sun
} week;
```
In diesem Fall ist ``week`` der Datentyp für dieses Enum und es gibt keine Möglichkeit eine Variable wie bei dem Fall ohne Typdefinition direkt zu deklarieren.
## Benutzung im Code
#### ``Zustand.h``
```c
#pragma once
#include <stdio.h>
typedef enum {
	Mon,
	Tue,
	Wed,
	Thu,
	Fri,
	Sat,
	Sun
} week;
```
#### ``Zustand.c``
```c
#include "Zustand.h"

int main(void){
	week day = Mon;
	printDayName(day);
}

void printDayName(week day){
	switch(day){
		case Mon:
			printf("Monday!\n");
			break;
		case Tue:
			printf("Tuesday!\n");
			break;
		case Wed:
			printf("Wednesday!\n");
			break;
		case Thu:
			printf("Thursday!\n");
			break;
		case Fri:
			printf("Friday!\n");
			break;
		case Sat:
			printf("Saturday!\n");
			break;
		case Sun:
			printf("Sunday!\n");
			break;
	}
}
```