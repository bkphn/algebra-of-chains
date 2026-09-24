## Przedmowa
Plik [[Wstęp do algebry łańcuchów]] został pokazany Dawidowi Piotrowskiemu, w ówczesnej wersji pliku twierdzenie o mianowniku odwrócenia widniało jako nieudowodnione. 27 kwietnia 2026 roku otrzymałem od niego plik, zawierający dowód twierdzenia o mianowniku odwrócenia.

Autorem dalszej części tekstu jest Dawid Piotrowski.

## Dowód na twierdzenie o mianowniku odwrócenia
**Twierdzenie o mianowniku odwrócenia** postuluje, że:

$$ \Delta(l) = \Delta(\rho(l)) $$

gdzie $\Delta(l)$ oznacza mianownik łańcucha $l$, definiowany jako:

$$
\Delta(l) = \begin{cases} 
1, & \lambda(l) = 0 \\ 
l_{1}, & \lambda(l) = 1 \\ 
l_{1} \cdot \Delta(L_{1}(l)) + \Delta(L_{2}(l)), & \lambda(l) \ge 2 
\end{cases}
$$

a $\rho(l)$ oznacza odwrócenie łańcucha $l$, definiowane wzorem:

$$ \rho([l_{0}, l_{1}, \dots, l_{n}]) = [l_{0}, l_{n}, \dots, l_{1}] $$

Twierdzenie to możemy udowodnić wykorzystując silną indukcję. Ponieważ $\Delta(l) = \Delta(\tau(l))$, twierdzenie wystarczy udowodnić dla łańcuchów postaci $[0, l_{0}, l_{1}, \dots, l_{n}]$.

## Baza indukcji

Dla $l = [0]$ ($\lambda(l) = 0$):
$$ \Delta(l) = 1 = \Delta(\rho(l)) $$

Dla $l = [0, l_{1}]$ ($\lambda(l) = 1$) mamy:
$$ \rho([0, l_{1}]) = [0, l_{1}] $$

Zatem trywialnie:
$$ \Delta(\rho([0, l_{1}])) = \Delta([0, l_{1}]) $$

## Krok indukcyjny

Dla $l = [0, l_{k}, l_{k-1}, \dots, l_{1}]$ ($\lambda(l) = k$), załóżmy ($Z_{i}$), że twierdzenie jest spełnione dla wszystkich łańcuchów o długości mniejszej niż $k$, w szczególności:

$$\Delta([0, l_{k-1}, \dots, l_{1}]) = \Delta([0, l_{1}, \dots, l_{k-1}]) $$

oraz

$$\Delta([0, l_{k-2}, \dots, l_{1}]) = \Delta([0, l_{1}, \dots, l_{k-2}]) $$

Wówczas:

$$
\begin{align*}
\Delta([0, l_{k}, \dots, l_{1}]) &= l_{k} \cdot \Delta([l_{k}, l_{k-1}, \dots, l_{1}]) + \Delta([l_{k-1}, \dots, l_{1}]) \\
&= l_{k} \cdot \Delta([0, l_{k-1}, \dots, l_{1}]) + \Delta([0, l_{k-2}, \dots, l_{1}]) \\
&= l_{k} \cdot \Delta([0, l_{1}, \dots, l_{k-1}]) + \Delta([0, l_{1}, \dots, l_{k-2}]) \\
&= \Delta([0, l_{1}, \dots, l_{k-2}, l_{k-1}]) \cdot l_{k} + \Delta([0, l_{1}, \dots, l_{k-2}]) \cdot 1 \\
&= \Delta([0, l_{1}, \dots, l_{k-2}, l_{k-1}]) \cdot \Delta([0, l_{k}]) + \Delta(R_{1}([0, l_{1}, \dots, l_{k-2}, l_{k-1}])) \cdot \Delta(L_{1}([0, l_{k}]))
\end{align*}
$$

Z twierdzenia o mianowniku złączenia:

$$\Delta([0, l_{k}, \dots, l_{1}]) = \Delta([0, l_{1}, \dots, l_{k-1}] \bowtie [0, l_{k}]) = \Delta([0, l_{1}, \dots, l_{k-1}, l_{k}]) $$
