# 神奇的素数

## 神奇的乘方取模(RSA算法原理)
```
32bit RSA算法
　　设A从2~(N-1) 
　　C=（A EXP D)  mod N 
　　满足如下条件： 
　　D是素数，N是两个素数(P,Q)之积， 
　　(D * E) mod ((P-1) * (Q-1))=1 
　　因为：若 
　　C=(A EXP D)mod N 
　　有： 
　　A=(C EXP E) mod N 
　　所以，C与A 一一对应。 
　　所以，对于A=2~(N-1),有不重复，无遗漏的伪随机码Ｃ

设Ｎ＝１５，Ｐ＝５，Ｑ＝３，则Ａ为２到14的数。现在要产生２到14的伪随机数。取Ｄ为３，E为３，
　　Ｃ２＝（２EXP３）mod１５ = 8,　　
　　Ｃ３＝（３EXP３）mod １５ = １２,
　　Ｃ４  ＝ （４EXP３）mod １５= ４，
　　Ｃ５  ＝ （５EXP３）mod １５= ５，
　　Ｃ６  ＝ （６EXP３）mod １５= ６，
　　Ｃ７  ＝ （７EXP３）mod １５= １３，
　　Ｃ８  ＝ （８EXP３）mod １５= ２，
　　Ｃ９  ＝ （９EXP３）mod １５= ９，
　　Ｃ１０  ＝ （１０EXP３）mod １５= １０，
　　Ｃ１１  ＝ （１１EXP３）mod １５= １１，
　　Ｃ１２  ＝ （１２EXP３）mod １５= ３，
　　Ｃ１３  ＝ （１３EXP３）mod １５= ７，
　　Ｃ１４  ＝ （１４EXP３）mod １５= １４。
```

## 线性同余算法

```
seed=(seed*prime+c)%max
只要prime跟max互质，就能产生[0,max)内不重复的序列
for i:=0;i<max;i++{
	ret:= (i*prime)%max
}
有同样的效果,只要prime跟max互质，就可以产生[0,max)内不重复的随机序列
```