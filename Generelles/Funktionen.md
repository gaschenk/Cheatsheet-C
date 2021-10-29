# Funktionen
## Wie deklariert man eine Funktion?
Man deklariert in C Funktionen indem man mit dem Rückgabe-Datentyp beginnt und dann mit einem Leerzeichen und dem Bezeichner (Namen) der Funktion folgt. Daraufhin kann man die Parameter für die Funktion angeben diese werden in den ``()``-Klammern angegeben und benötigen vor dem definieren ihres Namens auch die Definition des Datentyps.

Damit ist die Definition der Funktion auch schon vollständig. Die Implementation wiederum erfolgt aus dem was man vorher beschrieben hat und den ``{}``-Klammern, welche den Inhalt des auszuführenden Codes beinhalten.
### Tl;dr
```c
RückgabeDatentyp FunktionsBezeichner(ParameterDatenTyp ParameterBezeichner,
WeitererParameterDatentyp WeitererParameterBezeichner){
	// Code...
}
```
### Beispiel
```c
int printMySquaredNumber(int value){
	int squaredValue = value * value;
	printf("your value squared is: %d\n",squaredValue)
	return squaredValue;
}
```
### [Weitere Beispiele](Beispiele/Funktionen.md)