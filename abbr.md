# 字体命名缩略
**abbreviate**，“缩略”，简写作abbr。不少厂商的字体有统一的缩写后缀，暂且总结如下。

## 出典

|ID|厂商|
| -: | :- |
|ADBE|Adobe|
|H&FJ|Hoefler & Frere-Jones|
|LINO|Linotype|
|URW |(URW)++|

----

|原文|1字简写|2字简写|3字简写|4字简写|注释|
| -: | :- | :- | :- | :- | :- |
|Compressed|-|-|-|Comp (ADBE)|极窄|
|Condensed|-|Cn (ADBE,LINO)|Con (URW)|Cond (ADBE,URW)|窄|
|Extended|-|Ex (LINO)|Ext (ADBE)|-|宽,≈CSS3的expanded|
|Italic|-|It (ADBE,LINO)|Ita (H&FJ,URW)|Ital (URW)|意大利体|
|Mono|-|-|-|*Mono*|等宽|
|Oblique|O (LINO)|-|Obl (LINO)|Obli (URW)|倾斜体|
|Outline|-|Ou (LINO)|-|-|空心|
|Rounded|-|-|Rnd (H&FJ)|-|圆体|
|Semi|-|-|-|*Semi*|半~|
|Thin|-|Th (LINO)|-|*Thin*|极细,100|
|Ultra *Light*|-|-|Ult*Lt* (LINO)|-|特细,200,W1|
|Extra *Light*|E*L* (ADBE)|-|-|-|特细,200,W2|
|Light|L (ADBE)|Lt (LINO)|Lig (URW)|Ligh (URW)|细,300,W3|
|Regular/Roman|R (ADBE)|-|Reg (URW)|Regu/Roma (URW)|常规,400|
|Medium|M (ADBE)|Md (LINO)|Med (URW)|Medi (URW)|中粗,500,W5|
|DemiBold|D (ADBE)|-|Dem (URW)|Demi/Book (URW)|半粗,600,W6|
|Bold|B (ADBE)|Bd (LINO)|Bol (URW)|*Bold*|粗,700,W7|
|Black|-|-|Blk (LINO)|-|特粗/黑,900|
|Heavy|H (ADBE)|Hv (LINO)|-|-|特粗,900|
|Extra *Black*|X*Blk* (LINO)|-|-|-|特黑,1000?|

## 备注
[CSS3为`font-weight`和字体名中的字重描述词给的对应关系表](https://www.w3.org/TR/css-fonts-3/#font-weight-prop)
1. 100 - Thin
2. 200 - Extra Light (Ultra Light)
3. 300 - Light
4. 400 - Normal，我记得相当于Regular、Book(?)、Roman
5. 500 - Medium
6. 600 - Semi Bold (Demi Bold)
7. 700 - Bold
8. 800 - Extra Bold (Ultra Bold)
9. 900 - Black (Heavy)

ISO/IEC9541-1，信息技术 字型信息交换 第1部分：体系结构，8.6.12：
- 0 不用
- 1 → ultra light
- 2 → extra light
- 3 → light
- 4 → semilight
- 5 → medium
- 6 → semi bold
- 7 → bold
- 8 → extra bold
- 9 → ultra bold