# 字体命名缩略
**abbreviate**，“缩略”，简写作abbr。不少厂商的字体有统一的样式名称缩写后缀，暂且总结如下。

## 列表

### 厂商ID
每个字体都有、最多4字的代码。
|ID|厂商|
| -: | :- |
|ADBE|Adobe|
|BITS|Bitstream|
|DAMA|Dalton Maag Ltd|
|H&FJ|Hoefler & Frere-Jones|
|IBM |[IBM](https://github.com/IBM/plex/releases/tag/v6.0.0)|
|LINO|Linotype|
|URW |(URW)++|
|*MY*|我（綿飴）编的|

### 出典
如果是词组，简写字数不计斜体的。标`?`的表示不确定。
目前我倾向于字重用2字简写（因为对应`font-weight`100~900齐全）
|字重|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Thin|-|Th (ADBE,LINO,DAMA)|-|*Thin*|极细,100|
|Ultra *Light*|-|Ul *(MY)*|Ult*Lt* (ADBE,LINO)|-|特细,200,W1|
|Extra *Light*|E*L* (ADBE)|-|Ext*Lt* (IBM)|-|特细,200,W2|
|Light|L (ADBE,DAMA)|Lt (ADBE,IBM,LINO)|Lig (URW)|Ligh (URW)|细,300,W3|
|Regular/Roman|R (ADBE,DAMA)|Ra *(MY)*	/	Rg(ADBE)|Reg/Rom (URW)|Regu/Roma[^Ro] (URW)|常规,400|
|Medium|M (ADBE,DAMA)|Md (ADBE,LINO)|Med (URW)|Medm (IBM)	/	Medi(URW)|中粗,500,W5|
|DemiBold|D (ADBE)|Db *(MY)*|Dem (URW)|Demi/Book[^Db] (URW)|半粗,600,W6|
|Bold|B (ADBE,DAMA)|Bd (ADBE,BITS,LINO)|Bld (IBM)	/	Bol(URW)|*Bold*|粗,700,W7|
|Extra Bold|-|Xb *(MY)*|XBd (ADBE?)|-|特粗,800,W8|
|Black|K *(MY)*|-|Blk (ADBE,LINO)|-|极粗/黑,900|
|Heavy|H (ADBE)|Hv (ADBE,LINO)|-|-|极粗,900|
|Extra *Black*|X*Blk* (ADBE,LINO)|Xk *(MY)*|-|-|特黑,1000?|

|字宽|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Compact|-|Ct (ADBE)|-|-|窄?|
|Compressed|-|Cm (ADBE)|-|Comp (ADBE)|特窄?|
|Condensed|C (DAMA)|Cn (ADBE,LINO)|Con (URW)|Cond (ADBE,URW)|窄|
|Extended|-|Ex (ADBE,LINO)|Ext (ADBE)|-|宽,≈CSS3的expanded|
|Mono|-|Mo (BITS)|Mon (URW)|*Mono*|等宽[^Mo]|
|Narrow|-|Nr (ADBE)|-|-|稍窄?|

|样式|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Backslant|-|Bs *(MY)*|-|-|前倾体|
|Bold Italic/Oblique|-|BI (BITS)|-|-|粗斜体|
|Book|-|Bk (ADBE)|-|-|书版?|
|Demi~|-|Dm (ADBE)|-|*Demi*|半~,=Semi|
|Display|-|Ds (ADBE)|-|-|视觉尺寸之一|
|Inclined|-|Ic (ADBE)|-|-|斜体?|
|Italic|I (DAMA)|It (ADBE,BITS,LINO)|Ita (H&FJ,URW)|Ital (URW)|意大利体[^It]|
|Kursiv|-|Ks (ADBE)|-|-|德语Italic|
|Nord|-|Nd (ADBE)|-|-|宽&粗[^Nd]|
|Oblique|O (LINO)|-|Obl (ADBE,LINO)|Obli (URW)|倾斜体|
|Outline|-|Ou (LINO)|-|-|空心/轮廓|
|Poster|-|Po (ADBE)|-|-|视觉尺寸之一?|
|Rounded|-|-|Rnd (H&FJ)|Rond *(MY)*|圆体|
|Sans|-|-|San (URW)|*Sans*|无衬线|
|Semi~|-|Sm (ADBE,IBM)|-|*Semi*|半~[^Sm],=Demi|
|Serif|-|Se (BITS)|-|-|有衬线|
|Slanted|-|Sl (ADBE)|-|-|倾斜体?|
|Super|-|Su (ADBE)|-|-|超?|
|Upright|-|Up (ADBE)|-|-|直立(意大利体)|


## 备考
上述字重的说明有2种不一致的对应关系：

#### [CSS3为`font-weight`和字体名中的字重描述词给的对应关系](https://www.w3.org/TR/css-fonts-3/#font-weight-prop)
1. 100 - Thin
2. 200 - Extra Light (Ultra Light)
3. 300 - Light
4. 400 - Normal（相当于Regular、Roman）
5. 500 - Medium
6. 600 - Semi Bold (Demi Bold)
7. 700 - Bold
8. 800 - Extra Bold (Ultra Bold)
9. 900 - Black (Heavy)

#### ISO/IEC9541-1，信息技术 字型信息交换 第1部分：体系结构，8.6.12
- 0 不用
- 1 → ultra light
- 2 → extra light
- 3 → light
- 4 → semi light
- 5 → medium
- 6 → semi bold
- 7 → bold
- 8 → extra bold
- 9 → ultra bold
> 常见于日本厂商字体的“W1~9”后缀对应关系，比较过时。

### 注释
[^It]: 我曾想译作“写意体”，略作“写体”，与“斜体”谐音。可见[HanItalic](https://github.com/MY1L/HanItalic)
[^Mo]: 等宽（Monospace）的不一定是打字机风字体，也不一定是编程字体。在满足对齐的情况下，[编程字体也可能不等宽](https://input.djr.com/)。
[^Db]: DemiBold也常作Semibold。“Book（书版）”有视觉尺寸（Optical Size）的意味，可能比常规粗也可能比常规细，只是URW恰好有某字体相当于Demi……
[^Sm]: 对照CSS3，我猜“Semi Light”会不会等于Normal(400)，或Normal与Light之间(350)？也许用不上这个词🤔
[^Ro]: URW命名有许多例外，其Nimbus字体的Roman实际是罗马衬线体的意思。
[^Nd]: 1960年 Roger Excoffon 的 Antique Olive 字体家族最初发布版本中的字重，大字宽、粗字重。因为Adobe字体库中有这款字体的数字版本，Adobe就把它列入建议缩写名单了。这可能是它唯一一次出现。