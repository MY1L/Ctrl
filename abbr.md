# 字体命名缩略
**abbreviate**，“缩略”，简写作abbr。不少厂商的字体后缀有统一的样式名称缩写，总结如下。

## 列表

### 厂商ID
每个字体都有、最多4字的代码。某些字体软件会自带一个厂商列表（如[NexusFont](https://github.com/MY1L/Chinese)就带有`vendors.list`文件，收录388个厂）

|ID|厂商|
| -: | :- |
|ADBE|Adobe|
|APPL|Apple|
|BITS|Bitstream|
|DAMA|Dalton Maag Ltd|
|H&FJ|Hoefler & Frere-Jones|
|IBM |[IBM](https://github.com/IBM/plex/releases/tag/v6.0.0)|
|LINO|Linotype|
|MONO|Monotype Imaging|
|REAL|Underware|
|URW |(URW)++|
|*MY*|我（綿飴）编的|
|*AA*|[All Acronyms](https://www.allacronyms.com/)|

### 出典
PostScript全名的通常缀序是：字重、字宽、倾斜、视觉尺寸。

表格中若是词组，简写字数不计斜体的。标`?`的表示不确定。

目前我倾向于字重用2字简写（因为对应`font-weight`100~900齐全）

|字重|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Thin|-|Th (ADBE,LINO,DAMA)|-|*Thin*|极细,100|
|Ultra *Light*|-|Ul *(MY)*|Ult*Lt* (ADBE,LINO)|-|特细, 200,W1|
|Extra *Light*|E*L* (ADBE)|-|Ext*Lt* (IBM)|-|特细, 200,W2|
|Light|L (ADBE,DAMA)|Lt (ADBE,IBM,LINO)|Lig (URW)|Ligh (URW)|细,300,W3|
|Regular/Roman|R (ADBE,DAMA)|Ra *(MY)*	/	Rg(ADBE)|Reg/Rom (URW)|Regu/Roma[^Ro] (URW)|常规,400|
|Medium|M (ADBE,DAMA)|Md (ADBE,LINO)|Med (URW)|Medm (IBM)	/	Medi(URW)|中粗, 500,W5|
|DemiBold[^Sm]|D (ADBE)|Db *(MY)*|Dem (URW)|Demi/~Book~[^Bk] (URW)|半粗, 600,W6|
|Bold|B (ADBE,DAMA)|Bd (ADBE,BITS,LINO,MONO)|Bld (IBM)	/	Bol(URW)|*Bold*|粗,700,W7|
|Extra Bold|-|Xb *(MY)*|XBd (ADBE?)|ExBd (MONO)|特粗, 800,W8|
|Black|K *(MY)*|Bk *(AA)*|Blk (ADBE,LINO)|-|极粗/黑,900|
|Heavy|H (ADBE)|Hv (ADBE,LINO)|Hvy *(AA)*|-|极粗,900|
|Extra *Black*|X*Blk* (ADBE,LINO)|Xk *(MY)*|-|-|特黑,1000?|

|字宽|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Compact|-|Ct (ADBE)|-|-|窄?|
|Compressed|-|Cm (ADBE)|-|Comp (ADBE)|特窄|
|Condensed|C (DAMA)|Cn (ADBE,LINO,MONO)|Con (URW)|Cond (ADBE,MONO,URW)|窄,CSS属性[^Cn]用值|
|Normal|N *([AA])*|-|-|Norm *([AA])*|常规[^Sm]|
|Extended|-|Ex (ADBE,LINO)|Ext (ADBE)|-|宽,CSS3[^Cn]用的`expanded`|
|Mono|-|Mo (BITS)|Mon (URW)|*Mono*|等宽[^Mo]|
|Narrow|-|Nr (ADBE)|Nrw *(AA)*|-|稍窄,CSS[^Cn]用的`narrower`|
|Wide|-|-|-|*Wide*|更宽/扁? CSS[^Cn]用的`wider`|

|样式|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Backslant|-|Bs *(MY)*|-|-|前倾(斜)体|
|Bold Italic/Oblique|-|BI (BITS)|-|-|粗斜体|
|Book|-|Bk (ADBE)|Boo (URW)|*Book*|书版?[^Bk]|
|Code|-|-|-|*Code*|代码/编程体[^Mo]|
|Demi~|-|Dm (ADBE)|-|*Demi*|半~,=Semi|
|Inclined|-|Ic (ADBE)|-|-|斜体?|
|Italic|I (DAMA)|It (ADBE,BITS,LINO)|Ita (H&FJ,URW)|Ital (URW)|意大利体[^It]|
|Kursiv|-|Ks (ADBE)|-|-|Italic(德语)|
|Nord|-|Nd (ADBE)|-|~|宽&粗[^Nd]|
|Oblique|O (LINO)|-|Obl (ADBE,LINO)|Obli (URW)|倾斜体|
|Outline|-|Ou (LINO)|-|-|轮廓/空心体|
|Poster|-|Po (ADBE)|-|-|海报?|
|Rounded|-|-|Rnd (H&FJ)|Rond *(MY)*|圆体|
|Sans|-|-|San (URW)|*Sans*|无衬线|
|Semi~|-|Sm (ADBE,IBM)|-|*Semi* [^Sm]|半~,=Demi|
|Serif|-|Se (BITS)|-|-|有衬线|
|Shadow|-|-|-|Shdw *(AA)*|空心投影|
|Slanted|-|Sl (ADBE)|-|-|倾斜体?|
|SmallCapitals|-|SC (URW)|-|SmCp (REAL)|小型大写体|
|Super|-|Su (ADBE)|-|-|超?|
|Upright *Italic*|-|Up (ADBE)|-|-|直立写意体[^It]|

|尺寸[^Os]|2字简写|4字词|适用字号|说明|
| -: | :- | :- | - | :- |
|Display|Ds (ADBE)|-|>24(ADBE)	/	≥20(APPL)|标题/美术字：粗细对比强、字距紧、细节更多、x字高[^x]更小|
|Subhead|-|-|14~24(ADBE)|副标题：介乎 Display 和 Text|
|Text|-|*Text*|9~14(ADBE)	/	<20(APPL)|正文|
|Small(*Text*)|-|-|-|小字：介乎 Text 和 Caption ?|
|Caption|-|-|6~8(ADBE)|注脚：粗细对比弱、字距松、字形略宽|
|Opticals|Op *(AA)*|-|-|视觉尺寸可变? Adobe后缀|


## 备考
上述字重的说明有2种不一致的对应关系：

#### [CSS3为`font-weight`和字体名中的字重描述词给的对应关系](https://www.w3.org/TR/css-fonts-3/#font-weight-prop)
1. 100 - Thin
2. 200 - Extra Light (Ultra Light)
3. 300 - Light
4. 400 - Normal (也即Regular、Roman)
5. 500 - Medium
6. 600 - Semi Bold (Demi Bold)
7. 700 - Bold
8. 800 - Extra Bold (Ultra Bold)
9. 900 - Black (Heavy)

#### ISO/IEC9541-1，信息技术 字型信息交换 第1部分：体系结构，8.6.12
> 常见于日本厂商字体的“W1~9”后缀对应关系，比较过时。
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

### 注释
[^It]: 我想译作“写意体”，略作“写体”，与“斜体”谐音。可见[HanItalic](https://github.com/MY1L/HanItalic)
[^Mo]: 等宽（[Monospace](https://www.w3.org/TR/css-fonts-3/#monospace)，反义词为“比例”Proportional）的不一定是打字机风（Typewriter）字体，也不一定是编程（Code）字体。同时[编程字体也可能不等宽](https://input.djr.com/)
[^Bk]: “Book（书版）”或有视觉尺寸的意味，可能比常规粗也可能比常规细，只是URW恰好有某字体相当于Demi……
[^Cn]: CSS3 [font-stretch](https://www.w3.org/TR/css-fonts-3/#propdef-font-stretch) 属性可调整字宽。
[^Sm]: DemiBold也常作Semibold。对照CSS3，我猜“Semi Light”会不会等于Normal(400)，或Normal与Light之间(350)？也许这词用不上🤔
[^Ro]: URW命名比较混乱，例如其字体 Nimbus 的“Roman”实际是罗马风衬线的意思。
[^Nd]: 1960年 Roger Excoffon 的 Antique Olive 字族最初版里的样式：大字宽、粗字重。只因Adobe字库中有这款的数字版，ADBE就把它列入缩写建议表了。这或是它唯一一次出现。
[^Os]: 视觉尺寸（Optical Size），适用字号的单位是pt(point)，参见 [Adobe - Fonts : Type topics: Optical Size](https://web.archive.org/web/*/http://www.adobe.com/type/topics/opticalsize.html)
[^x]: x字高（x-height），通俗来讲，是西文字体里小写字母斩头去尾后中间那部分的高，以`x`为典型。

[AA]: https://www.allacronyms.com/normal/abbreviated