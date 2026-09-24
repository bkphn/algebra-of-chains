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
Łańcuchem nazywamy dowolne wyrażenie $a$ w postaci $a=[a_{0};a_{1},...,a_{n}]$ gdzie $a_{0}\in\mathbb{Z}$, a $\forall_{0<i<n} a_{i}\in\mathbb{N}$

Zbiór wszystkich łańcuchów oznaczamy literą $\mathbb{L}$ i definiujemy następująco:
$$\mathbb{L}=\{l=[l_{0};l_{1},...,l_{n}]:l_{0}\in\mathbb{Z},\forall_{1\le i\le n}l_{i}\in\mathbb{N},n\in\mathbb{N}\}$$
Dowolny łańcuch w postaci $[l_{0};]$ nazywamy **łańcuchem pustym**, a łańcuchy w postaci
$[0;l_{1},l_{2},...,l_{n}]$ nazywamy **łańcuchami prostymi**.

Łańcuch w postaci $[0;]$ nazywamy łańcuchem zerowym i oznaczamy go przez 0.
## Kardynalność
Oczywiście każdy łańcuch jest skończony, więc dla łańcucha o długości $n$ mamy dokładnie $|\mathbb{Z}\times\mathbb{N}^{n}|$ różnych łańcuchów. Jako, że $n\in\mathbb{N}$ to różnych długości jest przeliczalnie wiele, możemy
więc powiedzieć, że:
$$|\mathbb{L}|=|\bigcup_{n=0}^{\infty}\mathbb{Z}\times\mathbb{N}^{n}|$$
Przeliczalna suma zbiorów przeliczalnych zawsze daje zbiór przeliczalny, więc $\mathbb{L}$ jest zbiorem
przeliczalnym:
$$|\mathbb{L}|=\aleph_{0}$$
## Operatory unarne
Niech $l=[l_{0};l_{1},...,l_{n}]\in\mathbb{L}$ Liczbę $l_{0}$ nazywamy głową bądź częścią całkowitą łańcucha $l$, a ciąg
$l_{1},...,l_{n}$ ogonem bądź częścią ułamkową łańcucha $l$. Liczbę $n$ nazywamy długością łańcucha $l$.

Pojęcia te zdefiniujmy matematycznie jako:
$$\lambda(l)=\lambda([l_{0};l_{1},...,l_{n}])=n$$
$$\chi(l)=[l_{0};]$$
$$\tau(l)=[0;l_{1},...,l_{n}]$$
Odwrócenie łańcucha $l$ oznaczamy jako $\rho(l)$, definujemy je następująco:
$$\rho(l)=\rho([l_{0};l_{1},...,l_{n}])=[l_{0};l_{n},...,l_{1}]$$
## Operatory binarne
Niech $l,m\in\mathbb{L}$ będą łańcuchami, złączenie łańcuchów $l,m$ oznaczamy jako $l\bowtie m$ definiujemy je
następująco:
$$l\bowtie m =[l_{0};l_{1},...,l_{n}]\bowtie[m_{0};m_{1},...,m_{k}]=[l_{0}+m_{0};l_{1},...,l_{n},m_{1},...,m_{k}]$$
Dowolny całkowity skalar $x\in\mathbb{Z}$ definiujemy jako łańcuch pusty $x=[x;]\in\mathbb{L}$ W szczególności 
$[0;]=0$ Możemy zauważyć, że $\mathbb{Z}\subset\mathbb{L}$.

Niech $l\in\mathbb{L}$ oraz $x\in\mathbb{Z}$ Operację $+$ nazywamy sumą arytmetyczną, a operację $-$ różnicą
arytmetyczną, definujemy je następująco:
$$l+x=l\bowtie[x;]=[l_{0}+x;l_{1},...,l_{n}]$$
$$l-x=l\bowtie[-x;]=[l_{0}-x;l_{1},...,l_{n}]$$
Przy czym należy zaznaczyć, że jeżeli $m\in\mathbb{L}$ nie jest łańcuchem pustym, to:
$$l+m\ne l\bowtie m$$
Chcąc zdefiniować sumę dwóch niepustych łańcuchów $l, m$ musielibyśmy posłużyć się np.
algorytmem Gospera, korzysta on jednak w tym celu z macierzy. Jako, że konstruujemy łańcuchy
jako pierwotne pojęcia, w oderwaniu od innych struktur matematycznych to pominiemy definicję
sumy dla tych obiektów.
## Przycięcia
Niech $k\in\mathbb{N}$ i $l\in\mathbb{L}$. Funkcję $L_{k}:\mathbb{L}\rightarrow\mathbb{L}$ nazywamy $k$-tym przycięciem lewostronnym, a funkcję
$R_{k}$ $\mathbb{L}\rightarrow\mathbb{L}$ $k$-tym przycięciem prawostronnym. 

Funkcje te definujemy następująco:
$$L_{k}(l)=[l_{k};l_{k+1},...,l_{n}]$$
$$R_{k}(l)=[l_{0};l_{1},...,l_{n-k}]$$
W przypadku, gdy $k\ge\lambda(l)$ przyjmijmy, że:
$$L_{k}(l)=R_{k}(l)=[0;]$$
## Relacje
Niech $l,m\in\mathbb{L}$. Mówimy, że łańcuchy $l , m$ są **silnie równe**, jeżeli są tej samej długości i
odpowiadające sobie elementy są takie same:
$$l\equiv m\Leftrightarrow\lambda(l)=\lambda(m) \land l_{i}=m_{i},\quad\forall_{i\le\lambda(l)}$$
Mówimy, że $l, m$ są **ogonowo równe**, jeżeli zachodzi warunek:
$$l\cong m\Leftrightarrow\tau(l)\equiv\tau(m)$$
Niech $k\in\mathbb{Z}$, a $\diamond$ oznacza dowolną z relacji $<,\le,>,\ge$ mówimy, że:
$$l\text{ }\widetilde{\diamond}\text{ }k\Leftrightarrow l_{i}\diamond k, \quad \forall_{i\le\lambda(l)}$$
Mówimy, że $l, m$ są **ostatecznie równe** jeżeli ich ogony, od pewnego momentu się pokrywają, fakt
ten oznaczamy jako $l\sim m$ i definiujemy następująco:
$$l\sim m\Leftrightarrow\exists_{x,y\in\mathbb{N}}:L_{x}(l)\cong L_{y}(m)$$
Na podstawie ostatecznej równości zdefinujmy funkcję $σ$, mówiącą o stopniu podobieństwa
łańcuchów $l, m$:
$$\sigma(l,m)=\max\{\lambda(L_{x}(l)):L_{x}(l)\cong L_{y}(m)\wedge x\le\lambda(l)\wedge y\le\lambda(m)\}$$
Warto zauważyć, że w defnicji $\sim$ pojawia się ostra mniejszość, a w definicji $\sigma,\le$. Jest to celowy
zabieg w celu uniknięcia wartości maksymalnej ze zbioru pustego, w tym przypadku stopień
podobieństwa łańcuchów $l, m$ wynosi po prostu zero.
## Przestrzenie
Podzbiór $\mathcal{Z}\subset\mathbb{L}$ nazywamy **przestrzenią Zaremby** i definiujemy go następująco:
$$\mathcal{Z}=\{l\in\mathbb{L}:\chi(l)=0\wedge\tau(l)\widetilde{\leq}5\}$$
Podzbiór $\mathcal{P}\subset\mathbb{L}$ nazywamy **przestrzenią Pawlika** i definiujemy go następująco:
$$\mathcal{P}=\{l\in\mathbb{L}:\chi(l)=0\wedge\tau(l)\widetilde{\leq}2\}$$
Podzbiór $\set{l\in\mathbb{L} : \chi(l)=0 \land \tau(\lambda)\widetilde{\leq}0}$ nazywamy **przestrzenią trywialną** $\mathcal{O}$.

Dowolny zbiór $\{l\in\mathbb{L}:\chi(l)=0\wedge\tau(l)\widetilde{\leq}k\}$ gdzie $k\in\mathbb{N}$ nazywamy **przestrzenią $k$-Zaremby** co
oznaczamy jako $\mathcal{Z}_{k}$, w szczególności zachodzi:
	$\mathcal{P}=\mathcal{Z}_{2}$
	$\mathcal{Z}=\mathcal{Z}_{5}$
	$\mathcal{O}=\mathcal{Z}_{0}$
## Łańcuchy właściwe
Dowolny łańcuch $l=[l_{0};l_{1},...,l_{n}]$ nazywamy ułamkiem łańcuchowym bądź **łańcuchem**
**właściwym**, jeżeli $l_{i}\in\mathbb{N}_{+}$ dla każdego $i\in\{1,2,...,n\}$. 

Zbiór łańcuchów właściwych oznaczamy przez $\mathbb{L}^{*}$. Analogicznie przestrzenie $k$-Zaremby nazywamy przestrzeniami właściwymi $k$-Zaremby i oznaczamy je jako $\mathcal{Z}_{k}^{*},\mathcal{Z}^{*},\mathcal{P}^{*},\mathcal{O}^{*}$, przy czym: $O^{*}=\{[0;]\}$ przestrzenie takie formalnie definiujemy jako:
$$\mathcal{Z}_{k}^*=\{l\in\mathbb{L^*}:\chi(l)=0\wedge\tau(l)\widetilde{\leq}k\}$$

Niech funkcja $\Lambda:\mathbb{L}^{*}\rightarrow\mathbb{Q}$ będzie **wartościowaniem** łańcucha właściwego $l\in\mathbb{L}^{*}$. Funkcję tą
definiujemy rekurencyjnie:
$$\Lambda(l)=\begin{cases}l_{0},&l=[l_{0};]\\ l_{0}+\frac{1}{\Lambda(L_{1}(l))},&l\ne[l_{0};]\end{cases}$$

Pozwala nam ona wrócić z algebry łańcuchów do znanego zbioru liczb wymiernych.
Mówimy, że dwa dowolne łańcuchy $l,m\in\mathbb{L}$ są równe, jeżeli spełniają warunek:
$$l=m\Leftrightarrow\Lambda(l)=\Lambda(m)$$

Możemy zauważyć, że $l\equiv m\Rightarrow l=m\Rightarrow l\cong m\Rightarrow l\sim m$.

> [!example] Przykładowo
> Przykładowo $[0;1,1]\not\equiv[0;2]$, ale $[0;1,1]=[0;2]$, ponieważ:
> $\Lambda([0;1,1])=\Lambda([0;2])$
> $0+\frac{1}{1+\frac{1}{1}}=0+\frac{1}{2}$
> $\frac{1}{2}=\frac{1}{2}$

Oczywiście wartościowanie $\Lambda$ pozwala nam na definiowanie podstawowych operacji
arytmetycznych na łańcuchach właściwych:
$$l+m=k\Leftrightarrow\Lambda(l)+\Lambda(m)=\Lambda(k)$$
$$l-m=k\Leftrightarrow\Lambda(l)-\Lambda(m)=\Lambda(k)$$
$$l\cdot m=k\Leftrightarrow\Lambda(l)\cdot\Lambda(m)=\Lambda(k)$$
Chcąc wyznaczyć łańcuch $k\in\mathbb{L}^{*}$ musimy przejść przez zbiór $\mathbb{Q}$. Nie jest to satysfakcjonująca
definicja operacji, lecz dla formalności warto o niej wspomnieć.
## Mianownik
Mianownikiem łańcucha $l\in\mathbb{L}$ nazywamy liczbę $\Delta(l)$ gdzie $\Delta:\mathbb{L}\rightarrow\mathbb{N}$ jest funkcją mianownikową
łańcucha I daną wzorem rekurencyjnym:
$$\Delta(l)=\begin{cases}1,&\lambda(l)=0\\ l_{1},&\lambda(l)=1\\ l_{1}\cdot\Delta(L_{1}(l))+\Delta(L_{2}(l)),&\lambda(l)\ge2\end{cases}$$
Możemy zauważyć, że jeżeli $m=[m_{0};]$ jest łańcuchem pustym to $\Delta(m)=1$ Odzwierciedla to
mianowniki ułamka wymiernego, gdzie $\Lambda(m)=\frac{m}{1}$.

> [!example] Dowód
> Spróbujmy udowodnić indukcyjnie, że $\Delta$ jest zdefiniowana poprawnie. Na potrzeby dowodu niech $N(l)$ oznacza licznik, a $D(l)$ mianownik ułamka wymiernego $\Lambda(l)\in\mathbb{Q}$, zachodzi więc:
> $$\Lambda(l)=\frac{N(l)}{D(l)}$$
> 
> **1. Baza indukcji**
> **I. Dla $\lambda(l)=0$**
> $$\Lambda([l_{0};])=l_{0}=\frac{l_{0}}{1}\Rightarrow D(l)=1=\Delta(l)$$
> 
> **II. Dla $\lambda(l)=1$**
> $$\Lambda([l_{0};l_{1}])=l_{0}+\frac{1}{l_{1}}=\frac{l_{0}\cdot l_{1}+1}{l_{1}}\Rightarrow D(l)=l_{1}=\Delta(l)$$
> 
> **2. $Z_{i}$**
> $$D(L_{1}(l))=\Delta(L_{1}(l)),\quad D(L_{2}(l))=\Delta(L_{2}(l))$$
> 
> **3. $T_{i}$**
> $$D(l)=\Delta(l)$$
> 
> **4. Dowód indukcyjny dla $\lambda(l)\ge 2$**
> $$\Lambda(l)=l_{0}+\frac{1}{\Lambda(L_{1}(l))}=l_{0}+\frac{1}{\frac{N(L_{1}(l))}{D(L_{1}(l))}}=l_{0}+\frac{D(L_{1}(l))}{N(L_{1}(l))}=\frac{l_{0}N(L_{1}(l))+D(L_{1}(l))}{N(L_{1}(l))}\Rightarrow$$
> $$\Rightarrow D(l)=N(L_{1}(l))\quad(1)$$
> 
> $$\Lambda(L_{1}(l))=l_{1}+\frac{1}{\Lambda(L_{2}(l))}=l_{1}+\frac{1}{\frac{N(L_{2}(l))}{D(L_{2}(l))}}=l_{1}+\frac{D(L_{2}(l))}{N(L_{2}(l))}=\frac{l_{1}N(L_{2}(l))+D(L_{2}(l))}{N(L_{2}(l))}\Rightarrow$$
> $$\Rightarrow D(L_{1}(l))=N(L_{2}(l))\quad(2)$$
> 
> Z powyższego przypadku rozpiszmy także wzór na licznik $N(L_{1}(l))$:
> $$N(L_{1}(l))=l_{1}N(L_{2}(l))+D(L_{2}(l))\stackrel{(1)(2)}{\implies}D(l)=l_{1}\cdot D(L_{1}(l))+D(L_{2}(l))\stackrel{Z_{i}}{\implies}$$
> $$\implies D(l)=l_{1}\cdot\Delta(L_{1}(l))+\Delta(L_{2}(l))\implies D(l)=\Delta(l)\qquad\blacksquare$$

Nic nie stoi na przeszkodzie, by mianowniki zdefiniować również na łańcuchach niewłaściwych.

> [!example] Przykład
> Niech $n=[1;5,0,3]$, liczba ta nie istnieje w zbiorze liczb $\mathbb{Q}$. Korzystając ze wzoru na mianownik $\Delta$ możemy obliczyć:
> $$\Delta([1;5,0,3])=5\cdot\Delta([5;0,3])+\Delta([0;3])=5\cdot(0\cdot\Delta(0;3)+\Delta(3;))+\Delta([0;3])=$$
> $$=5\cdot(0+1)+3=8$$

Własności mianownika $\Delta$ dla dowolnych $x\in\mathbb{Z}$, $a,b,c,d\in\mathbb{N}$:
> $\Delta(0)=1$
> $\Delta(x)=1$
> $\Delta([x;a])=a$
> $\Delta([x;a,b])=ab+1$
> $\Delta([x;a,b,c])=abc+a+c$
> $\Delta([x;a,b,c,d])=abcd+ab+ad+cd+1$
## Licznik
Licznikiem łańcucha $l\in\mathbb{L}$ nazywamy liczbę $\Gamma(l)$ gdzie $\Gamma:\mathbb{L}\rightarrow\mathbb{Z}$ jest funkcją licznikową daną
wzorem rekurencyjnym:
$$\Gamma(l)=\begin{cases}l_{0},&\lambda(l)=0\\ l_{0}+1,&\lambda(l)=1\\ l_{0}\cdot\Gamma(L_{1}(l))+\Gamma(L_{2}(l)),& \lambda(1)\ge2\end{cases}$$

**Własności operatorów**:
Zbadajmy jak oddziałują na siebie zdefiniowane dotychczas operatory. Możemy wykazać, że
zachodzą następujące własności:

**Inwolutywność odwrócenia**
$$\rho(\rho(I))=I$$

**Element neutralny złączenia**
$$l\bowtie[0;]=[0;]\bowtie l=l$$
**Brak przemienności złączenia**
$$l\bowtie m≠m\bowtie l$$
**Zerowanie się łańcucha dla złożenia $\chi\circ\tau$**
$$\chi(\tau(l))=\tau(\chi(l))=0$$
**Łączność złączenia**
$$(l \bowtie m)\bowtie n=l\bowtie(m\bowtie n)$$
**Składanie przycięć**
$$L_{a}(L_{b}(l))=L_{a+b}(l)$$
$$R_{a}(R_{b}(l))=R_{a+b}(l)$$

**Mieszanie przycięć**
$$L_{a}(R_{b}(l))=R_{b}(L_{a}(l))$$

**Rozkład łańcuchów**
$$l=\chi(l)\bowtie\tau(l)$$
**Odwrócenie ogona**
$$\tau(\rho(l))=\rho(\tau(l))$$
**Złączenie całkowite odwrotności**
$$\rho(l\bowtie m)=\rho(m)\bowtie\rho(l)$$
>[!danger] Twierdzenie o mianownik odwrócenia
>Dla dowolnego łańcucha $l\in \mathbb{L}$ zachodzi:
>$$\Delta(l)=\Delta(\rho(l))$$
>*[[Mianownik odwrócenia|Dowód]]*

> [!danger] Twierdzenie o mianowniku złączenia całkowitego
> Dla dwóch dowolnych niepustych łańcuchów $l,m\in \mathbb{L}$ zachodzi:
> $$\Delta(I\bowtie m)=\Delta(I)\cdot\Delta(m)+\Delta(R_{1}(l))\cdot\Delta(L_{1}(m))$$
## Redefinicja hipotez
Mając sformułowane podstawowe pojęcia możemy spróbować przedefiniować hipotezy Zaremby
i Pawlika nie wychodząc poza zbiór $\mathbb{L}$.
- **Hipoteza Zaremby**
$$\forall_{k\in\mathbb{N}}\exists_{z\in\mathbb{Z}^{*}}:\Delta(z)=k$$
- **Hipoteza Pawlika**
$$\forall_{k\in\mathcal{N}}\exists_{p\in\mathcal{P}^{*}}:\Delta(p)=k,\qquad \exists_{n_{0}\in\mathbb{N}} : \mathcal{N}=\set{n\in\mathbb{N} : n\geq n_{0}}$$

Niech $\mathcal{D}_{n}^{k}$ oznacza zbiór wszystkich wartości, generowanych przez funkcję $\Delta$ dla łańcuchów
właściwych o długości $n$, z przestrzeni $\mathcal{Z}_{k}^{*}$. Formalnie zbiory te definiujemy następująco:
$$\mathcal{D}_{n}^{k}=\{\Delta(l):\lambda(l)=n\wedge l\in\mathcal{Z}_{k}^{*}\}$$

Chcąc udowodnić hipotezę Zaremby musimy wykazać, że:
$$\bigcup_{n=0}^{\infty}\mathcal{D}_{n}^{5}=\mathbb{N}$$
innymi słowy, trzeba wykazać, że funkcja  $\Delta: \mathcal{Z}^{*}\rightarrow\mathbb{N}$ jest suriekcją.

Analogicznie dla hipotezy Pawlika:
$$\bigcup_{n=0}^{\infty}\mathcal{D}_{n}^{2}=\mathcal{N},\qquad\mathcal{N}=\{n\in\mathbb{N}:n\ge n_{0}\}$$
więc $\Delta:\mathcal{P}^{*}\rightarrow\mathcal{N}$ musi być suriekcją.

Liczba $n_{0}$ jest pewną stałą liczbą naturalną, powyżej której każdy nieskracalny ułamek wymierny
daje się zapisać za pomocą łańcuchów $p\in\mathcal{P}^{*}$. Zgodnie z badaniami dr Pawlika, liczba ta (o ile
istnieje) musiałaby spełniać własność $n_{0}>10^{7}$.
