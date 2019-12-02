---
title: Method parameters
tags: Ruby
---

Los metodos en Ruby son como las funciones matematicas: metes valores de entrada, hace sus
calculos internos y te devulve una respuesta.
<!--more-->

---

Para hacer esto tenemos que pasarle a los métodos unos argumentos, esto es una lista de variables
despues del nombre del método. Para ser mas exactos cuando definimos estas variables en
el metodo lo llamamos _parámetros_ y cuando pasamos las variables en una llamada al metodo lo
llamamos _argumentos_.

Digamos que le queremos enseñara a un objeto como pasar de metros a pies. Puedes hacerlo enseñandole
como hacer la conversión con un método.

``` ruby
def obj.meters_to_foots(meters)
  meters * 3.28
end
```

El metodo obj.meters_to_foots tiene un parámetro esto significa que solo puede tomar un argumento.
Cuando proveemos un argumento:

``` ruby
 obj.meters_to_foots(4)
```

el resultado es:

``` ruby
# 13.12
# nil
```

Como puedes ver hay una correspondencia entre la sintaxis de la definición del método con sus
parámetros y el mensaje con su argumento, en ambos lados son opcionales por lo que puedes tambien
definirlo y llamarlos de esta manera:

``` ruby
def obj.meters_to_foots meters
```

y así:

``` ruby
 obj.meters_to_foots(4)
```

Pero no son siempre opcionales, sobretodo cuando tenemos varios parametros en un método, por lo
que te recomiendo que los uses siempre, excepto en conveciones y casos en los que son comumente
omitidos.

``` ruby
def hello_world()
 puts 'Hello world'
end
```

En este caso no se usa ningún parámetro, lo mejor es omitirlo:

``` ruby
def hello_world
 puts 'Hello world'
end
```

Al final del método se devuelve por defecto el último valor evaluado. Por ejemplo en el método
que hemos escrito:

``` ruby
def obj.meters_to_foots(meters)
  meters * 3.28
end
```

el último valor evaluado es: meters * 3.28. Por lo que al ser el último valor es el que se devuelve
en su llamada.

``` ruby
puts obj.meters_to_foots(4)

# 13.12
# nil
```

También puedes devolverlo escribiendo explicitamente en el codigo la palabra __return__ pero esto
solo hará falta cuando tengas que devolver un valor en un parte del código concreta o devolver
varios valores. Ya uses return o no un método siempre devolvera un valor.

