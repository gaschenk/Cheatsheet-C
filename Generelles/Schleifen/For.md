---
title: For Schleife
---
# For Schleife
## Wie Deklariert man eine For-Schleife?
Eine For-Schleife deklariert man, indem das Keyword ``for`` verwendet wird, gefolgt mit den ``()``-Klammern. In den Klammern kann man eine Variable für die Iteration definieren, sowie die Bedingung für das endgültige Abschließen der Schleife als auch die Schrittweite/Schrittart. Hier bei muss man darauf achten, dass zwischen der Iterationsvariable, Bedingung und der Schrittweite ein Semicolon muss.
```c
int main(void){
	// Diese Schleife wird 10 mal durchlaufen für 0 bis 9
	for(int i = 0; i < 10; i++){
		printf("%d",i);
	}
}
```
### ``Ausgabe``
> 0123456789
### Tl;dr
```c
	for(IterationsVariablenDatentyp IterationsVariablenBezeichner;
	Bedingung;Schrittartt)
```