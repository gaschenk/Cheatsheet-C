---
title: "Struct"
---
# Struct
Ein Struct ist ein zusammenschluss von Daten, um diese Werte unter einer Bezeichnung zusammen zu fassen. Das hat den Vorteil von einer besseren Übersicht.
## Deklaration im Code
Die Deklaration und Benutzung eines Structs findet mit ``struct NameDerStruktur`` und folgt innerhalb seines Scopes mit den Definitionen von seinen Memberwerten/Memberfields.
```c
struct Student{
	char[128] Name;
	unsigned char Alter;
	char[128] Fakultät;
	char[128] Studiengang;
	unsigned char Semester;
}
```
## Zugriff auf Memberwerte
Der Zugriff auf Memberwerte findet mit dem Operatoren ``->`` statt.
```c
int main(void){
	struct Student studentA;
	studentA->Name = "Hans Müller";
	studentA->Alter = 19;
	studentA->Fakultät = "Informatik";
	studentA->Studiengang = "Medien- und Kommunikationsinformatik";
	studentA->Semester = 3;
}
```