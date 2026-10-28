## Proste ułamki łańcuchowe
Dowolny, nieskracalny ułamek $\frac{p}{q}\in\mathbb{Q}$ możemy przekształcić do postaci prostego ułamka łańcuchowego:

$$a_{0}+\frac{1}{a_{1}+\frac{1}{a_{2}+\frac{1}{a_{3}+\frac{1}{\ddots+\frac{1}{a_{n}}}}}}$$

Odczytując kolejne współczynniki $a_{i}$, gdzie $i\in\{0,...,n\}$ możemy przedstawić ten ułamek w
postaci $[a_{0};a_{1},...,a_{n}]$

Co gdybyśmy jako pierwotne potraktowali jednak właśnie ułamki łańcuchowe? Spróbujmy
uogólnić pojęcie prostego ułamka łańcuchowego do szerszego pojęcia, które będziemy nazywać
**łańcuchem**. Zastanówmy się, jak moglibyśmy zdefiniować operacje na łańcuchach, a także ile
jesteśmy w stanie powiedzieć o łańcuchach bez posługiwania się liczbami wymiernymi.

## Łańcuchy
Wprowadźmy rozróżnienie $\mathbb{N}=\{0,1,2,\dots\}$ oraz $\mathbb{N}_{+}=\{1,2,3,4,\dots\}$.

**Łańcuchem** nazywamy dowolne wyrażenie $l$ w postaci $l=[l_{0};l_{1},...,l_{n}]$ gdzie $l_{0}\in\mathbb{Z}$, a $l_{i}\in\mathbb{N}_{+}$ dla $1\leq i\leq n$.

Zbiór wszystkich łańcuchów oznaczamy literą $\mathbb{L}$ i definiujemy następująco:

$$\mathbb{L}=\{l=[l_{0};l_{1},...,l_{n}]:l_{0}\in\mathbb{Z},\forall_{1\le i\le n}l_{i}\in\mathbb{N}_{+}\}$$

Dowolny łańcuch w postaci $[l_{0};]$ nazywamy **łańcuchem pustym**, a łańcuchy w postaci
$[0;l_{1},l_{2},...,l_{n}]$ nazywamy **łańcuchami prostymi**.

Łańcuch w postaci $[0;]$ nazywamy łańcuchem zerowym i oznaczamy go przez $0$.

## Kardynalność
Oczywiście każdy łańcuch jest skończony, więc dla łańcucha o długości $n$ mamy dokładnie $|\mathbb{Z}\times\mathbb{N}_{+}^{n}|$ różnych łańcuchów. Jako, że $n\in\mathbb{N}$ to różnych długości jest przeliczalnie wiele, możemy
więc powiedzieć, że:

$$|\mathbb{L}|=\left|\bigcup_{n=0}^{\infty}\mathbb{Z}\times\mathbb{N}_{+}^{n}\right|$$

Przeliczalna suma zbiorów przeliczalnych zawsze daje zbiór przeliczalny, więc $\mathbb{L}$ jest zbiorem
przeliczalnym:

$$|\mathbb{L}|=\aleph_{0}$$

## Operatory
Niech $l=[l_{0};l_{1},...,l_{n}]\in\mathbb{L}$ Liczbę $l_{0}$ nazywamy **głową** łańcucha $l$, a ciąg $l_{1},...,l_{n}$ **ogonem** łańcucha $l$. Liczbę $n$ nazywamy **długością** łańcucha $l$.

Pojęcia te zdefiniujmy matematycznie jako:

$$\lambda(l)=\lambda([l_{0};l_{1},...,l_{n}])=n$$

$$\chi(l)=[l_{0};]$$

$$\tau(l)=[0;l_{1},...,l_{n}]$$

Odwrócenie łańcucha $l$ oznaczamy jako $\rho(l)$, definujemy je następująco:

$$\rho(l)=\rho([l_{0};l_{1},...,l_{n}])=[l_{0};l_{n},...,l_{1}]$$

Niech $l,m\in\mathbb{L}$ będą łańcuchami, złączenie łańcuchów $l,m$ oznaczamy jako $l\bowtie m$ definiujemy je
następująco:

$$l\bowtie m =[l_{0};l_{1},...,l_{n}]\bowtie[m_{0};m_{1},...,m_{k}]=[l_{0}+m_{0};l_{1},...,l_{n},m_{1},...,m_{k}]$$

Dowolną liczbę całkowitą $x\in\mathbb{Z}$ definiujemy jako łańcuch pusty $x=[x;]\in\mathbb{L}$. W szczególności 
$[0;]=0$ Możemy zauważyć, że $\mathbb{Z}\subset\mathbb{L}$.

## Przycięcia
Niech $k\in\mathbb{N}$ i $l\in\mathbb{L}$. Funkcję $L_{k}:\mathbb{L}\rightarrow\mathbb{L}$ nazywamy $k$-tym przycięciem lewostronnym, a funkcję
$R_{k}: \mathbb{L}\rightarrow\mathbb{L}$ $k$-tym przycięciem prawostronnym. 

Funkcje te definujemy następująco:

$$L_{k}(l)=\begin{cases}
[l_{k};l_{k+1},...,l_{n}], \quad 0\leq k\leq n \\
[0;], \qquad k>n
\end{cases}$$

$$R_{k}(l)=\begin{cases}
[l_{0};l_{1},...,l_{n-k}], \quad 0\leq k\leq n \\
[0;], \quad k>n
\end{cases}$$

## Relacje
Niech $l,m\in\mathbb{L}$. Mówimy, że łańcuchy $l , m$ są **silnie równe**, jeżeli są tej samej długości i
odpowiadające sobie elementy są takie same:

$$l\equiv m\iff\lambda(l)=\lambda(m)\land \forall_{0\leq i\le\lambda(l)} l_{i}=m_{i}$$

Mówimy, że $l, m$ są **ogonowo równe**, jeżeli zachodzi warunek:

$$l\cong m\iff\tau(l)\equiv\tau(m)$$

Niech $k\in\mathbb{Z}$, a $\diamond$ oznacza dowolną z relacji $<,\le,>,\ge$ mówimy, że:

$$l\text{ }\widetilde{\diamond}\text{ }k\iff \forall_{0\leq i\le\lambda(l)} l_{i}\diamond k$$

Zdefinujmy funkcję $\sigma:\mathbb{L}\times \mathbb{L}\rightarrow\mathbb{N}$, mówiącą o stopniu podobieństwa łańcuchów $l, m$:

$$\sigma(l,m)= \max\bigg\{  \lambda(L_{x}(l)) :\big( 0\leq x\leq\lambda(l), \exists_{y\in\{0,\dots,\lambda(m)\}} :L_{x}(l)\cong L_{y}(m)\big)\bigg\}$$

## Przestrzenie $k$-Zaremby
Podzbiór $\mathcal{Z}_{k}\subset\mathbb{L}$, gdzie $k\in\mathbb{N}$ nazywamy **przestrzenią $k$-Zaremby** i definiujemy go następująco:

$$\mathcal{Z}_{k}=\{l\in\mathbb{L}:\chi(l)=0\wedge\tau(l)\widetilde{\leq}k\}$$

Dla $k=5$ możemy mówić o **przestrzeni Zaremby**, którą skrótowo będziemy oznaczać jako $\mathcal{Z}$.

Możemy zauważyć, że zachodzi:

$$\mathcal{Z}_{0}\subset \mathcal{Z}_{1}\subset \mathcal{Z}_{2}\subset\dots$$

Zbiór $\mathcal{Z}_{\infty}$ oznaczać będzie zbiór wszystkich łańcuchów prostych:

$$\mathcal{Z}_{\infty}=\bigcup_{k=0}^\infty \mathcal{Z}_{k}=\{l\in\mathbb{L}:\chi(l)=0\}$$

## Wartościowanie
Niech funkcja $\Lambda:\mathbb{L}\rightarrow\mathbb{Q}$ będzie **wartościowaniem** łańcucha $l\in\mathbb{L}$. Funkcję tą
definiujemy rekurencyjnie:

$$\Lambda(l)=\begin{cases}l_{0},&l=[l_{0};]\\ l_{0}+\frac{1}{\Lambda(L_{1}(l))},&l\ne[l_{0};]\end{cases}$$

Pozwala nam ona wrócić z algebry łańcuchów do znanego zbioru liczb wymiernych.

## Mianownik
Mianownikiem łańcucha $l\in\mathbb{L}$ nazywamy liczbę $\Delta(l)$ gdzie $\Delta:\mathbb{L}\rightarrow\mathbb{N}_{+}$ jest funkcją mianownikową
łańcucha $l$ daną wzorem rekurencyjnym:

$$\Delta(l)=\begin{cases}1,&\lambda(l)=0\\ l_{1},&\lambda(l)=1\\ l_{1}\cdot\Delta(L_{1}(l))+\Delta(L_{2}(l)),&\lambda(l)\ge2\end{cases}$$

Możemy zauważyć, że jeżeli $m=[m_{0};]$ jest łańcuchem pustym to $\Delta(m)=1$ Odzwierciedla to
mianowniki ułamka wymiernego, gdzie $\Lambda(m)=\frac{m}{1}$.

> [!example] Dowód
> Spróbujmy udowodnić indukcyjnie, że $\Delta$ jest zdefiniowana poprawnie. Na potrzeby dowodu niech $N(l)$ oznacza licznik, a $D(l)$ mianownik ułamka wymiernego $\Lambda(l)\in\mathbb{Q}$, zachodzi więc:
>
>
 > $$\Lambda(l)=\frac{N(l)}{D(l)}$$
>
>
>**1. Baza indukcji**
> **I. Dla $\lambda(l)=0$**
>
>
 > $$\Lambda([l_{0};])=l_{0}=\frac{l_{0}}{1}\Rightarrow D(l)=1=\Delta(l)$$
>
> 
> **II. Dla $\lambda(l)=1$**
>
>
 > $$\Lambda([l_{0};l_{1}])=l_{0}+\frac{1}{l_{1}}=\frac{l_{0}\cdot l_{1}+1}{l_{1}}\Rightarrow D(l)=l_{1}=\Delta(l)$$
>
> 
> **2. $Z_{i}$**
>
>
> $$D(L_{1}(l))=\Delta(L_{1}(l)),\quad D(L_{2}(l))=\Delta(L_{2}(l))$$
>
> 
> **3. $T_{i}$**
>
>
 > $$D(l)=\Delta(l)$$
>
> 
> **4. Dowód indukcyjny dla $\lambda(l)\ge 2$**
>
>
 > $$\Lambda(l)=l_{0}+\frac{1}{\Lambda(L_{1}(l))}=l_{0}+\frac{1}{\frac{N(L_{1}(l))}{D(L_{1}(l))}}=l_{0}+\frac{D(L_{1}(l))}{N(L_{1}(l))}=\frac{l_{0}N(L_{1}(l))+D(L_{1}(l))}{N(L_{1}(l))}\Rightarrow$$
>
>
>
 > $$\Rightarrow D(l)=N(L_{1}(l))\quad(1)$$
>
> 
>
> 
 > $$\Lambda(L_{1}(l))=l_{1}+\frac{1}{\Lambda(L_{2}(l))}=l_{1}+\frac{1}{\frac{N(L_{2}(l))}{D(L_{2}(l))}}=l_{1}+\frac{D(L_{2}(l))}{N(L_{2}(l))}=\frac{l_{1}N(L_{2}(l))+D(L_{2}(l))}{N(L_{2}(l))}\Rightarrow$$
>
>
>
 >$$\Rightarrow D(L_{1}(l))=N(L_{2}(l))\quad(2)$$
>
> 
> Z powyższego przypadku rozpiszmy także wzór na licznik $N(L_{1}(l))$:
>
>
 > $$N(L_{1}(l))=l_{1}N(L_{2}(l))+D(L_{2}(l))\stackrel{(1)(2)}{\implies}D(l)=l_{1}\cdot D(L_{1}(l))+D(L_{2}(l))\stackrel{Z_{i}}{\implies}$$
>
>
>
 > $$\implies D(l)=l_{1}\cdot\Delta(L_{1}(l))+\Delta(L_{2}(l))\implies D(l)=\Delta(l)\qquad\blacksquare$$

Własności mianownika $\Delta$ dla dowolnych $x\in\mathbb{Z}$, $a,b,c,d\in\mathbb{N}$:
-  $\Delta(0)=1$
- $\Delta(x)=1$
- $\Delta([x;a])=a$
- $\Delta([x;a,b])=ab+1$
- $\Delta([x;a,b,c])=abc+a+c$
- $\Delta([x;a,b,c,d])=abcd+ab+ad+cd+1$

## Licznik
Licznikiem łańcucha $l\in\mathbb{L}$ nazywamy liczbę $\Gamma(l)$ gdzie $\Gamma:\mathbb{L}\rightarrow\mathbb{Z}$ jest funkcją licznikową daną
wzorem rekurencyjnym:

$$\Gamma(l)= \begin{cases} l_0,&\lambda(l)=0,\\ l_0\Delta(l)+\Delta(L_1(l)),&\lambda(l)\ge1. \end{cases}$$

## Własności operatorów:
Zbadajmy jak oddziałują na siebie zdefiniowane dotychczas operatory. Możemy wykazać, że
zachodzą następujące własności:

- **Inwolutywność odwrócenia**

$$\rho(\rho(l))\equiv l$$

- **Element neutralny złączenia**

$$l\bowtie[0;]\equiv[0;]\bowtie l\equiv l$$

- **Zerowanie się łańcucha dla złożenia $\chi\circ\tau$**

$$\chi(\tau(l))\equiv\tau(\chi(l))\equiv0$$

- **Łączność złączenia**

$$(l \bowtie m)\bowtie n\equiv l\bowtie(m\bowtie n)$$

- **Składanie przycięć**

$$L_{a}(L_{b}(l))\equiv L_{a+b}(l)$$

$$R_{a}(R_{b}(l))\equiv R_{a+b}(l)$$

- **Mieszanie przycięć**

$$L_{a}(R_{b}(l))\equiv R_{b}(L_{a}(l))$$

- **Rozkład łańcuchów**

$$l\equiv \chi(l)\bowtie\tau(l)$$

- **Odwrócenie ogona**

$$\tau(\rho(l))\equiv \rho(\tau(l))$$

- **Złączenie całkowite odwrotności**

$$\rho(l\bowtie m)\equiv\rho(m)\bowtie\rho(l)$$

>[!danger] Twierdzenie o mianowniku odwrócenia
>Dla dowolnego łańcucha $l\in \mathbb{L}$ zachodzi:
>
> $$\Delta(l)=\Delta(\rho(l))$$
> 
>*[[Projekt 2 – Mianownik odwrócenia|Dowód]]*

> [!danger] Twierdzenie o mianowniku złączenia całkowitego
> Dla dwóch dowolnych niepustych łańcuchów $l,m\in \mathbb{L}$ zachodzi:
>
 >$$\Delta(l\bowtie m)=\Delta(I)\cdot\Delta(m)+\Delta(R_{1}(l))\cdot\Delta(L_{1}(m))$$

## Redefinicja hipotez
Mając sformułowane podstawowe pojęcia, możemy spróbować przedstawić hipotezę Zaremby wewnątrz algebry łańcuchów.

Niech $\mathcal{D}_n^k$ oznacza zbiór wszystkich mianowników łańcuchów długości $n$, należących do przestrzeni $\mathcal{Z}_k$ gdzie $n,k\in\mathbb N$. Formalnie:

$$\mathcal D_n^k= \{\Delta(l):l\in\mathcal Z_k \land \lambda(l)=n\}$$

Zbiór wszystkich mianowników generowanych przez przestrzeń $\mathcal{Z}_k$ oznaczmy przez $\mathcal{D}^k$:

$$\mathcal D^k=  
\bigcup_{n=0}^{\infty}\mathcal D_n^k  
=\Delta(\mathcal Z_k)$$

**Hipotezę Zaremby** z ograniczeniem współczynników do $5$ możemy sformułować następująco:

$$\forall_{q\in\mathbb N_+}  
\ \exists_{z\in\mathcal Z_5}:  
\Delta(z)=q$$

Równoważnie:
$$\mathcal D^5=\mathbb{N}_+$$

Innymi słowy, aby udowodnić hipotezę Zaremby, należy wykazać, że funkcja:

$$\Delta:\mathcal Z_5\longrightarrow\mathbb N_+$$

jest suriekcją.

**Hipoteza Hensleya**, według której wszystkie dostatecznie duże mianowniki występują w rozwinięciach o współczynnikach nieprzekraczających $2$, możemy sformułować następująco:

$$\exists_{n_0\in\mathbb N_+}  
\forall_{q\in\mathbb N_+}:  
q\ge n_0\implies  
\exists_{p\in\mathcal Z_2}\ \Delta(p)=q$$

Równoważnie:

$$\exists_{n_0\in\mathbb N_+}:  
\{q\in\mathbb N_+ : q\ge n_0\}  
\subseteq\mathcal D^2$$

W przeciwieństwie do hipotezy Zaremby nie wymagamy, aby obraz funkcji $\Delta$ był całym zbiorem $\mathbb{N}_+$, lecz aby jego dopełnienie było skończone.

Liczba $n_0$ jest pewną dodatnią liczbą całkowitą, od której każdy mianownik $q$ występuje jako mianownik co najmniej jednego nieskracalnego ułamka wymiernego reprezentowanego przez łańcuch $l\in\mathcal{Z}_2$. Zgodnie z badaniami dr Pawlika, liczba ta (o ile istnieje) musiałaby spełniać własność $n_{0}>10^7$.