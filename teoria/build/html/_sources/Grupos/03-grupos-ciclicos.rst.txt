Grupos Cíclicos
===============

La estructura de los grupos cíclicos es relativamente simple. Caracterizaremos completamente todos los grupos cíclicos (hasta el isomorfismo).

.. _primer-teorema-grupo-ciclico:

Teorema
--------------------------

*Todo subgrupo* :math:`H` *del grupo de aditivos* :math:`\mathbb{Z}` *es cíclico*. *Sea* :math:`H = \langle 0 \rangle` *o* :math:`H = \langle m \rangle`, *donde* :math:`m` *es el número entero menos positivo en* :math:`H`. *En particular, si* :math:`H \not = \langle 0 \rangle`, *entonces* :math:`H` *es infinito*.


**Prueba** Sea :math:`H = \langle 0 \rangle` o :math:`H` contiene un número entero positivo mínimo :math:`m`. Claramente :math:`\langle m \rangle = \{ km | k \in \mathbb{Z} \} \subset H`. Por el contrario, si :math:`h \in H`, entonces :math:`h = qm + r` con :math:`q, r \in \mathbb{Z}` y :math:`0\leq r <m `(algoritmo de división). Dado que :math:`r = h - qm \in H` la minimidad de :math:`m` implica :math:`r = 0` y :math:`h = qm`. De ahí que el :math:`H \subset \langle m \rangle`. Si :math:`H \not = \langle 0 \rangle`, está claro que :math:`H = \langle m \rangle` es infinito.

.. _teorema-grupo-ciclico-segun-el-orden:

Teorema
--------------------------

*Sea* :math:`H` *un grupo cíclico*:

    :math:`(i)` *Si* :math:`H` *es infinito entonces  es isomorfo al grupo aditivo* :math:`\mathbb{Z}`.

    :math:`(ii)` *Si* :math:`H` *es finito de orden* :math:`m` *entonces es isomorfo al grupo aditivo* :math:`\mathbb{Z}_{m}`.

**Prueba**. Sea :math:`a\in H: \langle a \rangle=H` y consideremos el mapa

.. math::

    \begin{align}
        \mathbb{Z} &\to H           \\
        k          &\mapsto a^{k}
    \end{align}

Notar que es un **morfismo de grupos**

.. math::

    f(k+k')=a^{k+k'}=a^{k}a^{k'}=f(k)f(k'),

más aún, es un **epimorfismo**.

- si :math:`f` es isomorfo :math:`\Rightarrow` :math:`H` es isomorfo a :math:`\mathbb{Z}`.

si :math:`f` no es isomorfismo entonces :math:`Kerf\not = \{ 0 \}`.

Así :math:`Kerf < \mathbb{Z}` distinto de :math:`\{ 0 \}` :math:`\Rightarrow` :math:`\exists n\in \mathbb{Z}_{+}:Kerf=\langle n \rangle`, por el :ref:`primer-teorema-grupo-ciclico` anterior.

Ahora, esto implica :math:`a^{n}=e` y :math:`n` es el menor número natural que satisface esta condición. Además

.. math::

    \begin{align}
        a^{r} = a^{s} &\Leftrightarrow a^{r}a^{-s} = e                              \\
                      &\Leftrightarrow a^{r-s} = e                                  \\
                      &\Leftrightarrow r-s \in Kerf                                 \\
                      &\Leftrightarrow r-s \in \langle n \rangle \Rightarrow n|r-s.
    \end{align}

Luego

.. math::

    \begin{align}
        a^{r} = a^{s} &\Leftrightarrow \overline{r}=\overline{s} \text{ en } \mathbb{Z}/n\mathbb{Z}.
    \end{align}

Definimos

.. math::

    \begin{align}
        \overline{f}:\mathbb{Z}/n\mathbb{Z} &\to H           \\
        \overline{r}                        &\mapsto a^{r}
    \end{align}

y :math:`\overline{f}` es un **isomorfismo**.

Notar que si :math:`a^{N}\in H\Rightarrow N=qn=+r` con :math:`0\leq r < N` y :math:`a^{N}= (a^{n})^{q}a^{r}=ea^{r}=\overline{f}(\overline{r})` :math:`\blacksquare`

.. _orden-de-un-grupo:

Definición
------------------------------

Sea :math:`G` un grupo y :math:`a \in G`. El orden de :math:`a` es el orden del subgrupo cíclico :math:`\langle a \rangle`. Lo denota :math:`|a|`.


Teorema
------------------------------

*Sea* :math:`G` *un grupo y* :math:`a \in G`.

1. *si* :math:`|a| = \infty` *entonces*

    :math:`(i)` :math:`a^{k} = e` *si y sólo si* :math:`k = 0`.

    :math:`(ii)` *Los elementos* :math:`\{ a^{k}|k\in \mathbb{Z} \}` *son todos distintos*.

2. *si* :math:`|a| = m` *entonces*

    :math:`(i)` :math:`m` *es el menor natural tal que* :math:`a^{m} = e`;

    :math:`(ii)` :math:`a^{m} = e \Leftrightarrow m|k`;

    :math:`(iii)` :math:`a^{k} = a^{l} \Leftrightarrow m|k-l`;

    :math:`(iv)` :math:`\langle a \rangle = \{a, a^{2}, a^{3}, \dots, a^{m}=e \}`:

    :math:`(v)` si :math:`k|m \Rightarrow |a^{k}|=m/k`

Teorema
------------------------------

*Sean* :math:`G` *y* :math:`K` *dos grupos tal que* :math:`G` *es cíclico*:

    :math:`(i)` *Si* :math:`f: G\to K` *es un homomorfismo de grupos un grupo entonces* :math:`Imf` *es un grupo cíclico*.

    :math:`(ii)` *Todo subgrupo de* :math:`G` *es cíclico. En particular, si* :math:`H` *es un subgrupo no trivial de* :math:`G = \langle a \rangle` *y* :math:`m` *es el número entero menos positivo tal que* :math:`a^{m}\in H`, *entonces* :math:`H = \langle a^{m} \rangle`. 

**Bosquejo de prueba**. Si :math:`f: G\to K` es un homomorfismo de grupos, entonces :math:`Imf = \langle f(a) \rangle`. Para probar la segunda declaración, simplemente traslade la demostración del Teorema 3.1 a notación multiplicativa (es decir, reemplace cada :math:`t \in Z` por :math:`a^{t}` en todo). Esta prueba funciona incluso si :math:`G` es finito.

Recuerde que dos elementos distintos en un grupo pueden generar el mismo subgrupo cíclico.


Teorema
------------------------------

*Sea* :math:`Imf = \langle f(a) \rangle` *un grupo cíclico.*

    :math:`(i)` *Si* :math:`G` *es infinito, entonces* :math:`a` y :math:`a^{-1}` *son los únicos generadores de* :math:`G`.
    
    :math:`(ii)` *Si* :math:`G` *es finito de orden* :math:`m`, *entonces* :math:`a^{k}` *es un generador de* :math:`G` *si y solo si* :math:`(k, m) = 1`.

**Bosquejo de prueba**. Es suficiente asumir que :math:`G = \mathbb{Z}`, en cuyo caso la conclusión es fácil de probar, o que :math:`G = \mathbb{Z}_{m}`.

- Si :math:`(k, m) = 1`, existen :math:`c, d \in \mathbb{Z}` tales que :math:`ck + dm = 1`; usar este hecho para demostrar que :math:`k` genera :math:`\mathbb{Z}_{m}`.

- Si :math:`(k, m) = r > 1`, demuestre que para :math:`n = m /r < m`, :math:`n\overline{k} = \overline{nk} = \overline{0}` y, por tanto, :math:`k` no puede generar :math:`\mathbb{Z}_{m}`. 

Ejercicios
------------------------------

1. Sean :math:`a,b \in G`. Mostrar que
    
    :math:`(i)` :math:`|a| = |a^{-1}|`;

    :math:`(ii)` :math:`|ab| = |ba|`, y

    :math:`(iii)` :math:`|a| = |cac^{-1}|` para todo :math:`c \in G`. 

2. Sea :math:`G` un grupo abeliano que contiene elementos :math:`a` y :math:`b` de órdenes :math:`m` y :math:`m` respectivamente. Demuestre que :math:`G` contiene un elemento cuyo orden es el mínimo común múltiplo de :math:`m` y :math:`m`. [Sugerencia: primero pruebe el caso cuando :math:`(m, n) = 1`.]

3. Sea :math:`G` un grupo abeliano de orden :math:`pq`, con :math:`(p, q) = 1.` Suponga que existe :math:`a,b \in G` tal que :math:`|a| = p`, :math:`|b| = q` y demuestre que :math:`G` es cíclico.

4. Si :math:`f: G\to H` es un homomofismo, :math:`a\in G`, y :math:`f (a)` tiene un orden finito en :math:`H`, entonces :math:`|a|` es infinito o :math:`|f(a)|` divide a :math:`|a|`.

5. Sea :math:`G` el grupo multiplicativo de todas las matrices :math:`2 \times 2` no singulares con entradas racional. Demuestre que :math:`a =  \left(\begin{matrix} 0 & -1 \\ 1 & 0 \end{matrix}\right)` tiene orden :math:`4` y :math:`b =  \left(\begin{matrix} 0 & 1 \\ -1 & -1 \end{matrix}\right)` tiene orden :math:`3`, pero :math:`ab` tiene orden infinita. A la inversa, demuestre que el grupo aditivo :math:`\mathbb{Z}_{2} \oplus \mathbb{Z}` contiene elementos distintos de cero :math:`a, b` de orden infinito, de modo que :math:`a + b` tiene un orden finito.

7. Sea :math:`p` primo y :math:`H` un subgrupo de :math:`\mathbb{Z}(p^{\infty})` (Ejercicio 1.10). 

    :math:`(a)` Cada elemento de :math:`\mathbb{Z}(p^{\infty})` tiene un orden finito pn para algunos :math:`n \geq 0`.

    :math:`(b)` Si al menos un elemento de :math:`H` tiene orden :math:`p^{k}` y ningún elemento de :math:`H` tiene orden mayor que :math:`p^{k}`, entonces :math:`H` es es el subgrupo cíclico generado por :math:`\overline{1/p^{k}}`, de donde :math:`H \cong \mathbb{Z}(p^{\infty})`.

    :math:`(c)` Si no hay límite superior en los órdenes de los elementos de :math:`H`, entonces :math:`H = \mathbb{Z}(p^{\infty})`; [vea el Ejercicio 2.16].

    :math:`(d)` Los únicos subgrupos propios de :math:`\mathbb{Z}(p^{\infty})` son los grupos cíclicos finitos :math:`C_{n} = \langle \overline{1/p^{k}} \rangle`, (:math:`n = 1, 2, \dots`). Además, :math:`\langle \overline{0} \rangle = C_{0} < C_{1} < C_{2} < C_{3} < \cdots`.
    
    :math:`(e)` Sean :math:`x_{1}, x_{2}, x_{3}, \dots` ser elementos de un grupo abeliano :math:`G` tal que :math:`|x_{1}| = p`, :math:`px_{2} = x_{1}, px_{3} = x_{2}, \dots, px_{n+1} = x_{n}, \dots` El subgrupo generado por :math:`x_{i}` (:math:`i \geq 1`) es isomorfo a :math:`\mathbb{Z}(p^{\infty})`. [Sugerencia: Verifique que el mapa inducido por :math:`x_{i} \mapsto \overline{1/p^{i}}` sea un isomorfismo bien definido.]

6. Si :math:`G` es un grupo cíclico de orden :math:`n` y :math:`k|n`, entonces :math:`G` tiene exactamente un subgrupo de orden :math:`k`.

8. Un grupo que tiene solo un número finito de subgrupos debe ser finito.

9. Si :math:`G` es un grupo abeliano, entonces el conjunto :math:`T` de todos los elementos de :math:`G` con orden finito es un subgrupo de :math:`G`. [Compare el ejercicio 5.]

10. Un grupo infinito es cíclico si y solo si es isomorfo a cada uno de sus subgrupos propios.


