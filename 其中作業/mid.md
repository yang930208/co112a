# 計算機結構學習筆記
## **基本電路閘程式學習**
### NOT
使用 NAND 可做出 NOT 的效果
### AND
使用 NAND 和 NOT 可做出 AND 的效果
### OR
使用2個 NOT 和 1個 NAND 可做出 OR 的效果
### XOR
使用 NOT 、 AND 和 OR 做出 XOR (兩者相同為1，不同為0)的效果
### MUX
使用 Not 、 And 、 Or 做出多工器 MUX (多個輸入，一個輸出的閘)
### DMUX
使用 Not 、 And 做出 DMUX (反多工器)
## **進階電路閘程式學習**
### NOT16
NOT 的 in[0] ~ in[15]
### AND16
AND 的 in[0] ~ in[15]
### OR16
OR 的 in[0] ~ in[15]
### MUX16
MUX 的 in[0] ~ in[15] 和 16個sel
### OR8WAY
使用7個 OR，並一階一階往下
Or(a=in[0], b=in[1], out=a);
    Or(a=a, b=in[2], out=b);
    Or(a=b, b=in[3], out=c);...
### MUX4WAY16
使用 MUX16 製作，in的a、b、c、d是0~15，分別跟sel=0作用，最後再與sel=1重複一次
### MUX8WAY16
用 MUX16 做七次，分成三部分，先做四次 sel=0，再做兩次 sel=0，再做一次 sel=0
### DMUX4WAY
和 MUX4WAY16 相似，差在輸出入的數量和sel的變化
### DMUX8WAY
和 MUX8WAY16 相似，差在輸出入的數量和sel的變化
## **進階功能製作**
### Halfadder(半加器)
使用 1個 XOR 和 1個 AND 組成
### Falladder(全加器)
使用 2個 Halfadder 和1個 OR 組成
### ADD16
先用1個 Halfadder(半加器) 做出一個進位，再把進位的值放到下一個 Falladder(全加器)裡面重複做15次
### INC16
使用 ADD16 輸入 a[0]~a[15] 和 b[0]=ture，做15次
### ALU
使用MUX(多工器)製作，用各種邏輯閘依照題目完成對應的功能
