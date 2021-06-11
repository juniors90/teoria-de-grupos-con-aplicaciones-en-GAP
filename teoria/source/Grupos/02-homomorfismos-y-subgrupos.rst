Homomorfismos y Subgrupos
==========================

Lo esencial para el estudio de cualquier clase de objetos algebraicos son las funciones que preservan la estructura algebraica dada en el siguiente sentido. 

Definición
--------------------------

Sean :math:`G` y :math:`H` semigrupos. Una función :math:`f: G \to H` es un homomorfismo proporcionado 

.. math::

    f(ab) = f(a)f(b) \text{ para todo } a,b \in G. 

- Si :math:`f` es *inyectiva* como un mapa de conjuntos, se dice que :math:`f` es un **monomorfismo**.
- Si :math:`f` es *sobreyectiva*, :math:`f` se llama **epimorfismo**.
- Si :math:`f` es *biyectiva*, :math:`f` se llama **isomorfismo**. En este caso, se dice que :math:`G` y :math:`H` son isomorfos (denotado por :math:`G\cong H)`.
- Un homomorfismo :math:`f: G \to G` se denomina endomorfismo de :math:`G` y un isomorfismo :math:`f: G \to G` se denomina automorfismo de :math:`G`.

.. note::

    - Si :math:`f: G \to H` y :math:`g: H \to K` son homomorfismos de semigrupos, es fácil ver que :math:`g f: G \to K` es también un homomorfismo.
    - La composición de los monomorfismos es un monomorfismo;
    - La composición de los epimorfismos es un epimorfismos;
    - La composición de los isomorfismos es un isomorfismo;
    - La composición de los automorfismos es un automorfismo;
    - Si :math:`G` y :math:`H` son grupos con identidades :math:`e_{G}` y :math:`e_{H}` respectivamente y :math:`f: G \to H `es un homomorfismo, entonces :math:`f(eG) = eH`; sin embargo, **esto no es cierto para los monoides** (ejercicio 1).
    - Además :math:`f (a^{-1}) = f(a)^{-1}` para todo :math:`a \in G` (ejercicio 1).


Ejemplo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

El mapa :math:`f: \mathbb{Z}\to \mathbb{Z}_{m}` dado por :math:`x\mapsto \overline{x}` (es decir, cada número entero se asigna a su clase de equivalencia en :math:`\mathbb{Z}_{m}`) es un epimorfismo de grupos aditivos. :math:`f` es el epimorfismo canónico de :math:`\mathbb{Z}` sobre :math:`\mathbb{Z}_{m}`. De manera similar, el mapa :math:`g: \mathbb{Q}\to \mathbb{Q}/\mathbb{Z}` dado por :math:`r\mapsto r` también es un epimorfismo de grupos aditivos.

Ejemplo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Si :math:`A` es un grupo abeliano, entonces el mapa dado por :math:`a\mapsto a^{-1}` es un automorfismo de :math:`A`.

Ejemplo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Si :math:`A` es un grupo abeliano, entonces el mapa dado por :math:`a\mapsto a^{2}` es un endomorfismo de :math:`A`. 

Ejemplo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sean :math:`m > 1`, :math:`k \in \mathbb{N}^{\ast}`. El mapa :math:`g : \mathbb{Z}_{m}\to \mathbb{Z}_{mk}` dada por  :math:`\overline{x} \mapsto \overline{kx}` es un monomorfismo. 

Ejemplo
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Dados los grupos :math:`G` y :math:`H`, hay cuatro homomorfismos:

.. math::

    G \underset{\iota_{1}}{\overset{\pi_{1}}{\leftrightarrows}} G\times H \underset{\iota_{2}}{\overset{\pi_{2}}{\rightleftarrows}} H

dadas por

    - :math:`\iota_{1}(g) = (g,e)`;
    - :math:`\iota_{2}(h) = (e,h)`;
    - :math:`\pi_{1}(g,h) = g`;
    - :math:`\pi_{2}(g,h) = h`. 

:math:`\iota_{i}` es un monomorfismo y :math:`\pi_{j}` es un epimorfismo (:math:`i,j = 1,2`). 


Definición
--------------------------

Sea :math:`f: G \to H` un homomorfismo de grupos.

- El *núcleo de* :math:`f` (denotado :math:`Kerf`) es 

.. math::
    
    \{ a \in G | f(a) = e \in H \}.
    
- Si :math:`A` es un subconjunto de :math:`G`, entonces

.. math::

    f (A) = \{ b \in H | b = f (a) \text{ para algunos } a \in A \}
    
es *la imagen de* :math:`A`. :math:`f(G)` se llama *imagen de* :math:`f` y se denota :math:`Imf`.

- Si :math:`B` es un subconjunto de :math:`H`,

.. math::

    f^{-1}(B) = \{ a \in G | f (a) \in B \}
    
es *la imagen inversa de* :math:`B`. 

.. _teorema-monomorfismo-isomorfismo:

Teorema
--------------------------

Sea :math:`f: G \to H` un homomorfismo de grupos.

    :math:`(i)` :math:`f` es un monomorfismo si y sólo si :math:`Ker f = \{e\}`;

    :math:`(ii)` :math:`f` es un isomorfismo si y solo si :math:`f^{-1}: H \to G` es un homomorfismo tal que :math:`ff^{-1} = I_{H}` y :math:`f^{-1}f = I_{G}`.

**Prueba** :math:`(i)` por hipótesis, sea :math:`f` un monomorfismo y :math:`a \in Ker f`. Luego, tenemos que :math:`f(a) = e_{H} = f(e)` implica :math:`a = e`, por lo tanto :math:`Ker f = \{e\}`. Ahora bien, si :math:`Ker f = \{e\}` y :math:`f(a) = f(b)`, entonces :math:`e_{H} = f(a)f(b)^{-1} = f(a)f(b^{- 1} ) = f(ab^{- 1})`, y así tenemos que :math:`ab^{-1}\in Kerf`. Por lo tanto, :math:`ab^{-1} = e` (que es equilvalente a decir :math:`a = b`) y :math:`f` es un monomorfismo. 

:math:`(ii)` Si :math:`f` es un isomorfismo, entonces, por (13) de Introduccíoion, Sección 3 hay un mapa de conjuntos :math:`f^{-1}: H \to G` tal que :math:`ff^{-1} = I_{H}` y :math:`f^{-1}f = I_{G}`. :math:`f^{-1}` se ve fácilmente como un homomorfismo. Lo contrario es una consecuencia inmediata de (13) de la Introducción, Sección 3 y Definición 2.1.


Sea :math:`G` un semigrupo y :math:`H` un subconjunto no vacío de :math:`G`. Si para cada :math:`a`, si tenemos :math:`ab \in H`, decimos que :math:`H` está cerrado bajo el producto en :math:`G`. Esto equivale a decir que la operación binaria en :math:`G`, cuando se restringe a :math:`H`, es de hecho una operación binaria en :math:`H`.

.. _definicion-de-subgrupo:

Definición
--------------------------

Sea :math:`G` un grupo y :math:`H` un subconjunto no vacío que está cerrado bajo el producto en :math:`G`. Si :math:`H` es en sí mismo un grupo bajo el producto en :math:`G`, entonces se dice que :math:`H` es un subgrupo de :math:`G`. Esto se denota por :math:`H < G`.

Dos ejemplos de subgrupos de un grupo :math:`G` son el propio :math:`G` y el subgrupo trivial :math:`\{e\}` que consta únicamente del elemento de identidad. Un subgrupo :math:`G` tal que :math:`H \not = G`, :math:`H \not = \{e\}` se denomina **subgrupo propio**.

Ejemplo
~~~~~~~~~~~~~

El conjunto de todos los múltiplos de algún entero fijo :math:`n` es un subgrupo de :math:`\mathbb{Z}`, que es isomorfo a :math:`\mathbb{Z}` (ejercicio 7).

Ejemplo
~~~~~~~~~~~~~

En :math:`\mathbb{S}_{n}`, el grupo de todas las permutaciones de :math:`\{1,2,\dots, n\}`, el conjunto de todas las permutaciones que dejan fijo a :math:`n` forma un subgrupo isomorfo a :math:`\mathbb{S}_{n-1}` (ejercicio 8).

Ejemplo
~~~~~~~~~~~~~

En :math:`\mathbb{Z}_{6} = \{\overline{0},\overline{1},\overline{2},\overline{3},\overline{4},\overline{5}\}`, tanto :math:`\{\overline{0},\overline{3}\}` como :math:`\{\overline{0},\overline{2},\overline{4}\}` son subgrupos bajo la suma. Si :math:`p` es primo, :math:`(\mathbb{Z}_{p}, +)` no tiene subgrupos adecuados.

Ejemplo
~~~~~~~~~~~~~

- Si :math:`f: G \to H` es un homomorfismo de grupos, entonces :math:`Ker f`es un subgrupo de :math:`G`.
- Si :math:`A` es un subgrupo de :math:`G`, :math:`f (A)` es un subgrupo de :math:`H`; en particular :math:`Im f` es un subgrupo de :math:`H`.
- Si :math:`B` es un subgrupo de :math:`H`, :math:`f^{-1} (B)` es un subgrupo de :math:`G` (ejercicio 9).

Ejemplo
~~~~~~~~~~~~~

Si :math:`G` es un grupo, entonces el conjunto :math:`Aut G` de todos los automorfismos de :math:`G` es un grupo, con la composición de funciones como operación binaria (ejercicio 15).

Según el :ref:`propiedades-basicas-de-grupos` 1.2, el elemento identidad de cualquier subgrupo :math:`H` es el elemento identidad de :math:`G` y el inverso de :math:`a \in H` es el inverso :math:`a^{-1}` de :math:`a` en :math:`G`.

Teorema
--------------------------

Sea :math:`H` un subconjunto no vacío de un grupo :math:`G`. Entonces :math:`H` es un subgrupo de :math:`G` si y solo si :math:`ab^{-1} \in H` para todo :math:`a, b \in H`.

**Prueba**. :math:`(\Leftarrow)` Existe un :math:`a \in H` y por lo tanto :math:`e = aa^{-1} E H`. Por lo tanto, para cualquier :math:`b \in H`, :math:`b^{-1} = eb^{-1} \in H`. Si :math:`a, b \in H`, entonces :math:`b^{-1} \in H` y por lo tanto :math:`ab = a(b^{-1}){-1} \in H`. El producto en :math:`H` es asociativo ya que :math:`G` es un grupo. Por tanto, :math:`H` es un (sub)grupo. :math:`(\Rightarrow)` es trivial.

Corolario
--------------------------

Si :math:`G` es un grupo y :math:`\{H_{i} | i\in I\}` es una familia de subgrupos no vacía, entonces :math:`\displaystyle\bigcap_{i\in I}H_{i}` es un subgrupo de :math:`G`.

**Prueba. Pendiente.**


Definición
--------------------------

Sea :math:`G` un grupo y :math:`X` un subconjunto de :math:`G`. Sea :math:`\{H_{i} | i\in I\}` la familia de todos los subgrupos de :math:`G` que contienen :math:`X`. Entonces :math:`\displaystyle\bigcap_{i\in I}H_{i}` se denomina subgrupo de :math:`G` generado por el conjunto :math:`X` y se denota :math:`\langle X\rangle`.

Los elementos de :math:`X` son los generadores del subgrupo :math:`\langle X\rangle`, que también pueden ser generados por otros subconjuntos (es decir, podemos tener :math:`\langle X\rangle = \langle Y \rangle` con :math:`X\not = Y`). Si :math:`X = \{a_{1}, a_{2},\dots, a_{n}\}`, escribimos :math:`\langle a_{1}, a_{2},\dots, a_{n}\rangle` en lugar de :math:`\langle X\rangle`. Si :math:`G = \langle a_{1}, a_{2},\dots, a_{n}\rangle`, :math:`a_{i} \in G`, se dice que :math:`G` se genera de forma finita. Si :math:`a \in G`, el subgrupo :math:`\langle a \rangle` se llama el (sub)grupo cíclico generado por :math:`a`.

Teorema
--------------------------

Sean :math:`G` un grupo y :math:`X` subconjunto no vacío de :math:`G`, entonces el subgroup :math:`\langle X\rangle` generado por :math:`X` consiste de todos los productos finitos de la forma :math:`a_{1}^{n_{1}} a_{2}^{n_{2}} \dots a_{r}^{n_{r}}` (:math:`a_{i} \in X, n_{i} \in \mathbb{Z}`). En particular para todo :math:`a e G`, :math:`\langle a \rangle = \{a_{n} | n \in \mathbb{Z}\}`.

**Bosquejo de la prueba**. Demuestre que el conjunto :math:`H` de todos esos productos es un subgrupo de :math:`G` que contiene :math:`X` y está contenido en cada subgrupo que contiene :math:`X`. Por lo tanto, :math:`H < \langle X \rangle < H`. :math:`\blacksquare`

Ejemplos
--------------------------

El grupo aditivo :math:`\mathbb{Z}` es un grupo cíclico infinito con generador :math:`1`, ya que según la :ref:`producto-n-estandar` 1.8 (notación aditiva), :math:`m1=m` para todo :math:`m\in\mathbb{Z}`. Por supuesto, las "potencias" del elemento generador no necesitan ser todas distintas como lo son en :math:`\mathbb{Z}`. El subgrupo trivial :math:`\langle e \rangle` de cualquier grupo es cíclico; el subgrupo multiplicativo :math:`\langle i \rangle` en :math:`\mathbb{C}` es cíclico de orden :math:`4` y para cada m el grupo aditivo :math:`\mathbb{Z}_{m}` es cíclico de orden :math:`m` con generador :math:`1 \in \mathbb{Z}_{m}`. En la Sección :doc:`03-grupos-ciclicos` demostraremos que todo subgrupo cíclico es isomorfo a :math:`\mathbb{Z}` o :math:`\mathbb{Z}` para algunos :math:`m`. Además, vea el ejercicio 12.

Si :math:`\{H_{i} | i \in I \}` es una familia de subgrupos de un grupo :math:`G`, entonces :math:`\displaystyle\bigcup_{i \in I} H_{i}` no es un subgrupo de :math:`G` en general.

El subgrupo :math:`\langle \displaystyle\bigcup_{i \in I} H_{i}\rangle` generado por el conjunto :math:`\displaystyle\bigcup_{i \in I} H_{i}` se llama subgrupo generado por los grupos :math:`\{H_{i} | i \in I \}`. Si :math:`H` y :math:`K` son subgrupos, el subgrupo :math:`\langle H \cup K \rangle` generado por :math:`H` y :math:`K` se llama la unión de :math:`H` y :math:`K` y se denota :math:`H \vee K` (en notación aditiva: :math:`H + K`).

Ejercicios
--------------------------

    1. Si :math:`f: G \to H` es un homomorfismo de grupos, entonces :math:`f (e_{G}) = e_{h}` y  :math:`f(a^{-1}) = f(a)^{-1}` para todo :math:`a \in G`. Demuestre con un ejemplo que la primera conclusión puede sea ​​falsa si :math:`G, H` son monoides que no son grupos.

    2. Un grupo :math:`G` es abeliano si y solo si el mapa :math:`\iota: G\to H` dado por :math:`a \overset{\iota}{\mapsto} a^{-1}` es un automorfismo. 

    3. Sea :math:`Q_{8}` el grupo (bajo multiplicación de matrices ordinaria) generado por las matrices complejas :math:`A = \left(\begin{matrix} 0 & 1 \\ -1 & 0\end{matrix}\right)` y :math:`B = \left(\begin{matrix} 0 & i \\ i & 0\end{matrix}\right)` donde :math:`i^{2}=-1`. Muestre que :math:`Q_{8}` es un grupo no abeliano de orden :math:`8`. :math:`Q_{8}` se llama grupo de cuaterniones. [Sugerencia: observe que :math:`BA = A^{3}B`, de donde cada elemento de :math:`Q_{8}` es de la forma :math:`A^{i}B^{j}`. Tenga en cuenta también que :math:`A^{4} = B^{4} = I`, donde :math:`I = \left(\begin{matrix} 1 & 0 \\ 0 & 1\end{matrix}\right)` es el elemento de identidad de :math:`Q_{8}`.]

    4. Sea :math:`H` el grupo (bajo multiplicación de matrices) de matrices reales generadas por :math:`C = \left(\begin{matrix} 0 & 1 \\ -1 & 0\end{matrix}\right)` y :math:`C = \left(\begin{matrix} 0 & 1 \\ 1 & 0\end{matrix}\right)`. Demuestre que :math:`H` es un grupo no abeliano de orden :math:`8` que no es isomorfo al grupo de cuaterniones del ejercicio 3, pero es isomorfo al grupo :math:`D_{4}^{\ast}`.

    5. Sea :math:`S` un subconjunto no vacío de un grupo :math:`G` y una relación en :math:`G` definida por :math:`a \sim b` si y solo si :math:`ab^{-1} \in S`. Demuestrar que :math:`\sim` es una relación de equivalencia si y solo si :math:`S` es un subgrupo de :math:`G`.

    6. Un subconjunto finito no vacío de un grupo es un subgrupo si y solo si está cerrado bajo el producto en :math:`G`.
    
    7. Si :math:`n` es un número entero fijo, entonces :math:`\{kn | k \in \mathbb{Z}\} \subset \mathbb{Z}` es un subgrupo aditivo de :math:`\mathbb{Z}`, que es isomorfo a :math:`\mathbb{Z}`.
    
    8. El conjunto :math:`\{\sigma \in \mathbb{S}_{n} | \sigma (n) = n \}` es un subgrupo de :math:`\mathbb{S}_{n}` que es isomorfo a :math:`\mathbb{S}_{n-1}`.

    9. Sea :math:`f: G \to H` un homomorfismo de grupos, :math:`A` un subgrupo de :math:`G` y :math:`B` un subgrupo de :math:`H`.
    
        :math:`(a)` :math:`Ker f` y :math:`f^{-1} (B)` son subgrupos de :math:`G`.

        :math:`(b)` :math:`f(A)` es un subgrupo de :math:`H`.
    
    10. Enumere todos los subgrupos de :math:`\mathbb{Z}_{2}\oplus\mathbb{Z}_{2}`. ¿Es :math:`\mathbb{Z}_{2}\oplus\mathbb{Z}_{2}` isomorfo a :math:`\mathbb{Z}_{4}`?
    
    11. Si :math:`G` es un grupo, entonces :math:`C = \{a \in G | ax = xa \text{ para todo } x \in G \}` es un subgrupo abeliano de :math:`G`. :math:`C` se llama el centro de :math:`G`.
    
    12. El grupo :math:`D_{4}^{\ast}` no es cíclico, pero puede ser generado por dos elementos. Lo mismo ocurre con :math:`\mathbb{S}_{n}` (no trivial). ¿Cuál es el número mínimo de generadores del grupo aditivo :math:`\mathbb{Z}\oplus\mathbb{Z}`?
    
    13. Si :math:`G = \langle a\rangle` es un grupo cíclico y :math:`H` es cualquier grupo, entonces todo homomorfismo :math:`f: G \to H `está completamente determinado por el elemento :math:`f(a) \in H`.

    14. Los siguientes subgrupos cíclicos son todos isomorfos: el grupo multiplicativo :math:`\langle i \rangle` en :math:`\mathbb{C}`, el aditivo grupo :math:`\mathbb{Z}_{4}` y el subgrupo :math:`\langle \left(\begin{matrix} 1 & 2 & 3 & 4 \\ 2 & 3 & 4 & 1 \end{matrix}\right) \rangle` de :math:`\mathbb{S}_{4}`. 

    15. Sea :math:`G` un grupo y :math:`Aut G` el conjunto de todos los automorfismos de :math:`G`.
        
        :math:`(a)` :math:`Aut G` es un grupo con composición de funciones como operación binaria. [Ayuda. :math:`1_{G} \in Aut G` es una identidad; los inversos existen según el :ref:`teorema-monomorfismo-isomorfismo` 2.3.]

        :math:`(b)` :math:`Aut \mathbb{Z}\cong \mathbb{Z}_{2}` y :math:`Aut \mathbb{Z}_{6}\cong \mathbb{Z}_{2}`; :math:`Aut \mathbb{Z}_{8}\cong \mathbb{Z}_{2}\oplus \mathbb{Z}_{2}`; :math:`Aut \mathbb{Z}_{p}\cong \mathbb{Z}_{p-1}` (:math:`p` primo).
        
        :math:`(c)` ¿Qué es :math:`Aut \mathbb{Z}_{n}` para arbitrario :math:`n \in \mathbb{N}^{\ast}`?

    16. Para cada primo :math:`p`, el subgrupo aditivo :math:`\mathbb{Z}(p^{\infty})` de :math:`\mathbb{Q}/\mathbb{Z}` (ejercicio 1.10) es generado por el conjunto :math:`\{ \overline{1/p^{\infty}} | n \in \mathbb{N}^{\ast} \}`.
    
    17. Sea :math:`G` un grupo abeliano y sean :math:`H, K` subgrupos de :math:`G`. Demuestre que la unión :math:`H \vee K` es el conjunto :math:`\{ab | a \in H, b \in K \}`. Extienda este resultado a cualquier número finito de subgrupos de :math:`G`.

    18.
        
        :math:`(a)` Sea :math:`G` un grupo :math:`\{ H_{i} | i \in I \}` una familia de subgrupos. Enuncie y demuestre una condición que implicará que :math:`\displaystyle\bigcup_{i\in I} H_{i}` es un subgrupo, es decir, que :math:`\displaystyle\bigcup_{i\in I} H_{i} = \langle \displaystyle\bigcup_{i\in I} H_{i} \rangle`
    
        :math:`(b)` Dé un ejemplo de un grupo :math:`G` y una familia de subgrupos :math:`\{H_{i} | i \in I\}` tal que :math:`\displaystyle\bigcup_{i\in I} H_{i} \not = \langle \displaystyle\bigcup_{i\in I} H_{i} \rangle`.
        
    19.
    
        :math:`(a)` El conjunto de todos los subgrupos de un grupo :math:`G`, parcialmente ordenados por inclusión de la teoría de conjuntos, forma un retículo completo (Introducción, Ejercicios 7.1 y 7.2) en el que g.l.b. de :math:`\{ H_{i} | i \in I \}` es :math:`\displaystyle\bigcap_{i\in I} H_{i}` y el l.u.b. es :math:`\langle \displaystyle\bigcup_{i\in I} H_{i} \rangle` .
        
        :math:`(b)` Mostrar la red de subgrupos del :math:`\mathbb{S}_{3}`, :math:`D_{4}^{\ast}`, :math:`\mathbb{Z}_{6}`, :math:`\mathbb{Z}_{27}`, y :math:`\mathbb{Z}_{36}`. 



 




