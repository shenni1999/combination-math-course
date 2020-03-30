# 参考答案

## 组合作业2
1.学校有100名学生和3个宿舍A,B和C，它们分别容纳25、35和40人。\
(1)为学生安排宿舍有多少种方法；\
(2)设100个学生中有50名男生和50名女生，而宿舍A是全男生宿舍，宿舍B是全女生宿舍，宿舍C男女兼收。有多少种方法可为学生安排宿舍？
>答：(1)因为学生数与宿舍总容纳数刚好相等，所以共有
>$$C^{25}_{100}C^{35}_{75}C^{40}_{40}=C^{25}_{100}C^{35}_{75}种方法。$$
>   (2)先在50名男生种选择25人住宿舍A，然后在50名女生中选择35人住宿舍B，剩下的人全住宿舍C。故有
>$$ C^{25}_{50}C^{35}_{50}种方法。 $$
\
2.求$1\sim n$的满足下列性质的全排列的个数，在每个数$i$后（不一定紧随）一定有数$i+1$或者$i-1$(例如，1432满足，但2431不满足此性质)。
>答：设$i_1,i_2,\dots,i_n$是符合此性质的一个排列。
>则$i_1$只能是$1$或者$n$,若$i_1=1$，则$i_2$只能是$2$或者$n-2$,若$i_2=2$，则$i_3$只能是$3$或者$n-3$,$\cdots$;若$i_2=n$，则$i_3$只能是$n-1$或者$2$,$\cdots$，若$i_1=n$，可作类似讨论，注意到每个位置均为两种选择方案，所以
>$$全排列的个数为2^{n-1}$$
\
3.方程$x_1+x_2+x_3+x_4=30$有多少满足$x_1\geq 2,x_3\geq -5 ,x_4\geq 8$的整数解？
> 答：令$y_1=x_1-2,y_2=x_2,y_3=x_3+5,y_4=x_4-8$，则
>  $$y_1+y_2+y_3+y_4=(x_1+x_2+x_3+x_4)-2+0+5-8=25$$
> 且$y_i$均是非负整数，每一组关于$x_i$的解对应一组关于$y_i$的解$(i=1,\cdots,4)$,而方程$y_1+y_2+y_3+y_4=25$的解的个数为$F(4,25)=C(28,25)=3276$

\
4.考虑大小为$3n+1$的多重集$\{n*a,n*b,1,2,3,\cdots ,n+1\}$,确定它的$n-$组合数。
>答：相当于从$n$个$a$，从$n$个$b$以及$1,2,\cdots,n+1$共$3n+1$个数种选n个。将每个$a$和每个$b$都看做不同的元素，则$n-$组合数为$C(3n+1,n)$。\
>如果看成相同的元素则有 
>$$\sum_{k=0}^nF(2,k)C(n+1,n-k)=\sum_{k=0}^{k+1}\begin{pmatrix}n+1\\ k \end{pmatrix}=\sum_{k=1}^{k+1}k\begin{pmatrix}n+1\\ k \end{pmatrix}=(n+1)\cdot 2^n$$

\
5.求能除尽1400的正整数数目（1除外），其中包含多少个奇数？
>答：$1400=2^3\times5^2\times 7$
>能除尽1400的正整数必为$2^m\times 5^n\times 7$，其中$0\leq m\leq 3,0\leq n\leq 2,0\leq l \leq 1$。所以有$C^1_4C^1_3C^1_2-1=23$个，其中奇数为$m=0$时，有$C^1_3C^1_2-1=5$个，所以能除尽1400的正整数个数为23，包含5个奇数。

\
6.求5位数中至少出现一个6，而被3整除的数的个数。
>答：五位数中被3整除的有$\frac{99999}{3}-\frac{9999}{3}=30000$个\
五位数中不含6，但是能被整除的有\
（1）十位数的选择，$C_9^1$。\
（2）百位数，$C_9^1$。\
（3）千位数，$C_9^1$。\
（4）万位数，$C_8^1$。\
记万位数+千位数+百位数+十位数除3的余数为x。则
>$$  \Biggr\{ \begin{aligned} &若x=0，则个位数的选择有三个，\\ &若x=1，则个位数有2，5，8三个选择\\&若x=2，则个位数有1，4，7，三个选择。 \end{aligned}$$
>则五位数中至少出现一个6且能够被3整除的个数为 
> $$30000-C_8^1C_9^1C_9^1C_9^1C_3^1=12504$$

\
7.证明：对$n\in \mathbb{N}，\sum_{k=0}^{n}C^2(n,k)=C(2n,n)$。
>答：由范德蒙德等式，令
>$$ \sum_{k=0}^rC(m,k)C(n,r-k)=C(m+n,r)$$
>其中令$m=n,r=n$，满足
> $$r\leq min(m,n)$$
>  则上式变为
> $$\sum_{k=0}^nC(n,k)C(n,n-k)=C(2n,n)$$
> 也就是
> $$\sum_{k=0}^{n}C^2(n,k)=C(2n,n)。$$

\
8.证明对于$p,q\in N,\sum_{k=0}^pC(p,k)C(q,k)C(n+k,p+q)=C(n,p)C(n,q)$。
> 答：
> $$ \begin{aligned} &C(n,p)C(n,q)=C(n,q)\sum_{k=0}^pC(n-q,k)C(q,n-k)\\=&\sum_{k=0}^pC(q,p-k)C(n,q)C(n-q,k)\\=&\sum_{k=0}^pC(q,p-k)C(q+k,k)C(n,q+k)\\=&\sum_{k=0}^pC(p,k)C(q+k,p)C(n,q+k)\\=&\sum_{k=0}^pC(p,k)C(q,k)\sum_{j=0}^pC(n,q+j)C(k,p-j) \\=&\sum_{k=0}^pC(p,k)C(q,k)C(n+k,p+q)\end{aligned}$$

\
9.证明：对于 $n,m \in \mathbb{N},\sum^n_{k=0}(-1)^{k+m}C(n,k)C(k,m)=\bigg\{ \begin{aligned}1,n=m\\ 0 ,n\not = m \end{aligned}$
>答：（1）若$n<m$时，则$k<n<m$,则$C(k,m)\equiv 0$\
(2)若$n>m$时，有 
>$$\sum_{k=0}^n(-1)^{k+m}C(n,k)C(k,m)=\sum _{k=m}^n(-1)^{k+m}C(n,k)C(k,m)$$
>由于
>$$\begin{aligned}\begin{pmatrix}n\\k\end{pmatrix}\begin{pmatrix}k\\m\end{pmatrix}&=\frac{n!}{m!(n-k)!(k-m)!}\\\begin{pmatrix}n-m\\k-m\end{pmatrix}&=\frac{(n-m)!}{(n-k)!(k-m)!}\\\begin{pmatrix}n\\k\end{pmatrix}\begin{pmatrix}k\\m\end{pmatrix}&=\frac{n!}{m!(n-m)!}\begin{pmatrix}n-m\\k-m\end{pmatrix} =\begin{pmatrix}n\\m\end{pmatrix} \begin{pmatrix}n-m\\k-m\end{pmatrix} \end{aligned}$$
>所以
>$$
\begin{aligned}
&\sum_{k=m}^n(-1)^{k+m}C(n,k)C(k,n)\\
=&\begin{pmatrix}n\\m\end{pmatrix}\sum_{k=m}^n(-1)^{k+m}\begin{pmatrix}n-m\\k-m\end{pmatrix}\\
=&\begin{pmatrix}n\\m\end{pmatrix}\sum_{k=m}^n(-1)^{k}\begin{pmatrix}n-m\\k\end{pmatrix}
\end{aligned}$$
>又有
>$$ (1-x)^{n-m}=\sum_{k=0}^{n-m}(-1)^k\begin{pmatrix}n-m\\k\end{pmatrix}$$
>带入$x=1$,得到$\sum_{k=0}^{n-m}(-1)^k\begin{pmatrix}n-m\\k\end{pmatrix}=0$,所以$n>m$时，$\sum_{k=0}^n(-1)^{k+m}C(n,k)C(k,m)=0$。
\
(3)$m=n$时，
>$$\begin{aligned}
&\sum_{k=0}^n(-1)^{k+m}C(n,k)C(k,m)\\
=&\sum_{k=0}^n(-1)^{k+m}C(n,k)C(k,n)\\
=&(-1)^{n+n}C(n,n)C(n,n)\\
=&1
\end{aligned}$$
>综上，得证。
## 组合作业3
1.
>答：因为$11^2=121$，所以不超过120的合数，必为2，3，5，7的倍数，且不超过120的合数的因子不可能超过11。\
设$A_i$为不超过120的数i的倍数集，$i=2,3,5,7$，有
>$$|A_2|=[\frac{120}{2}]=60,|A_3|=[\frac{120}{3}]=40,|A_5|=[\frac{120}{5}]=24,|A_7|=[\frac{120}{7}]=17,$$
>$$|A_2\cap A_3|=[\frac{120}{6}]=20,|A_3\cap A_5|=[\frac{120}{15}]=8,|A_5\cap A_2|=[\frac{120}{10}]=12,$$
>$$|A_7\cap A_2|=[\frac{120}{14}]=8,|A_7\cap A_3|=[\frac{120}{21}]=5,|A_7\cap A_5|=[\frac{120}{35}]=3,$$
>$$|A_2\cap A_3 \cap A_5|=4,|A_2\cap A_3 \cap A_7|=2,|A_2\cap A_5 \cap A_7|=1$$
>$$\begin{aligned}|&\overline{A_2\cup A_3\cup A_5\cup A_7}|\\&=120-\sum_{i=2,3,5,7}|A_i|+\sum_{i,j=2,3,4,7,i\not ={j}}|A_i\cap A_j|-\sum_{i,j,k=2,3,5,7,i\not ={j}\not ={{k}}}|A_i\cap A_j\cap A_k|\\&+|A_2\cap A_3\cap A_5 \cap A_7|=27\end{aligned}$$
>有因为排除了2，3，5，7，多算了1所以素数个数为$27+4-1=30$个。

\
2.
>答:设集合A为能被5整除的数，集合B为能被6整除的数，集合C为能被8整除的数，集合S为1~1000的所有数，
>$$\begin{aligned}&|A|=[\frac{1000}{5}]=200,|B|=[\frac{1000}{6}]=166,|C|=[\frac{1000}{8}]=125\\ 
&|A\cap B|=[\frac{1000}{30}]=33,|A\cap B|=[\frac{1000}{40}]=25,|A\cap B|=[\frac{1000}{24}]=41\\
&|A\cap B\cap C|=[\frac{1000}{24\times 5}]=8\\
&|\overline{A\cup B\cup C}|=|S|-|A|-|B|-|C|+|A\cap B|+|A\cap C|+|B\cap C|-|A\cap B\cap C|\\
&=600个
\end{aligned}$$

\
3.
>答:集合S为甲班全部学生，$|S|=60$。设集合A-喜爱数学，B-喜爱物理，C-喜爱化学的学生集合。则
>$$\begin{aligned}&|A|=24,|B|=28,|C|=26,|A\cap B|=10,|A\cap C|=8,|B\cap C|=14,\\ &|A\cap B\cap C|=6\end{aligned}$$
>所以对于三门学科都不喜爱，即
>$$|\overline{A\cup B\cup C}|=|S|-|A|-|B|-|C|+|A\cap B|+|A\cap C|+|B\cap C|-|A\cap B\cap C|\\=8个$$

\
4.
>答：设集合S为8个字母的全排列组合的集合$|S|=8!$\
>设$A_i$分别为$A,C,E,G$这四个字母在原来位置上的排列的集合，$i=1,2,3,4$
>$$|A_i|=7!,|A_i\cap A_j|=6!,|A_i\cap A_j\cap A_k|=5!,|A_i\cap A_j\cap A_k\cap A_l|=4!,$$
>所求的排列数为
>$$|\overline{A\cup B\cup C}|=|S|-C(4,1)7!+C(4,2)6!-C(4,3)5!+4!\\=24024个$$

\
5.
>答：$C(n,r)D_{n-r}$

\
6.
>答:设n名儿童全部的座位排列组合集合S，$|S|=(n-1)!$\
令$P_i$表示第i名儿童前面的儿童和原来一样的座位排列方式，即有$i(i+1)$的形式。\
$P_n$表示$n!$的形式。\
令$A_i(i=1,2,\cdots ,n)$表示S中具有性质$P_i$的元素组成的集合。则$|\overline{A_1\cup A_2\cup \cdots \cup A_n}|$为所求。由容斥原理有
>$$|\overline{A_1\cup A_2\cup \cdots \cup A_n}|=(n-1)!-\begin{pmatrix}n\\1\end{pmatrix}(n-2)!+\begin{pmatrix}n\\2\end{pmatrix}(n-3)!+\cdots +(-1)^n\begin{pmatrix}n\\n\end{pmatrix}
$$

\
7.
>答：A={a,b,c,d,e,f,g,h}\
设集合S是A的全排列构成的集合$|S|=8!$\
设集合M是出现了abc的A的全排列的集合$|M|=6!$\
设集合N是出现了efgh的A的全排列的集合$|N|=5!$\
且$|M\cap N|=3!$
>$$|\overline{M\cup N}|=|S|-|M|-|N|+|M\cap N|=39486
$$

