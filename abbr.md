# 字体命名缩略
**abbreviate**，“缩略”，简写作abbr。不少厂商的字体后缀有统一的样式名称缩写，总结如下。

## 列表

### 厂商ID
每个字体都有、最多4字的代码。以下列出本表提及的厂商。

|ID|厂商|
| -: | :- |
|ADBE|Adobe|
|APPL|Apple|
|BITS|Bitstream|
|DAMA|Dalton Maag Ltd.|
|H&FJ|Hoefler & Frere-Jones|
|IBM |[IBM](https://github.com/IBM/plex/releases/tag/v6.0.0)|
|LINO|Linotype|
|MS|Microsoft Corp.|
|MT[^MT]|Monotype Imaging|
|REAL|Underware|
|URW |(URW)++|
|*My*|我（綿飴）编的|
|*Aa*|[AllAcronyms.com](https://www.allacronyms.com/)|

某些字体软件会自带一个厂商列表（如[NexusFont](https://github.com/MY1L/Chinese)带有`vendors.list`文件，收录388个厂）但总有新厂商出现，还有些厂商会改ID[^MT]或注册多个ID，所以列举不完的。
[这儿有微软登记的不完全列表](https://learn.microsoft.com/en-us/typography/vendors/)，注意其中有些并非厂商，也有某些代码虽有字体使用但微软不接受而未列出。

### 出典
PostScript全名的通常缀序是：字重、字宽、倾斜、视觉尺寸。

表格中若是词组，简写字数不计斜体的。标`?`的表示不确定。

#### 字重
Weight，目前我倾向于用2字简写（因为对应`font-weight`100~900齐全）

|字重|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Thin|-|Th (ADBE,LINO,DAMA)|Thn *(Aa)*|*Thin*|超细,100|
|Ultra *Light*|-|Ul *(My,Aa)*|Ult*Lt* (ADBE,LINO)|-|极细, 200,W1|
|Extra *Light*|E*L* (ADBE)|-|Ext*Lt* (IBM)|-|纤细, 200,W2|
|Light|L (ADBE,DAMA,MS)|Lt (ADBE,IBM,LINO)|Lig (URW)|Ligh (URW)|细体,300,W3|
|SemiLight|S (MS)|Sl (MS)|-|-|半细,350,W4|
|Regular/Roman|R (ADBE,DAMA,MS)|Ra *(My)*	/	Rg(ADBE)|Reg/Rom (URW)|Regu/Roma[^Ro] (URW)|常规,400[^Nl]|
|Medium|M (ADBE,DAMA,MS)|Md (ADBE,LINO)|Med (URW)|Medm (IBM)	/	Medi(URW)|中等, 500,W5|
|DemiBold|D (ADBE)|Db *(My)*	/	Sb[^Sm] (MS)|Dem (URW)|Demi/~Book~[^Bk] (URW)|半粗, 600,W6|
|Bold|B (ADBE,DAMA,MS)|Bd (ADBE,BITS,LINO,MS,MT)|Bld (IBM)	/	Bol(URW)|*Bold*|粗体,700,W7|
|Extra Bold|-|Xb *(My)*|XBd (ADBE?)|ExBd (MT)|大粗, 800,W8|
|Heavy|H (ADBE)|Hv (ADBE,LINO)|Hvy *(Aa)*|-|特粗,900|
|Black|K *(My)*|Bl (MS)|Blk (ADBE,LINO,MS)|-|超粗/黑,900|
|Extra *Black*|X*Blk* (ADBE,LINO)|Xk *(My)*|-|-|特黑,950|

##### 据[DWRITE_FONT_WEIGHT](https://learn.microsoft.com/zh-cn/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)
据称除了单独“Semi”[^zh]，视窗认同以下Preferred Subfamily（首选子族）为同一字族，字体文件夹会归拢之：
- 100 = Thin
- 200 = ExtraLight, UltraLight
- 300 = Light
- 350 = SemiLight, Demilight
- 400 = Book[^Bk], Normal[^Nl], Regular, Roman[^Ro]
- 500 = Medium
- 600 = DemiBold, Demi, SemiBold
- 700 = Bold
- 800 = ExtraBold, UltraBold
- 900 = Heavy
- 900 = Black
- 950 = ExtraBlack, UltraBlack

#### 字宽
Width，目前我倾向于用4字简写，尤其是“[Mono](https://github.com/MY1L/Ctrl#mono)”，若字体名称较长则用2字。

|字宽|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Compact|-|Ct (ADBE)|-|Cmpt *(Aa)*|窄?|
|Compressed|-|Cm (ADBE)|-|Comp (ADBE)|特窄|
|Condensed|C (DAMA)|Cn (ADBE,LINO,MT)|Con (URW)|Cond (ADBE,MT,URW)|窄,CSS属性[^Cn]用值|
|Normal|N *([Aa])*|Nl *([Aa])*|Nml *([Aa])*|Norm *([Aa])*|标准[^Nl]|
|Extended|-|Ex (ADBE,LINO)|Ext (ADBE)|Extd *(Aa)*|宽,CSS[^Cn]用的`expanded`|
|Mono|-|Mo (BITS)|Mon (URW)|*Mono*|等宽[^Mo]|
|Narrow|-|Nr (ADBE)|Nrw *(Aa)*|Nrrw *(My)*|稍窄,CSS[^Cn]用的`narrower`|
|Wide|W *(Aa)*|Wd *(Aa)*|-|*Wide*|更宽/扁? CSS[^Cn]用的`wider`|

##### 据[DWRITE_FONT_STRETCH](https://learn.microsoft.com/zh-cn/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)
据称除了“Demi~”[^zh]，视窗认同以下首选子族为字族：
- 1 = UltraCondensed
- 2 = ExtraCondensed
- 3 = Condensed
- 4 = SemiCondensed
- 6 = SemiExpanded, SemiExtended
- 7 = Expanded, Extended
- 8 = ExtraExpanded, ExtraExtended
- 9 = UltraExpanded, UltraExtended
> Normal和Medium[^Nl]的usWidthClass = 5

#### 样式
Style。不限倾斜，以下还列举了其它不便分类的样式。

|样式|1字简写|2字简写|3字简写|4字简写|说明|
| -: | :- | :- | :- | :- | :- |
|Backslant|-|Bs *(My)*|-|-|前倾(斜)体|
|Bold Italic/Oblique|Z (MS)|BI (BITS,MS)|-|-|粗斜体|
|Book|-|Bk (ADBE)|Boo (URW)|*Book*|宜读[^Bk]|
|Code|-|Cd *(Aa)*|Cod *(Aa)*|*Code*|代码/编程体[^Mo]|
|Demi~|-|Dm (ADBE)|-|*Demi*|半~,=Semi|
|Inclined|-|Ic (ADBE)|-|-|斜体?|
|Italic|I (DAMA,MS)|It (ADBE,BITS,LINO,MS)|Ita (H&FJ,URW)|Ital (URW)|意大利体[^It]|
|Kursiv|-|Ks (ADBE)|-|-|Italic(德语)|
|Nord|-|Nd (ADBE)|-|~|宽&粗[^Nd]|
|Oblique|O (LINO)|-|Obl (ADBE,LINO)|Obli (URW)|倾斜体|
|Outline|-|Ou (LINO)|-|-|轮廓/空心体|
|Poster|-|Po (ADBE)|-|-|海报?|
|Rounded|-|-|Rnd (H&FJ)|[Rond](https://github.com/MY1L/Sulfurme/releases/tag/SulfRond) *(My)*|圆体|
|Sans|-|-|San (URW)|*Sans*|无衬线|
|Semi~|-|Sm (ADBE,IBM)|-|*Semi* [^Sm]|半~,=Demi|
|Serif|-|Se (BITS)|-|-|有衬线|
|Shadow|-|-|-|Shdw *(Aa)*|空心投影|
|Slanted|-|Sl (ADBE)|-|-|倾斜体?|
|SmallCapitals|-|SC (URW)|-|SmCp (REAL)|小型大写体|
|Super|-|Su (ADBE)|-|-|超?|
|Upright *Italic*|-|Up (ADBE)|-|-|直立写意体[^It]|

##### 据[DWRITE_FONT_STYLE](https://learn.microsoft.com/en-us/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)
视窗认同以下首选子族为字族：
- Italic
- Oblique

#### 视觉尺寸
Optical Size，适用字号的单位是pt(point)，参见 [Adobe - Fonts : Type topics: Optical Size](https://web.archive.org/web/*/http://www.adobe.com/type/topics/opticalsize.html)

|尺寸|2字简写|4字词|适用字号|说明|
| -: | :- | :- | - | :- |
|Display|Ds (ADBE)|-|>24(ADBE)	/	≥20(APPL)|标题/美术字：粗细对比强、字距紧、细节更多、x字高[^x]更小|
|Subhead|Sh *(My)*|-|14~24(ADBE)|副标题：介乎 Display 和 Text|
|Text|-|*Text*|9~14(ADBE)	/	<20(APPL)|正文|
|Small(*Text*)|-|-|-|小字：介乎 Text 和 Caption ?|
|Caption|-|-|6~8(ADBE)|注脚：粗细对比弱、字距松、字形略宽|
|Opticals|Op *(Aa)*|-|-|视觉尺寸可变? Adobe后缀|

#### 其它
主要是微软特色。
|名称|简写|
| -: | :- |
|Emoji|Emj|
|Historic|His|
|Symbol|Sym|

## 备考
上述字重的说明有2种不一致的对应关系：

#### CSS3
[`font-weight`和字体名中的字重描述词给的对应关系](https://www.w3.org/TR/css-fonts-3/#font-weight-prop)
1. 100 - Thin
2. 200 - Extra Light (Ultra Light)
3. 300 - Light
4. 400 - Normal (也即Regular、Roman)
5. 500 - Medium
6. 600 - Semi Bold (Demi Bold)
7. 700 - Bold
8. 800 - Extra Bold (Ultra Bold)
9. 900 - Black (Heavy)

#### ISO
	/IEC9541-1，信息技术 字型信息交换 第1部分：体系结构，8.6.12
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
[^Bk]: “Book”表示造字者认为该字重最宜阅读，可能比常规粗也可能比常规细，只是URW恰好有某字体相当于Demi🤔
[^Cn]: CSS3 [font-stretch](https://www.w3.org/TR/css-fonts-3/#propdef-font-stretch) 属性可调整字宽。
[^It]: 我想译作“写意体”，略作“写体”，与“斜体”谐音。可见[HanItalic](https://github.com/MY1L/HanItalic)
[^Mo]: 等宽（[Monospace](https://www.w3.org/TR/css-fonts-3/#monospace)，反义词为“比例”Proportional）的不一定是打字机风（Typewriter）字体，也不一定是编程（Code）字体。同时[编程字体也可能不等宽](https://input.djr.com/)
[^MT]: Monotype Imaging曾用`AGFA`、`MT`，现在ID是`MONO`，只是为免表格过长选最短的。
[^Nd]: 1960年 Roger Excoffon 的 Antique Olive 字族最初版里的样式：大字宽、粗字重。只因Adobe字库中有这款的数字版，ADBE就把它列入缩写建议表了。这或是它唯一一次出现。
[^Ro]: URW命名比较混乱，例如其字体 Nimbus 的“Roman”实际是罗马风衬线的意思。
[^Sm]: DemiBold也常作SemiBold——所以我不用微软的简写。
[^Nl]: Normal用作字重时等同Regular，用作字宽时等同Medium。
[^x]: x字高（x-height），通俗来讲，是西文字体里小写字母斩头去尾后中间那部分的高，以`x`为典型。
[^zh]: [怎么给系统字体归类？ - 知乎](https://www.zhihu.com/question/29715469) 同一行表示视窗认为等同。

[Aa]: https://www.allacronyms.com/normal/abbreviated