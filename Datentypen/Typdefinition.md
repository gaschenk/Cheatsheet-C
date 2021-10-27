---
title: "Typdefinition"
---
# Typdefinition "typedef"
Eine Typdefinition ist eine Änderung beziehungsweise eine Möglichkeit einem Datentyp oder Zusammenschluss an Datentypen einen weiteren Namen zu geben.
## Deklaration im Code
Das folgende Beispiel zeigt wie man ein Struct ``StudentStruktur`` eine weitere Namensdefinition geben kann, in diesem Falle ``Student``.
```c
typedef struct StudentStruktur{
	char Name[128];
	unsigned char Alter;
	char Fakultät[128];
	char Studiengang[128];
	unsigned char Semester;
}Student;
```

#### ``Alternative``
```c
typedef struct{
	char Name[128];
	unsigned char Alter;
	char Fakultät[128];
	char Studiengang[128];
	unsigned char Semester;
}Student;
```
## Beispiel Benutzung
Wie man im Teil ["Deklaration im Code"](#Deklaration%20im%20Code) den Struct ``StudentStruktur`` definiert hat, kann man ihn nun mit ``Student`` verwenden anstatt mit ``struct StudentStruktur``.
```c
int main(void){
	Student studentA;
	studentA->Name = "Hans Müller";
	studentA->Alter = 19;
	studentA->Fakultät = "Informatik";
	studentA->Studiengang = "Medien- und Kommunikationsinformatik";
	studentA->Semester = 3;
}
```