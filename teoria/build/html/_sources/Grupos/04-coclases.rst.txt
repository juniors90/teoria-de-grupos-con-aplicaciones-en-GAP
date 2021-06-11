Coclases
========
 
En este apartado obtenemos los primeros teoremas significativos que relacionan la estructura de un grupo finito :math:`G` con las propiedades teóricas numéricas de su orden :math:`|G|`. Comenzamos extendiendo el concepto de congruencia módulo :math:`m` en el grupo :math:`\mathbb{Z}`. Por definición :math:`a \equiv b (mod~m)` si y solo si :math:`m | a - b`, es decir, si y solo si :math:`a - b` es un elemento del subgrupo :math:`\langle m \rangle= \{mk | k \in \mathbb{Z} \}`. De manera más general (y en notación multiplicativa) tenemos

Definición
---------------------------------

Sea :math:`H < G` y :math:`a, b \in G`, decimos que: 

    - :math:`a` es congruente a la derecha de :math:`b` módulo :math:`H` si :math:`ab^{-1} \in H`. Lo denotamos :math:`a \equiv_{r} b (mod~H)`.
    
    - :math:`a` es congruente a la izquierda de :math:`b` módulo :math:`H` si :math:`a^{-1}b \in H`. Lo denotamos :math:`a \equiv_{l} b (mod~H)`.

Si :math:`G` es abeliano, entonces la congruencia derecha e izquierda módulo :math:`H` coinciden (ya que :math:`ab^{-1} \in H \Leftrightarrow (ab^{-1})^{-1} \in H` y :math:`(ab^{-1})^{-1}=(b^{-1})^{-1}a^{-1}=ba^{-1}`. También existen grupos no abelianos :math:`G` y subgrupos :math:`H` tal que coinciden la congruencia derecha e izquierda (Sección 5), pero esto no es cierto en general.

.. _teorema-de-congruencia-a-derecha:

Teorema
---------------------------------

Sea :math:`G` un grupo tal que :math:`H < G`. 

    :math:`(i)` La congruencia a derecha [resp. a izquierda] :math:`H` es una relación de equivalencia en :math:`G`.

    :math:`(ii)` La clase de equivalencia de :math:`a\in G` vía la congruencia a derecho [resp. a izquierda] módulo :math:`H` es el conjunto
    
    .. math::
        
        Ha = \{ha | h \in H \} \text{ [resp. } aH = \{ah | h \in H\}\text{]}.

    :math:`(iii)` :math:`|Ha| = |H| = |aH|` para todo :math:`a \in G`.
    
.. important::

    - El conjunto :math:`Ha = \{ha | h \in H \}` se llama *clase lateral derecha de* :math:`H` *en* :math:`G`
    - El conjunto :math:`aH = \{ah | h \in H \}` se llama *clase lateral izquierda de* :math:`H` *en* :math:`G`.
    - En general, no es el caso de que una clase lateral derecha sea también una clase lateral izquierda (ejercicio 2).

**Prueba del** :ref:`teorema-de-congruencia-a-derecha` **4.2**. Escribimos :math:`a \equiv b` para :math:`a \equiv_{r} b (mod~H)` y probamos el teorema de congruencia a derecha y clases laterales a derecha. Se aplican argumentos análogos para la congruencia a izquierda.
    
:math:`(i)` Sean :math:`a, b, c \in G`.
    
        - **Reflexiva**: :math:`a \equiv a` ya que :math:`aa^{-1}=e\in H`.

        - **Simétrica**: como
            
            .. math::

                a \equiv b \Rightarrow ab^{-1}\in H \Rightarrow (ab^{-1})^{-1} \in H \Rightarrow ba^{-1} \in H \Rightarrow b \equiv a.

        - **Transitiva**: veamos que se cumple que :math:`a \equiv b` y :math:`b \equiv a` entonces :math:`a \equiv c`.
        
        Ahora bien, si :math:`a \equiv b` y :math:`b \equiv a` entonces :math:`ab^{-1} \in H` y :math:`bc^{-1} \in H`. Luego, tenemos que 
        
        .. math::
        
            ac^{-1} = (ab^{-1})(bc^{-1}) \in H.
            
        Así, :math:`a \equiv c`, que es lo que debíamos probar.
        
        Entonces, la congruencia a derecha [resp. a izquierda] :math:`H` es una relación de equivalencia en :math:`G`.

:math:`(ii)` Sea :math:`C_{r}(a)` la clase de equivalencia de :math:`a \in G` entonces
    
    .. math::
        
        \begin{align}
            b \in C_{r}(a) &\Leftrightarrow a \equiv b                                                  \\
                           &\Leftrightarrow ab^{-1} \in H \Leftrightarrow \exists h \in H : ab^{-1} = h \\
                           &\Leftrightarrow b = h^{-1}a \Leftrightarrow b \in Ha
        \end{align}

    En conclusión, :math:`C_{r}(a) = Ha`.

:math:`(iii)` Sea :math:`\varphi : H \to Ha` dado por :math:`\varphi(a) = ha` entonces :math:`\varphi` tiene inversa :math:`\varphi' : Ha \to H` dada por :math:`\varphi'(a) = (ha)a^{-1}` y tal que

.. math::
    
    \begin{align}
        \varphi\circ\varphi' &= Id_{Ha} &&& \varphi'\circ\varphi &= Id_{H}
    \end{align} 

Luego, :math:`|H| = |Ha|`. :math:`\blacksquare`

.. _corolario-4-3:

Corolario
---------------------------------

Sea :math:`G` un grupo tal que :math:`H < G`. 

    :math:`(i)` :math:`G = \displaystyle\bigcup_{a \in G} Ha = \displaystyle\bigcup_{a \in G} aH`.
        
    :math:`(ii)` :math:`Ha =  Hb` o :math:`Ha \cap  Hb = \emptyset`.

    :math:`(iii)` Para todo :math:`a, b \in G`, :math:`Ha =  Hb \Leftrightarrow ab^{-1} \in H` y :math:`aH =  bH \Leftrightarrow a^{-1}b \in H`.

**Notación aditiva**. Si :math:`H` es un subgrupo de un grupo aditivo, entonces la congruencia módulo a derecha :math:`H` se define por: :math:`a \equiv_{r} b (mod~H) \Leftrightarrow a - b \in G`. La clase de equivalencia de :math:`a \in G` es la clase lateral a derecha :math:`H + a = \{h + a | h \in H\}`; de manera similar para la congruencia a izquierda y las clases laterales a izquierdas. 


Definición
---------------------------------

Sea :math:`H` un subgrupo de un grupo :math:`G`. El índice de :math:`H` en :math:`G`, lo denotamos :math:`[G: H]`, es el número cardinal del conjunto de distintas clases laterales a derechas [resp. a izquierda] de :math:`H` en :math:`G`.

En vista del :ref:`corolario-4-3` 4.3 :math:`(iv)`, :math:`[G: H]` no depende de si se utilizan las clases laterales derecha o izquierda en la definición. Nuestro interés principal está en el caso en que :math:`[G: H]` es finito, lo que puede ocurrir incluso cuando :math:`H` y :math:`G` son grupos infinitos (por ejemplo, :math:`[\mathbb{Z}: \langle m \rangle] = m` por Introducción, Teorema 6.8 :math:`(i)`. Nota que si :math:`H = \langle e \rangle`, entonces :math:`Ha = \{a\}` para cada :math:`a \in G` y :math:`[G: H] = |G|`.


Un conjunto completo de representantes de clases laterales derechas de un subgrupo :math:`H` en un grupo :math:`G` es un conjunto :math:`\left( a_{i} \right)_{i\in I}` que consta precisamente de un elemento de cada clase lateral derecha de :math:`H` en :math:`G` y en :math:`G = \displaystyle\bigsqcup_{i \in I} Ha_{i}`. Claramente, el conjunto :math:`\{ a_{i} \}` tiene cardinalidad :math:`[G: H]`. Tenga en cuenta que dicho conjunto contiene exactamente un elemento de :math:`H` ya que :math:`H = He` es en sí mismo una clase lateral derecha. Se aplican afirmaciones análogas a las clases laterales izquierdas.

Teorema
---------------------------------

Si :math:`K`, :math:`H`, :math:`G` son grupos con :math:`K < H < G`, entonces :math:`[G: K] = [G: H][H: K]`. Si dos de estos índices son finitos, también lo es el tercero.




Ejercicios
--------------------------------- 

1. Sea :math:`G` un grupo y :math:`\{ H_{i} | i \in I \}` una familia de subgrupos de :math:`G`. Entonces, para todo :math:`a \in G`, :math:`\left( \displaystyle\bigcap_{i \in I} H_{i} \right) a = \displaystyle\bigcap_{i \in I} H_{i}a`.

2.

    :math:`(a)` Sea :math:`H` el subgrupo cíclico (de orden :math:`2`) de :math:`\mathbb{S}_{3}` generado por :math:`\left( \begin{matrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{matrix} \right)`. Entonces, ninguna clase lateral izquierda de :math:`H` (excepto la propia :math:`H`) es también una clase lateral derecha. Existe :math:`a \in \mathbb{S}_{3}` tal que :math:`aH \cap Ha = \{ a \}`.
    
    :math:`(b)` Si :math:`K` es el subgrupo cíclico (de orden :math:`3`) de :math:`\mathbb{S}_{3}` generado por :math:`\left( \begin{matrix} 1 & 2 & 3 \\ 2 & 3 & 1 \end{matrix} \right)` entonces cada clase lateral izquierda de :math:`K` es también una clase lateral derecha de :math:`K`.

3. Las siguientes condiciones en un grupo finito :math:`G` son equivalentes. 
    
    :math:`(i)` :math:`|G|` es primo.

    :math:`(ii)` :math:`G \not = \langle e \rangle` y :math:`G` no tiene subgrupos propios.

    :math:`(ii)` :math:`G \cong \mathbb{Z}_{p}` para algunos prime :math:`p`.

4. (Euler-Fermat) Sea :math:`a` un número entero y :math:`p` un primo tal que :math:`p \not | a`. Entonces a :math:`a^{p - 1} \equiv 1 (mod~p)`. [Sugerencia: considere :math:`\overline{a} \in \mathbb{Z}_{p}` y el grupo multiplicativo de elementos distintos de cero de :math:`\mathbb{Z}_{p}`; Ver Ejercicio 1.7.]. De ello se deduce que :math:`a^{p} \equiv a (mod~p)` para cualquier número entero :math:`a`.

5. Demuestrar que solo hay dos grupos distintos de orden :math:`4` (hasta el isomorfismo), es decir, :math:`\mathbb{Z}_{4}` y :math:`\mathbb{Z}_{2} \oplus \mathbb{Z}_{2}`. [Sugerencia: según el Teorema de Lagrange 4.6 , un grupo de orden :math:`4` que no es cíclico debe constar de una identidad y tres elementos de orden :math:`2`.]

6. Sean :math:`H` y :math:`K` subgrupos de un grupo :math:`G`. Entonces :math:`HK` es un subgrupo de :math:`G` si y solo si :math:`HK = KH`.

7. Sea :math:`G` un grupo de orden :math:`p^{k}m`, con :math:`p` primo y :math:`(p, m) = 1`. Sea :math:`H` un subgrupo de orden :math:`p^{k}` y :math:`K` un subgrupo de orden :math:`p^{d}`, con :math:`0 < d \leq k` y :math:`K\not \subset H`. Demuestre que :math:`HK` no es un subgrupo de :math:`G`.

8. Si :math:`H` y :math:`K` son subgrupos de índice finito de un grupo :math:`G` tales que :math:`[G: H]` y :math:`[G: K]` son ​​primos relativos, entonces :math:`G = HK`. 

9. Sea :math:`G` un grupo tal que :math:`H, K, N \lhd G` y :math:`H < N`, entonces :math:`HK \cap N = H (K \cap N)`.

10. Sea :math:`G` un grupo tal que :math:`H, K, N \lhd G`, :math:`H < N`, :math:`H \cap N = K \cap N` y :math:`HN = KN`. Demuestre que :math:`H = K`.

11. Sea :math:`G` un grupo de orden :math:`2n` entonces :math:`G` contiene un elemento de orden :math:`2`. Si :math:`n` es impar y :math:`G` abeliano, solo hay un elemento de orden :math:`2`.

12. Si :math:`H` y :math:`K` son subgrupos de un grupo :math:`G`, entonces :math:`[H \vee K: H] \geq [K: H \cap K]`.

13. Si :math:`p > q` son primos, un grupo de orden :math:`pq` tiene como máximo un subgrupo de orden :math:`p`. [Sugerencia: Suponer que :math:`H`, :math:`K` son subgrupos distintos de orden :math:`p`. Mostrar que :math:`H \cap K = \langle e \rangle`; Utilizar el ejercicio 12 para obtener una contradicción.]

14. Sea :math:`G` un grupo y :math:`a, b \in G` tal que

    :math:`(i)` :math:`|a| = 4 = |b|`;

    :math:`(ii)` :math:`a^{2} = b^{2}`;

    :math:`(iii)` :math:`ba = a^{3}b = a^{-1}b`;

    :math:`(iv)` :math:`a \not = b`;

    :math:`(v)` :math:`G = \langle a, b \rangle`.
    
Muestre que :math:`|G| = 8` y :math:`G \cong Q_{8}`. [Ver el ejercicio 2.3; observe que los generadores :math:`A`, :math:`B` de :math:`Q_{8}` también satisfacen :math:`(i)` - :math:`(v)`.]



