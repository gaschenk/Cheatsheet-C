---
title: Union
---
# Union
Ein Union ist ein Zusammenschluss von verschiedenen Datentypen unter einem Namen, jedoch lediglich, um aus diesem Bezeichner mit verschiedenen Datentypen Informationen zu erhalten.

Ein Union wird immer die Menge an Speicher verwenden von dem größten Datentyp.
Wichtig zu merken ist, dass es nicht wie bei einem Struct unterschiedliche Speicherbereiche sind, sondern immer der gleiche, das heißt schreibt man in den einen "Member" rein werden auch die anderen Beeinflusst, lediglich der Datentyp mit dem zu gegriffen wird ist anders.
## Deklaration im Code
#### ``Simples Beispiel``
```c
union IntBytes{
	int ValueOfAnInteger;
	char bytes[sizeof(int)];
}
```
Dies ist ein Union, welches entweder als Integer ausgelesen werden kann oder als Array von characters, mit der größe eines Integers.
#### ``Komplizierteres Beispiel``
```c
union IntBytes{
	int ValueOfAnInteger;
	char string[20];
}
```
Dies wiederum ist ein Union, welches entweder als Integer ausgelesen werden kann oder als ein Array von Characters mit der Länge 20.
Weil in diesem Fall der größte Datentyp das Array von Characters ist, wird das Union die 20 Bytes verwenden die das Array benötigt, unabhängig davon wie groß das Integer ist.