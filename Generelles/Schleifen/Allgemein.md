---
title: Allgemeines zu Schleifen
---
# Allgemeines zu Schleifen
## Wie breche ich verfrüht aus einer Schleife aus?
Das ausbrechen aus einer Schleife ohne die Bedingungen zu erfüllen, lässt sich in C über dem Keyword ``break`` ermöglichen.

```c
int main(void){
	// Diese Schleife ist immer wahr, sie wird also
	// immer weiterlaufen.
	while(1){
		// Jedoch können wir einfach mit "break" 
		// aus der Schleife ausbrechen.
		break;
	}
}
```
## Wie überspringe ich eine Iteration einer Schleife?
Mit dem Keyword ``continue`` können wir Iterationen einer Schleife überspringen. Dies ist sehr nützlich wenn man eine  komplexe Logik hat und diese für gewisse Bedingungen nicht durch laufen muss.
```c
int main(void){
	for(int i = 0; i < 5; i++){
		if(i < 3)
			continue;
		printf("%d", i);
	}
}
```
### ``Ausgabe``
> 3
> 4