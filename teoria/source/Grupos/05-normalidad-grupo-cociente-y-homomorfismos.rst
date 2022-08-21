Normalidad, Grupo Cociente y Homomorfismos
===========================================

Estudiaremos aquellos subgrupos :math:`N` de un grupo :math:`G`` tales que
coincidan con la congruencia módulo :math:`N` a izquierda y a derecha.
Tales subgrupos juegan un papel importante en la determinación
tanto de la estructura del grupo :math:`G` como de la naturaleza de los
homomorfismos con dominio :math:`G`.

Teorema
-------

Si :math:`N` es un subgrupo de un grupo :math:`G`, entonces las siguientes
condiciones son equivalentes:

#. La congruencia módulo :math:`N` a izquierda y a derecha coincide (esto es
   que, define la misma relación equivelencia :math:`G`); 

#. Toda coclase izquierda de :math:`N` en :math:`G` es una coclase derecha
   de :math:`N` en :math:`G`; 

#. :math:`aN=Na` para todo :math:`a \in G`; 

#. Para todo :math:`a \in G`, :math:`aNa^{-1} \subset N`,
   donde :math:`aNa^{-1}=\{ ana^{-1} | n \in N \}`;

#. Para todo :math:`a \in G`, :math:`aNa^{-1}=N`.

**Demostración** 

- :math:`1 \Longrightarrow 3`: Dos relaciones de equivalencias :math:`R` y
  :math:`S` son identicas si y solo si las clases de equivalencias de cada
  elemento bajo :math:`R` es igual a la clase de equivalencia bajo :math:`S`.
  En este caso, la clases de equivalencias son los cosets izquierdos y
  derechos respectivamente de :math:`N`. 

- :math:`2 \Longrightarrow 3`: Si :math:`aN=Na` para algún :math:`b \in G`,
  entonces :math:`a \in Nb \cap Na`, lo que implica que :math:`Nb=Na` ya que
  dos cosets derechos son disjuntos de a dos o son iguales.

- :math:`3 \Longrightarrow 4` es trivial.

- :math:`4 \Longrightarrow 5` Si tenemos :math:`aNa^{-1} \subset N`. Ya que
  :math:`4` también se mantiene para :math:`a^{-1}\in G`, :math:`a^{-1}Na \subset N`.
  Por lo tanto para cada :math:`n \in N`, :math:`n = a(a^{-1}na)a^{-1} \subset aNa^{-1}` y
  :math:`N \subset aNa^{-1}`.

- :math:`5 \Longrightarrow 2` es inmediato.

Definición
-----------

Un subgrupo :math:`N` de un grupo :math:`G` que satisface las
condiciones equivalentes del Teorema 5.1 es llamado normal en :math:`G` (o
un subgrupo normal de :math:`G`).

Denotamos :math:`N \triangleleft G` si :math:`N` es normal en :math:`G`.

En vista del Teorema 5.1 podemos omitir los subíndices ":math:`r`" e
":math:`l`" al denotar  módulo de congruencia un subgrupo normal. 

