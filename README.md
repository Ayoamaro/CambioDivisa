# CambioDivisa

Implementar una aplicación en JavaFX que permita calcular los cambios entre distintas divisas: Euro, Dolar, Yen, Libra esterlina, ...

El aspecto de la interfaz será el siguiente:

![](https://github.com/Ayoamaro/CambioDivisa/blob/main/docs/images/Cambio%20divisa.png?raw=true)

Debemos hacer uso de la clase "Divisa", que nos ayudará a realizar las conversiones entre divisas. Un ejemplo de su uso:

```
Divisa euro = new Divisa("Euro", 1.0);
Divisa libra = new Divisa("Libra", 0.8873);
Divisa dolar = new Divisa("Dolar", 1.2007);
Divisa yen = new Divisa("Yen", 133.59);
Divisa origen = yen;
Divisa destino = dolar; 
Double cantidad = 2000.0;    
System.out.println(destino.fromEuro(origen.toEuro(cantidad))); // convierte 2000 yenes en dólares
```

Cuando se pulse el botón "Cambiar" se deberá realizar la conversión de la cantidad especificada en el cuadro de texto superior y mostrar el resultado en el cuadro de texto de debajo. Este último deberá ser "no editable".

Deberá controlarse si la cantidad especificada no es válida (campo vacío, caracteres no numéricos, ...), y avisar al usuario con una "**[Alert](https://docs.oracle.com/javase/8/javafx/api/javafx/scene/control/Alert.html)**".
