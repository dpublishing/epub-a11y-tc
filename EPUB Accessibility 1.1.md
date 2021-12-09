# EPUB無障礙輔助性 1.1
EPUB出版品的適用性與發現性規定

W3C工作草稿 01 October 2021

本版本：

https://www.w3.org/TR/2021/WD-epub-a11y-11-20211001/

最新發佈版本：

https://www.w3.org/TR/epub-a11y-11/

最新編輯草稿：

https://w3c.github.io/epub-specs/epub33/a11y/

前一版本：

https://www.w3.org/TR/2021/WD-epub-a11y-11-20210929/

編輯者：

Matt Garrish (DAISY Consortium)
George Kerscher (DAISY Consortium)
Charles LaPierre (Benetech)
Gregorio Pellegrino (Fondazione LIA)
Avneesh Singh (DAISY Consortium)

參與協助：

GitHub w3c/epub-specs

提出問題
版本紀錄
修改要求

Copyright © 2017-2021 W3C® (MIT, ERCIM, Keio, Beihang). W3C liability, trademark and permissive document license rules apply.

<hr />

## 概要

本規格指定了用來驗證EPUB出版品無障礙輔助性的內容適用性規定。也同時指定了供EPUB出版品發現性使用的無障礙輔助性詮釋資料規定。

## 本文件狀態

本章節解釋了本文件在其發表時的狀態。其他文件可能取代本文件。W3C的當前出版品清單以及本技術報告的最新版本可於位在https://www.w3.org/TR/之W3C技術報告索引中獲得。

###### 編輯註解

目前沒有製作具無障礙輔助性內容的出版社，在本規格尚在制訂發展時，建議可以更新其產製流程以符合[EPUB-A11Y-10]的規定。符合該版本規定的內容，基本上僅需一些必要的變更，就可以符合本規格之規定。

本文件由EPUB 3工作小組發布為工作草稿。本文件預計將成為W3C推薦規格。

推薦使用GitHub Issues對本規格進行討論。此外，你也可以將意見寄送到我們的郵寄列表。請寄送到public-epub3@w3.org（訂閱，存檔）。

所發表的工作草稿不代表受到所有W3C會員所支持。

本文件為草稿，而且可能會隨時會被其他文件更新、取代、淘汰。編輯作業尚未完成前，不適宜引用本文件。

本文件由基於W3C專利政策下運作的一個小組所製作。W3C維護了一份與該小組交付成果有關的任何專利披露公開清單，該頁面也包含了專利披露的說明。任何人若實際擁有某項專利知識並相信其包含該專利之主要申請範圍，則必須依照W3C專利政策第六節之規定揭露該訊息。

本文件受2020年9月15日W3C流程文件所規範。

##  目錄

概要
本文件狀態

1. 導論
1.1 概要
1.2 有效技巧
1.2.1 國際化
1.3 適用於舊版規格
1.4 術語
1.5 適用性
2. 發現性
2.1 導論
2.2 包裝詮釋資料
2.3 連結的詮釋資料紀錄
3. 無障礙出版品
3.1 導論
3.2 與WCAG之關係
3.3 WCAG適用性
3.3.1 WCAG適用性規定
3.3.2 評量WCAG適用性
3.3.2.1 頁面與出版品Page and Publication
3.3.2.2 應用適用性規範
3.4 EPUB規定
3.4.1 Page導覽
3.4.1.1 概論
3.4.1.2 可應用性
3.4.1.3 目標
3.4.1.3.1 分頁來源
3.4.1.3.2 頁面列表
3.4.1.3.3 分頁點
3.4.2 媒體覆蓋播放
3.4.2.1 概論
3.4.2.2 可應用性
3.4.2.3 目標
3.4.2.3.1 完整性
3.4.2.3.2 閱讀順序
3.4.2.3.3 可跳過性
3.4.2.3.4 可跳出性
3.4.2.3.5 導覽文件
3.5 適用性報告
3.5.1 導論
3.5.2 出版品適用性
3.5.3 評量者資訊
3.5.4 重新評量適用性
4. 最佳化的出版品
5. 遞送
6. 隱私與安全
A. EPUB無障礙用語集
A.1 概要
A.1.1 關於此用語集
A.1.2 參照
A.1.3 供適用性使用的特性
A.1.3.1 certifiedBy
A.1.3.2 certifierCredential
A.1.3.3 certifierReport
B. 變更紀錄
C. 致謝
D. 參考資料
D.1 規範性文件
D.2 參考性文件

## 1. 導論

### 1.1 概要

本章節為非規範性。

本規格，EPUB無障礙輔助性，用以描述EPUB®生態系統中的兩項關鍵需求。

- 對EPUB出版品的無障礙品質提供發現性；以及

- 對具無障礙輔助的EPUB出版品進行評量以及認證。

提供無障礙輔助性詮釋資料可便於判斷一本EPUB出版品的易用性。消費者能用以檢視內容擁有哪些特性，以決定一本EPUB出版品是否符合其需求，無論是否滿足無障礙輔助的驗證標準。最低標準，所有適用本規格的EPUB出版品，需滿足 §2發現性 中所闡述的無障礙輔助性詮釋資料規定。

儘管EPUB製作者總是以高標準提供EPUB出版品無障礙輔助性，本規格依然設置了正式的規定以驗證內容是否具備無障礙輔助性。這些規定提供了EPUB製作者一系列明確的指引來評量其內容，並且能用於驗證其品質。一本具無障礙輔助性的EPUB出版品需要滿足 §3無障礙出版品 中所闡述的無障礙輔助性規定。

本規格也建立了一套機制以識別EPUB製作者如何針對特殊的使用者需求，對內容進行最佳化，以致於無法滿足更廣泛的無障礙輔助性規定。最佳化出版品的規定請參閱 §4最佳化出版品 以獲得更多資訊。

本規格不指定單一版本的EPUB。其可應用於合乎任何版本或者子集的EPUB出版品，包含了本標準的未來版本。

理想上，這些準則可協助評量任何基於開放網頁技術製作的數位出版品，然而確保這樣的應用並非本規格的目標。

###### 注意事項

若想取得本規格中各決定的額外背景資訊，請參考EPUB無障礙輔助性常見問題（FAQ）。

### 1.2 有效技巧（Success Techniques）

本章節為非規範性。

本規格以抽象的手段來定義EPUB出版品的無障礙輔助規定，就如同網頁內容無障礙指引（WCAG）[WCAG2]將其無障礙輔助性指引和達成該指引的技巧分開一般。這種手段能夠讓指引隨著格式進化依然保持穩定。

為了讓此手段更易於執行，本規格伴隨的文件EPUB無障礙輔助性技巧[EPUB-A11Y-TECH-11]匡列出合規用的技巧。這些技巧解釋如何符合本規格中供不同版本EPUB之規定。

###### 編輯注意事項

EPUB 3工作小組成立了一個任務組正在規劃供固定版面出版品使用的無障礙輔助技巧。當該文件正式發表時，將會於本章節提及。

#### 1.2.1 國際化

本規格在敘述無障礙輔助性需求，也注意到不同語言讀者之需求。這和定義在[WCAG2]中的各項原則（Principles）以及成功標準（success criteria）相同。目標是為了確保使用者能夠完整地獲取一份出版品的資訊，無論他們偏好使用何種感知方式閱讀。

同時，所發行文字的語言與書寫習慣會影響符合無障礙輔助性規定所必要的技巧。EPUB要求支援萬國碼（Unicode）文字[EPUB-3]，例如，為了確保能夠使用正確的字元資料（例如：EPUB製作者不需將文字做成圖片）。儘管這是重要的功能，但光這樣不足以確保文字能使每一種語言都具備無礙輔助性（例如也可能需要額外的資訊，如文字方向、強調、標點等）。

結論上，符合無障礙輔助性規定可能須針對語言或文化來進行實踐。這些實踐定義在本規格或者其達成技巧，或其他地方（例如，在WCAG技巧或者特別語言的最佳實踐推薦中），取決於其是否專屬於EPUB，或者更廣泛地影響到所有網頁內容。

#### 1.3 適用於舊版規格

本章節為非規範性。

本規格可應用於任何EPUB出版品，就算符合不參考此規格舊版本的內容亦然（例如，EPUB 2 [OPF-201]）。

像這樣的EPUB出版品的製作者應該在製作內容時，合乎本規格對無障礙輔助性及發現性的規定。EPUB製作者也應該收集到最新版本的EPUB以能夠使用最先進的無障礙輔助功能以及技巧。

#### 1.4 術語

本規格採用以下定義於EPUB 3 [EPUB-3]中的術語：

- EPUB內容文件
- EPUB製作者
- EPUB出版品
- 媒體覆蓋文件
- 包裝文件
- 閱讀系統

此外，也使用了[WCAG2]中的輔助科技定義。

###### 注意事項

輔助科技並非為分離於閱讀系統的應用程式。閱讀系統經常整合了獨立的輔助科技功能，像是文字轉換語音（text-to-speech）播放。

#### 1.5 適用性

本規格中被標註為非規範性的章節，以及所有製作指引、圖表、範本以及注意事項都為非規範性。本規格其他部分皆為規範性。

關鍵字：**可以(MAY)**、**必需(MUST)**、**不得(MUST NOT)**、**選擇性(OPTIONAL)**、**推薦(RECOMMENDED)**、**應該(SHOULD)**在本文件中，僅有在如上方式以粗體出現時，需按照BCP 14 [RFC2119]中的敘述詮釋。

## 2. 發現性

### 2.1 導論

本章節為非規範性。

不像網頁，EPUB製作者透過許多管道遞送EPUB出版品供人們使用──此模式使得EPUB成為成功的電子書和其他類型數位出版品的格式。然而，作為此模式的結果，出版品在無障礙輔助性上特定細節，必須伴隨著一併發布。

線上書店從出版社以及作者處取得內容，故此，除非出版社透過詮釋資料告知，不然他們無法得知每次遞交出版品之製作品質。

將能使任何相關組織能夠發現EPUB出版品的無障礙輔助品質，作為主要考量。使用者必須能夠在他們購買、借閱或以其他方式取得EPUB出版品時，判斷其可用性，需要評判標準以知悉該書提供了多少可能性以符合無障礙輔助性規定。

同樣，未能達到本規格之無障礙輔助性需求的內容，則不代表無法滿足個別讀者之需求。

唯有透過提供完整詮釋資料，才能讓使用者判斷內容是否適合他們使用。

### 2.2 包裝詮釋資料

所有EPUB出版品**必需**在其包裝文件中包含 [schema-org] 無障礙詮釋資料，以展現其無障礙輔助特性，無論該出版品是否符合無障礙輔助性或者最佳化規定。

EPUB出版品**必需**包含以下無障礙輔助性詮釋資料：

- accessMode — 
- accessibilityFeature — 功能及內容修改，其有助於整體內容的無障礙輔助性（例如，替代文字、延伸描述、字幕）。
- accessibilityHazard — 任何內容呈現時的潛在危害（例如，閃光、模仿動作、聲音）。
- accessibilitySummary — 一份人類可閱讀的整體無障礙輔助性摘要，其包含了對於任何已知缺失的敘述（例如，缺少延伸描述，特定的危害）。

EPUB出版品**應該**包含以下[schema-org] 無障礙詮釋資料

- accessModeSufficient — 一組一或多個存取模式，其足以用來消費內容並且不會明顯掉失資訊。一本EPUB出版品可以有多於一組充要的存取模式供內容消費，取決於其包含了哪種類型的內容（然而，與accessMode不同，本特性考量內容不具備廣泛的無障礙輔助性，像是包含聲音內容的文字抄本）。

EPUB製作者**可以**包含本章節並未指定、額外的 [schema-org] 無障礙輔助性詮釋資料。

###### 注意事項
請參照 詮釋資料發現性技巧 [EPUB-A11Y-TECH-11] 以獲得更多關於這些特性的資訊，以及如何將其包含在不同版本的EPUB中。也請見 在遞送紀錄中包含無障礙輔助性詮釋資料 [EPUB-A11Y-TECH-11] 獲得更多資訊，以在其他格式中包含無障礙輔助性詮釋資料。

### 2.3 連結的詮釋資料紀錄

無障礙輔助性詮釋資料也能包含在連結的紀錄 [EPUB-3] 中（即為，透過link元素參照的詮釋資料紀錄），但僅在連結的紀錄中包含這樣的詮釋資料無法滿足本規格的發現性規定。

## 3. 無障礙出版品

### 3.1 導論

本章節為非規範性。

EPUB建構在開放Web平台上，HTML、CSS、JavaScript與SVG為應用在內容製作的核心科技。使用這些技術即代表，EPUB製作者可以輕鬆地適當應用既已完善的Web無障礙輔助性技巧，來打造具有高度無障礙輔助性的EPUB出版品。

產出具無障礙輔助Web內容的主要依據是W3C網頁內容無障礙輔助性指引（Web Content Accessibility Guidelines, WCAG） [WCAG2]。本規格受到了WCAG既已完成的廣泛工作所影響，用其建構對無障礙輔助內容的評比標竿，也是用相同的四項高等級內容原則 — 可感知（perceivable）、可操作（operable）、可理解（understandable）、穩健的（robust） — 此為製作無障礙EPUB出版品的中心。

本章節定義了如何應用定義於WCAG中的適用性標準於EPUB出版品，以及描述獨特的性質。

符合本章節規定製作的EPUB出版品，及擁有高度的無障礙輔助性，可廣泛地滿足讀者對閱讀的需求以其偏好方式。

### 3.2 與WCAG之關係

本章節為非規範性。

WCAG [WCAG2]及其相關的技巧，提供了網頁內容無障礙輔助性問題及解法，其包含範圍廣闊 — 從表格到嵌入式多媒體，以至於豐富語義。這些都是本規格所能建構的基礎。

本規格並不重複這些規定，或者於這些文件中所介紹的技巧。因為這麼做將會造成使兩份標準不相容的風險（即為，讓指引不同步，甚至產生衝突）。同時，就算本規格不再重申這些規定，也不會減低製作具無障礙輔助性EPUB出版品的重要性。

相對之下，本規格定義如何應用WCAG在EPUB出版品上 — 相對於網頁為一整頁，EPUB出版品是一系列Web文件的集合 — 並且添加一組額外的規定。這些規定與WCAG所涵蓋範圍同等重要；它們只是單純為了EPUB出版品需求所提供（每項規定都在其各自章節解釋與WCAG的關係）。

同樣的道理可套用在EPUB無障礙輔助性技巧文件 [EPUB-A11Y-TECH-11] 上頭。其提供了特別為了EPUB出版品所用的技巧，或者在EPUB出版品脈絡下需要特別說明。這不意味著其他的WCAG技巧不適用。

結果上，儘管EPUB製作者可以在不擁有對WCAG適用性的深刻知識下閱讀本章節，但要實作本規格的無障礙輔助性規定，依然需要對WCAG有所理解。

由於本規格添增了不屬於WCAG的規定，所以一本EPUB出版品可以合乎WCAG卻不合於本規格。

### 3.3 WCAG適用性

#### 3.3.1 WCAG適用性規定

一本EPUB出版品若要合乎本規格，則：

- **必需**符合WCAG 2.0 [WCAG20] 的規定，但強烈**推薦**符合最新推薦版本WCAG 2之規定。

- **必需**符合A等級的規定，但強烈**推薦**符合AA等級之規定 [WCAG2]。

以上規定所提供的報告彈性，是用以確保本規格能在那些強制要求無障礙輔助性的區域受到採用，但不需要取消或者取代這些區域既已生效的規定。

本規格將WCAG 2.0 A等級設為規定底線，主要是為了給EPUB製作者對舊內容的反向相容性，以及在沒有正式規定下，鼓勵採用具無障礙輔助產製流程的彈性。大多數實踐無障礙輔助性的製作者，都不會認為A等級提供了高度的無障礙輔助性。

理想上，EPUB製作者應該試著符合最新版本WCAG 2 AA等級規定，但地方與國家法律，或代理商、通路端，才決定了他們需要符合的正式規定。

###### 注意事項
對於無障礙輔助性的法律規定，案例包括歐盟的2019/882指令，以及美國1973年發布《康復法案》的508條款。EPUB出版品需要符合高於基本A等級以上的成功標準，才能合乎這些法規。

持續跟進WCAG的優點是可以持續增進對使用者的使用權。隨著Web技術迭代演進，察覺阻礙使用權的狀況的手段也會進化，標準就會增添新的規定。符合這些額外的規定可以協助確保EPUB出版品使用最先進的技巧。然而，符合舊版本的規定也依然有用，結果上提供的閱讀體驗比最佳化差一點。

同樣的，法律框架與政策也經常採用AA等級適用性作為無障礙輔助性的評比標竿。理由是其提供了EPUB製作者實際上能夠實作出最大幅度的改進（EPUB製作者如果可以，就應該嘗試符合AAA等級，但是一般不大可能完整符合AAA等級規定）。當EPUB製作者僅符合A等級適用性，他們對許多使用者族群做出了妥協，結果上提供的閱讀體驗比最佳化差一點。

###### 注意事項


#### 3.3.2 評量WCAG適用性

##### 3.3.2.1 頁面與出版品

WCAG原則 [WCAG2] 聚焦於評量單一網頁，但一本EPUB出版品更近似於WCAG中所指出的一組網頁「（一組）具備相同目標的網頁集合」[WCAG2]。

結論上，在評量一本EPUB出版品的無障礙輔助性時，EPUB製作者不能單獨檢視個別頁面 — 在EPUB 3中稱為內容文件。相對之下，EPUB製作者**必需**將其視為更大作品的一部分來評量其無障礙輔助性。

舉個例子，EPUB製作者光是給予單獨EPUB內容文件邏輯閱讀順序還不夠，還要確認該文件置於正確的閱讀順序中。同樣的在每一份EPUB內容文件中包含標題可以作為整份出版品標題的補充：但無論少了哪一方，都會降低整體無障礙輔助性。

EPUB製作者**必需**依照WCAG對內容的指引：可感知、可操作、可理解、穩健的，對整本EPUB出版品進行評量，而不僅對之中的個別內容文件為之。

EPUB無障礙技巧 [EPUB-A11Y-TECH-11] 提供了更多應用這些指引到EPUB出版品上的資訊。

##### 3.3.2.2 應用適用性規範

當評量EPUB出版品時，WCAG適用性標準可按照以下方式應用：

- 當判斷合乎哪一個適用性等級時，EPUB出版品整體都**必需**達到要達到之等級的適用性規定。
- EPUB製作者**不得**利用EPUB的回退機制來提供合規的替代版本 [WCAG2]，因為無法提供可信賴的手段讓使用者得以存取這些回退。如果EPUB製作者使用回退，那麼主要內容與其回退兩方都**必需**符合要達到之適用性等級的規定。專屬於EPUB的回退機制包含了宣告回退 [EPUB-3]、bindings元素 [EPUB-3]以及透過epub:switch元素的內容切換 [EPUB-3]。
- 當以「整個頁面」規定[WCAG2]來判斷合規與否時（例如當宣稱合規時，頁面中的部分不得有例外），每一份EPUB內容文件的完整性**必需**達到該適用性等級，以及EPUB出版品中的每一份內容文件**必需**符合宣稱的適用性等級。


### 3.4 EPUB規定

#### 3.4.1 Page導覽

###### 3.4.1.1 概論

本章節為非規範性。

靜態分頁的內容迄今依然普及，就像是印刷書，目前還是被一般讀者大眾以及教育現場兩方最主要用來閱讀的媒介。印刷書不僅是固定分頁的內容來源，同時在固定版面（fixed-layout）數位出版品中，也會看到靜態分頁的內容。

結果來說，在相同使用靜態分頁內容的環境中，透過非視覺方式閱讀的讀者與其同儕相比，相對處於劣勢，他們不能輕鬆地在一份出版品中找到相同的位置（例如，當老師要求學生翻到指定的一頁）。

包含分頁邊界的位置可以協助撫平這項不公平，讓選擇文字重排媒介的使用者不會居於劣勢。

文字重排出版品缺少靜態分頁資訊，提供分頁導覽可以作為補齊。這些出版品透過閱讀系統的預設分頁並非固定，會按照顯示區域尺寸以及使用者的字型設定而產生變化。結果上，若缺乏靜態參照資訊，要讓使用者閱讀同一本EPUB出版品時到相同位置難以達成。

包含分頁導覽資訊，可作為一項達成多面向成功標準（Multiple Ways success criterion） [WCAG2] 的方法，其提供了另一個有意義的手段，讓使用者能用來存取內容（即為，在目錄、線性閱讀順序以及其他導覽協助之外附加此項）。

提供分頁導覽在混合印刷書/電子書的環境中相當重要，規定包含此項功能為優先，也可以視為達到多面向成功標準的多種手段之一。

###### 注意事項
請見 [EPUB-A11Y-TECH-11] 

###### 3.4.1.2 可應用性

當以下任一狀況成立時，一本EPUB出版品**應該**包含定義在本章節中的分頁導覽目標：

- EPUB製作者將該EPUB出版品視為靜態分頁出版品的動態分頁對等版（即為包含在一個印刷／數位合輯中）；
- EPUB製作者提供該EPUB出版品作為靜態分頁出版品的替代品，並應用於合理推斷會同時使用兩種版本的環境（例如教育現場）；或者
- EPUB製作者在同一流程中產製出EPUB出版品以及靜態分頁的出版品，可跨格式維持分頁點位置。

EPUB製作者**可以**在沒有相對靜態分頁對應的狀況下，為文字重排的EPUB出版品包含分頁導覽。

###### 3.4.1.3 目標

###### 3.4.1.3.1 分頁來源

**目標**

識別靜態分頁點位置來源。

**了解目標**

使用者需要知道一本EPUB出版品分頁的來源，以決定是否能滿足他們的需求。例如印刷出版品，其精裝書與平裝書版本可能在分頁上有所差異。同一本書的不同版本可能在分頁上也會不同。

包含靜態分頁來源之可辨識的識別碼，像是其ISBN或ISSN，可以讓使用者用來判斷分頁對應到哪一個版本。

如果EPUB製作者要為僅有數位版之出版品加入分頁作為導覽輔助，就不能指定來源（即為，不可以把該出版品當作自己分頁的來源）。

**達成目標**

當一本EPUB出版品包含分頁點標記及／或頁面列表，其對應到該出版品的靜態分頁版本時，EPUB製作者**必需**在包裝文件詮釋資料中識別其來源。

###### 3.4.1.3.2 頁面列表

**目標**

提供靜態分頁點位置的導覽。

**了解目標**

頁面列表是用於導覽分頁點位置的主要手段，其提供了一組列表，各項目可連結到EPUB出版品中的靜態分頁點位置。

閱讀系統一般使用此列表來產生「到第？頁」介面，讓使用者能夠輸入他們想要前往的頁碼，但有時也會讓使用者能夠存取整份列表來選擇他們想要前往的頁碼。

若缺少頁面列表，翻頁導覽將變得非常困難，只能依賴對個別分頁點標記的導覽（如果有的話）。

**達成目標**

一本EPUB出版品**必需**包含一份頁面列表。

EPUB製作者**應該**包含到由來源重新製作內容所有頁面的連結，（例如，列表不需要提供連結到空白頁面、或者連結到數位版本中沒有的內容）。

EPUB製作者應該將供來源中所有頁面的連結包含於其中，無論是否被重新製作，但這並非規定。

###### 3.4.1.3.3 分頁點

**目標**

提供靜態分頁點位置。

**了解目標**

在EPUB出版品中插入分頁點標記能夠提供給使用者他們在文字中哪一部分的脈絡。輔助科技可以使用這項資訊來告知使用者現在的頁碼，例如，當使用者想要摘要頁面上的內容時。

包含分頁點標記也能讓使用者透過頁數快速地前後翻閱，而不需要每次都透過頁面列表來存取。

包含這些標記也可讓製作頁面列表變得簡單，只需要簡單地提供這些連結的參照位置。

**達成目標**

在EPUB出版品中包含分頁點標記為**選擇性**。

但若EPUB製作者要包含分頁點標記時，則：

- 他們**應該**包含由來源重新製作所有頁面使用的分頁點標記（即為，空白頁以及在數位版本中沒有被重製的內容就不需要標記）。
- 它們應該包含將供來源中所有頁面使用的的分頁點標記（無論是否被重新製作），但這並非規定。

此外，如果頁碼在該內容的同步文字語音播放中被朗讀出來（例如，EPUB 3媒體覆蓋 [EPUB-3] ），EPUB製作者**必需**在標記中識別其頁碼以控制播放。

##### 3.4.2 媒體覆蓋播放

###### 3.4.2.1 概論

本章節為非規範性。

媒體覆蓋能夠透過文字與語音同步提供無障礙輔助播放體驗給需要的受眾。對於僅需要聲音播放，或者僅需要閱讀時強調文字的的使用者也有幫助。媒體覆蓋也能為全部使用者提供整本EPUB出版品從頭到尾無縫的播放體驗。

然而，作為基礎的媒體覆蓋文件規格 [EPUB-3] 僅提供閱讀系統最小限的教程。其指出了聲音片段需要呼應文字，並且強調該段文字。結果使得使用者僅有基本的開始與停止選項可用。

EPUB製作者需要為媒體覆蓋文件添加結構與語意，才能讓閱讀系統提供更多有用的體驗。有完善的標記，閱讀系統可以提供這些功能，包括：跳過次要內容、使其不會干預到主要敘事。以及讓使用者可以跳出深層巢狀結構，如表格。以及讓他們可以出版品的章節間進行導覽，而不需要回到目錄頁。

為媒體覆蓋文件添加結構與語意，可廣義滿足 [WCAG2] 中的資訊與關聯成功標準。缺乏句結構以及有語意的播放序列，其影響會剝奪使用者對內容進行完整導覽的可能。

###### 3.4.2.2 可應用性

媒體覆蓋文件**必需**符合 [EPUB-3] 中的規定。沒有必要符合定義於 [EPUB-3] 外的額外規定，即可符合本規格之規定。

為了讓媒體覆蓋的效益最大化，符合人們不同的閱讀需求，強烈鼓勵EPUB製作者符合定義在下一章節的**選擇性**目標。

###### 注意事項

EPUB製作者不需要為了符合這些規定，在其EPUB出版品中添加媒體覆蓋。

###### 3.4.2.3 目標

###### 3.4.2.3.1 完整性

**目標**

確認全文都有對應的語音。

**了解目標**

雖然使用者可以使用文字轉換語音播放來將整本出版品轉換成聲音形式，但其體驗相對於提供預先錄製旁白的出版品來得差。文字轉換語音引擎受限於內建的詞彙，當他們遇到非常用字時，常會不曉得怎麼發音或者發錯音。結果讓使用者必須重複播放該字或者逐字拼出才能讀懂內容的意義，這降低了他們的閱讀速度並且阻礙對內容的理解。

因此，一本出版品額外提供全文的旁白顯得重要。使用者可以決定以何種偏好的模式進行閱讀：文字、聲音，或者兩者混合。

**達成目標**

EPUB製作者**必需**為所有文字內容透過媒體覆蓋方式提供同步語音播放。

###### 3.4.2.3.2 閱讀順序

**目標**

確保媒體覆蓋播放符合邏輯閱讀順序。

**了解目標**

每一本EPUB出版品都有其預設閱讀順序，可讓使用者按照邏輯進度閱讀內容。其確保讀者可以跟從主要敘述，以及他們會在最符合文脈之處遇到次級內容。預設閱讀順序也建立一些較不明顯的關係，像是在表格的格與格以及列與列之間的順序。

如果在媒體覆蓋文件中的par及seq元素的序列不符合該順序，會造成讀者的混亂，無論他們單純聆聽聲音或者嘗試在視覺上跟隨進度。

對播放提供順序以符合預設閱讀順序是最安全的方法，以確保使用者可以跟隨文字。在某些案例裡，嚴格遵守這項原則可能會令閱讀體驗變得較不好（例如，以行來播放表格，而並非列，在某些狀況下可能更符合邏輯）。本項目標的目的並非禁止以不同的方式呈現，而是確保任何差異都能回歸內容的邏輯順序。

**達成目標**

EPUB製作者**應該**在媒體覆蓋文件中排列par與seq元素的順序，使其能夠反映以下兩者：

- 所參照EPUB內容文件在書脊 [EPUB-3] 中的順序；以及
- 每個元素在其個別EPUB內容文件中的順序。

如果EPUB製作者使用不同的順序，其順序**必需**依然讓邏輯按照邏輯播放。

###### 3.4.2.3.3 可跳過性

**目標**

讓使用者可以自動跳過內容。

**了解目標**

在不受干預之下能夠閱讀一部作品的主要敘述，是閱讀理解的中心。EPUB製作者一般建構EPUB出版品在視覺上表現次要資訊，如側邊欄以及腳註等外於主敘述流的內容（例如，使用不同的背景色或者位置，如此一來讀者在閱讀時可以在視覺上分辨這些資訊）。

然而，如果讀者偏好使用聲音播放，預設就無法同樣簡單地跳過這些資訊。媒體覆蓋在閱讀系統中，一般會在遇到次級內容時直接播放。

當EPUB製作者為媒體覆蓋文件提供結構性語意時，閱讀系統就可以提供讓使用者預設決定在播放時要跳過哪些次級內容的閱讀體驗。

**達成目標**

EPUB製作者**應該**在媒體覆蓋文件中識別所有可跳過的結構 [EPUB-3] 。

###### 3.4.2.3.4 可跳出性

**目標**

讓使用者可以自動從結構性內容跳出。

**了解目標**

當以視覺閱讀時，使用者可以快速移開或者跳出高度結構性的內容，像是表格、列表以及圖片等。表格使用行與列構成，例如，讀者可以快速順著兩軸線之一來找到他們要的資訊，並且找到以後能輕易地回到主要敘述。同樣的，列表中的項目可讓使用者掃到他們要的內容，然後在他們找到想要的資訊後跳出來。

但預設上，媒體覆蓋文件就無法提供相同簡單地跳出內容功能了。使用者無法從表格的格、列甚至表格本身中跳出，除非EPUB製作者將文件中的這些元素以結構化語意進行編碼。

當EPUB製作者提供這些資訊時，閱讀系統可以為使用聲音的讀者簡化播放以提供更適切的閱讀體驗。

**達成目標**

EPUB製作者**應該**在媒體覆蓋文件中識別所有可跳出的結構 [EPUB-3] 。

###### 3.4.2.3.5 導覽文件

**目標**

確保當閱讀系統顯示EPUB導覽文件時，聲音播放能夠作為導覽輔助。

**了解目標**

閱讀系統一般提供自有介面來提供EPUB導覽文件的導覽輔助。例如，閱讀系統開啟目錄維特化的介面，呈現在使用者正在閱讀內容的頂端。

為了使用這些介面，使用者一般而言必須仰賴文字轉換語音播放（如果有）來聽到目錄項目。

為EPUB導覽文件提供媒體覆蓋文件，可以提供閱讀系統透過聲音標記呈現連結的能力，為使用聲音的讀者增進體驗。

**達成目標**

EPUB製作者**應該**為EPUB導覽文件 [EPUB-3] 包含媒體覆蓋文件。

### 3.5 適用性報告

#### 3.5.1 導論

本章節為非規範性。

評量者透過在EPUB包裝文件中的詮釋資料特性表述，以報告一本EPUB出版品的無障礙輔助適用性。

該詮釋資料建構以下兩者：

- 達成的適用性等級；以及
- 誰執行該項評量的資訊。

該詮釋資料使用了來自DCMI詮釋資料術語 [DCTERMS] 和EPUB無障礙輔助性用語集的特性組合，將會於以下章節進行更詳細的說明。

#### 3.5.2 出版品適用性

為了指出一本EPUB出版品合乎本規格的無障礙輔助性需求，其**必需**包含一個conformsTo特性，其值**必需**精準對應（即為在大小寫以及空格上）以下模式：

	EPUB-A11Y-A11Y-VER_WCAG-WCAG-VER-WCAG-LVL

其中：

**A11Y-VER**

  EPUB製作者**必需**指定該出版品符合的EPUB無障礙輔助性規格版本，但不包含小數點。EPUB製作者**必需**使用值11來指定本版本規格。

**WCAG-VER**

  EPUB製作者**必需**指定該出版品符合的WCAG版本，但不包含小數點（例如對於WCAG 2.0為20，WCAG 2.1為21）。

**WCAG-LVL**

  EPUB製作者**必需**指定該出版品符合的WCAG適用性等級（例如A或AA）。

以下是適用性字串可用於合乎本規格的出版品：

- EPUB-A11Y-11_WCAG-20-A
- EPUB-A11Y-11_WCAG-20-AA
- EPUB-A11Y-11_WCAG-20-AAA
- EPUB-A11Y-11_WCAG-21-A
- EPUB-A11Y-11_WCAG-21-AA
- EPUB-A11Y-11_WCAG-21-AAA

###### 注意事項

合規的適用性字串清單將會隨著W3C發布WCAG新版本而增加。

###### 範例1

以下範例呈現一本EPUB 3出版品的適用性宣告，其合乎EPUB無障礙輔助規格1.1版，並且達到WCAG 2.1的AA等級。

<package …>
   <metadata>
      …
      <meta 
          property="dcterms:conformsTo"
          id="conf">
         EPUB-A11Y-11_WCAG-21-AA
      </meta>
      …
   </metadata>
   …
</package>

###### 注意事項

未來WCAG 3.0版本可能也會出現新的等級名稱（現在為銅、銀、金）。這些名稱將會取代字串模式中的A、AA及AAA。

###### 注意事項

EPUB製作者可以使用適用性URL，如 [WCAG2] 中 適用性宣稱的必要元件 一節所定義，當EPUB出版品僅達到WCAG適用性規定時，可透過conformsTo特性提供（即為，不完整符合本規格）。

由於 [WCAG2] 未定義如何透過URL來指定適用性等級，EPUB製作者還是可以找到替代手段，在需要時連結該資訊（例如透過無障礙輔助性摘要）。

#### 3.5.3 評量者資訊

EPUB出版品**必需**包含一個 a11y:certifiedBy 特性，用以指定評量該EPUB出版品的組織名稱。

###### 注意事項

任何個人或者組織都可以進行適用性評量。評量者可為第三方，或和製作EPUB出版品的組織相同。

###### 範例2

以下範例呈現一本由出版社自行評量的EPUB 3出版品（dc:publisher與 a11y:certifiedBy特性的值相同）。

<metadata>
  …
  <dc:publisher>
     Acme Publishing Inc.
  </dc:publisher>
  …
  <meta
      property="dcterms:conformsTo"
      id="conf">
     EPUB-A11Y-11_WCAG-21-AA
  </meta>
  <meta
      property="a11y:certifiedBy"
      refines="#conf">
     Acme Publishing Inc.
  </meta>
  …
</metadata>

###### 範例3

以下範例呈現一本由第三方進行評量的EPUB 3出版品。（dc:publisher與 a11y:certifiedBy特性的值不同）。

<metadata>
  …
  <dc:publisher>
     Acme Publishing Inc.
  </dc:publisher>
  …
  <meta
      property="dcterms:conformsTo"
      id="conf">
     EPUB-A11Y-11_WCAG-21-AA
  </meta>
  <meta
      property="a11y:certifiedBy"
      refines="#conf">
     Foo's Accessibility Testing
  </meta>
  …
</metadata>

###### 範例4

以下範例呈現一本由EPUB製作者自行評量的EPUB 3出版品。

<metadata>
  …
  <dc:creator>
     Jane Doe
  </dc:creator>
  …
  <meta
      property="dcterms:conformsTo"
      id="conf">
     EPUB-A11Y-11_WCAG-21-AA
  </meta>
  <meta
      property="a11y:certifiedBy"
      refines="#conf">
     Jane Doe
  </meta>
  …
</metadata>

###### 範例5

以下範例呈現一本自行評量的EPUB 2出版品。

<metadata>
  …
  <dc:publisher>
     Acme Publishing Inc.
  </dc:publisher>
  …
  <meta
      name="dcterms:conformsTo"
      content="EPUB-A11Y-11_WCAG-21-AA"/>
  <meta
      name="a11y:certifiedBy"
      content="Acme Publishing Inc."/>
  …
</metadata>

###### 注意事項

當一本出版品由某組織評量時，使用者一般可能會想知道該組織的名稱。本規格鼓勵包含進行評量的個人姓名，以取代組織名稱，然而這樣的宣告可能會降低使用者的信任。

進行評量的日期**可以**透過連結一個dcterms:date特性 [DCTERMS] 到id:certifier，來進行指定。

###### 範例6

以下範例呈現進行評量的日期。
<meta
    property="a11y:certifiedBy"
    id="certifier">
   EPUB Accessibility Evaluator
</meta>
<meta
    property="dcterms:date"
    refines="#certifier">
   2021-09-07
</meta>

如果評量內容的組織有憑證或者標章可用來提供評量內容的權威，可透過一個a11y:certifierCredential特性來包含該項資訊。

###### 範例7

以下範例呈現一個憑證。使用refines屬性將憑證與id：certifier進行關聯。

<meta
    property="dcterms:conformsTo"
    id="conf">
   EPUB-A11Y-11_WCAG-21-AA
</meta>
<meta
    property="a11y:certifiedBy"
    refines="#conf"
    id="certifier">
   EPUB Accessibility Evaluator
</meta>
<meta
    property="a11y:certifierCredential"
    refines="#certifier">
   A+ Accessibility Rating
</meta>

如果評量內容的組織提供公開可讀的報告，可以透過一個a11y:certifierReport特性來提供對該報告的連結。

###### 範例8

以下範例呈現到遠端託管無障礙輔助性報告的連結。

<meta
    property="dcterms:conformsTo"
    id="conf">
   EPUB-A11Y-11_WCAG-21-AA
</meta>
<meta
    property="a11y:certifiedBy"
    refines="#conf"
    id="certifier">
   EPUB Accessibility Evaluator
</meta>
<link
    rel="a11y:certifierReport"
    refines="#certifier"
    href="http://www.example.com/a11y/report/9780000000001"/>

###### 範例9

以下範例呈現到本地端無障礙輔助性報告的連結。

<meta
    property="dcterms:conformsTo"
    id="conf">
   EPUB-A11Y-11_WCAG-21-AA
</meta>
<meta
    property="a11y:certifiedBy"
    refines="#conf"
    id="certifier">
   EPUB Accessibility Evaluator
</meta>
<link
    rel="a11y:certifierReport"
    refines="#certifier"
    href="reports/a11y.xhtml"/>

###### 注意事項

每一個詮釋資料格式所能表達的內容都具其獨特性，本規格並不指定在EPUB包裝文件外，該如何表示適用性詮釋資料。

###### 注意事項



#### 3.5.4 重新評量適用性

本章節為非規範性。

###### 注意事項

以下指引用於協助EPUB製作者判斷是否需要進行新的評量。而不是為了合乎本規格的規定。

一本EPUB出版品的適用性評量有效期間多長？這是個複雜的問題。不像網站會持續性的演進，EPUB製作者可能在初版之後就不會再更新EPUB出版品了。結論來說，EPUB出版品若不修改，就永遠適用於最終的評量。

然而，發布更新版的EPUB出版品以修正作品中的錯誤或者誤字，或者週期性地發布新版本，對出版而言這是常態。而並非所有對EPUB出版品變更都會改變其無障礙輔助性，這使得EPUB製作者需不需要進行新的評量成了複雜的問題，要做整體、還是部分的重新評量就好，也是問題。

作為規則，EPUB製作者必須重新評量其內容，當他們對一本EPUB出版品的結構以及功能做了根本性的變更，例如：

- 調整了EPUB內容文件中標記的性質或者順序；
- 添加或修改了承載資訊的圖片；
- 修改會影響到可讀性的格式（例如：對比）；以及
- 添加或修改了控制與表單等互動。

如果該EPUB出版品大致上內容與標記與前一發佈版本相同，EPUB製作者可以僅需要評量修改之處以重新確認適用性。

如果本規格或者 [WCAG] 在該EPUB出版品最終發布後推出了更新版本，本規格則推薦進行新的評量以確保適用性符合最新標準。在這狀況下，EPUB製作者可以不需進行完整的重新評量（即為，他們僅需要確認新的或者變更的成功標準，除非標準在方法或者適用性上進行了大幅變更）。

反過來，EPUB製作者在進行以下微幅變更時，不需要進行重新評量，如：

- 修正內文的錯誤修正（即為，沒有變更到標記）；
- 新增或者調整裝飾性的圖片；
- 修改不會影響到理解內容或者變更文字顯示的格式；以及
- 修改包裝文件的詮釋資料。

能夠判斷對EPUB出版品的無障礙輔助性的個人，應該判斷修改是否為根本性。舉個例子來說，編輯可能不會注意到小格式修正造成的影響。

就算僅微幅修改，若無障礙標準有所修訂，本標準依然建議更新評量（全部或者部分）。

EPUB製作者應該嘗試比這裡所敘述更積極的態度。等到內容更新，才檢視與更新EPUB出版品的無障礙輔助性，可能使其無法對應近期的演進。舉個例子，出版社應該優先地週期性檢視最熱銷EPUB出版品，以確保它們能夠廣泛地受到最多數讀者所使用。

## 4. 最佳化的出版品

本章節為非規範性。

雖然WCAG [WCAG2] 提供了一組通用指引使內容能夠具備廣泛的無障礙輔助性，但合規的內容並非都能針對特別使用族群最佳化。反過來說，針對特殊需求或者閱讀模式的最佳化內容，通常不會正好合乎WCAG，因為目標受眾為特殊族群。

例如，一本EPUB出版品包含同步的文字與聲音，可以包含完整內容的錄音，但是文字內容僅包含主要標題。這案例中，EPUB出版品可以被需要聽到內容的使用者所消費（即為，他們可以聽到完整的出版品，並且透過標題進行導覽），但是卻無法被不能聽到聲音的人所使用。

換句話說，當EPUB製作者針對特定閱讀模式為EPUB出版品進行最佳化，就會無法達到WCAG適用性等級，但依然能對預期的受眾提供完整的無障礙輔助。

為最佳化出版品定義規定並非本規格的目標，我們認同其他為這些特別需求所制定的標準以及指引。本規格僅提供基本的通用模式，以識別EPUB製作者對內容做出了如何的最佳化。

詳細來說，如果一本EPUB出版品符合一項最佳化標準，最佳實踐推薦如下：

- 該EPUB出版品應該符合本規格的發現性詮釋資料規定，使無障礙特性能被機器所閱讀。

- EPUB出版品應該在一個符合[DCTERMS]的conformsTo特性中，識別其所遵從的標準或者指引，使資訊能夠讓使用者取得。

- 若該標準未定義適用性的值供conformsTo特性使用，EPUB製作者應該使用URL [URL] 以指向標準的公開位置，這樣使用者可以查詢標準的特定細節。

- 如果識別碼不足以讓使用者理解其適用性（例如，該指引並未公開），EPUB製作者應該在無障礙輔助性摘要中提供額外資訊說明內容如何最佳化。

當為最佳化的EPUB出版品製作指引時，建議這些實踐應該要與正式適用性規定相整合。

###### 注意事項

請參照最佳化出版品標準指南，以取得非正式的標準列表。

###### 範例10

以下範例呈現一本符合DAISY可導覽僅有聲音的EPUB 3指引 [DAISYAudio] EPUB出版品的合規性聲明。

<package …>
   <metadata>
      …
      <link
          rel="dcterms:conformsTo"
          href="http://www.daisy.org/guidelines/epub/navigable-audio-only-epub3-guidelines"/>
      …
   </metadata>
   …
</package>

###### 範例11

以下範例呈現一本針對點字呈現最佳化的EPUB出版品的無障礙輔助摘要。

<meta property="schema:accessibilitySummary">
    This publication is optimized for braille readers. It will not be 
    usable by persons who cannot read braille. The publication is designed
    for braille reading devices capable of displaying 6-character cells and
    40-character line lengths. The text is not contracted, and follows 
    Unified English Braille formatting conventions. All characters are
    encoded using the Unicode braille character set.
</meta>

###### 範例12



<meta property="schema:accessibilitySummary">
    This publication is an audio book. It will not be usable by persons who 
    cannot hear the audio. The publication is recorded by a professional
    narrator. There is navigation to the beginning of each chapter. The text
    of the publication is not included. Images are not included, but the
    photo captions are narrated at the end of the chapter where they occur.
</meta>

## 5. 遞送

本章節為非規範性。

###### 注意事項

儘管EPUB製作者不需要跟從本章節中的推薦事項，依然可以符合本規格。但有些法規要求EPUB製作者按照相同的方式執行。例如歐盟2019/882指令，包含了相同的規定供在歐盟流通的數位出版品使用。

製作具無障礙輔助的EPUB出版品，並不保證該出版品能被使用者以具輔助性的方式取得或者消費。取決於EPUB製作者如何遞送他們的EPUB出版品。其他要素將會影響到整體無障礙輔助性。例如，在遞送過程中，具有無障礙輔助的介面供定位和取得內容是必要的環節，能夠搜尋並且檢視無障礙輔助性詮釋資料也一樣重要。



為了讓遞送對無障礙輔助性的影響限縮在最小限度，本規格建議EPUB製作者遵守以下遞送實踐：

- 其不得添加限制以限制輔助科技的存取；以及
- 若該格式支援，其必須在EPUB出版品供遞送使用的紀錄格式中包含無障礙輔助詮釋資料（即為[ONIX] 或 [MARC21]）。

###### 注意事項

遞送端可能會套用數位權利管理綱要，其會阻礙無障礙輔助性，但這並非EPUB製作者的錯。跟從本章節的指引，不是要限制EPUB製作者使用這樣的遞送端。其目的是讓EPUB製作者不要啟動某個一般不會啟動的功能以影響無障礙輔助性。

## 6. 隱私與安全

本章節為非規範性。

製作無障礙輔助內容並不會為使用者產生新的隱私與安全性考量。符合無障礙輔助規定僅為適當地使用既有的科技，本規格未提出任何新的功能。

EPUB製作者包含無障礙輔助詮釋資料也一樣，不會為其產生安全或隱私問題，僅用於描述一本EPUB出版品提供通用概念，表示是否適用於不同使用者族群。

使用無障礙輔助詮釋資料的一端，如閱讀系統、書店、以及其他可能建立使用者樣貌的介面，從另一個角度來看，就有可能違反個人隱私法律。例如，其可能有助於儲存或者預估使用者會想要消費或者最佳啟動其播放的內容類型，開發者不應該搜集這類資訊，除非取得該類使用者的同意，並且應該提供簡易刪除該使用者樣貌的手段。

儘管在使用者同意應用程式取得關於他們無障礙輔助需求資訊的狀況下，開發者必需確保這些資訊能夠保持私有（即為，不得和第三方廣告商、甚至原出版社分享）。

使用者基於內容的無障礙輔助性特性進行搜尋，作為搜尋的一種特性，開發者也應該注意關於此類資訊之儲存或者探勘。這類資訊可以間接地描述使用者的狀態。

## A. EPUB無障礙用語集

### A.1 概要

#### A.1.1 關於此用語集

本用語集定義了在EPUB出版品包裝文件詮釋資料中用以敘述無障礙輔助性的特性。

#### A.1.2 參照

用以參照本用語集的基準URL為http://www.idpf.org/epub/vocab/package/a11y/#

本規格保留字首"a11y:"供本用語集的特性使用。EPUB製作者不需要在包裝文件供宣告此字首。

#### A.1.3 供適用性使用的特性

##### A.1.3.1 certifiedBy

certifiedBy特性之定義

名稱：certifiedBy

說明：	識別負責對EPUB出版品之無障礙附註性進行測試與認證的組織。


允許的值：xsd:string

基數：	一或多個

範例：
	
<meta
    property="a11y:certifiedBy">
   Accessibility Testers Group
</meta>

##### A.1.3.2 certifierCredential

certifierCredential特性之定義

名稱：certifierCredential

說明：	識別一項憑證或者標章，其由與certifiedBy特性相關聯的組織所發行，其權威組以驗證內容具無障礙輔助性。

允許的值：	xsd:string

基數：	零或多個

延伸：	a11y:certifiedBy

範例：

<meta
    property="a11y:certifiedBy"
    id="certifier">
   Accessibility Testers Group
</meta>
<meta
    property="a11y:certifierCredential"
    refines="#certifier">
   DAISY OK
</meta>

##### A.1.3.3 certifierReport

certifierReport特性之定義

名稱：certifierReport

說明：	提供對一份無障礙輔助性報告的連結，其由與certifiedBy特性相關聯的組織所製作。

允許的值：xsd:anyURI

基數：	零或多個

延伸：	 certifiedBy

範例：

<meta
    property="a11y:certifiedBy"
    id="certifier">
   Accessibility Testers Group
</meta>
<link
    rel="a11y:certifierReport"
    refines="#certifier"
    href="https://example.com/a11y-report/"/>

## B. 變更紀錄

本章節為非規範性。

請注意，本變更紀錄僅用於辨識自EPUB無障礙輔助性1.0以來根本性的變更 — 這些變更會影響到EPUB出版品的適用性，或具同樣的重要性。

若要取得在改版過程中所有議題的列表，請參考工作小組的議題追蹤器。

28-Sep-2021: 最佳化出版品章節改為非規範性，並且重新寫過以強調用以便是合乎哪些標準的最佳實踐，請見pull request 1833。

23-Sep-2021: 新增章節以解釋國際化的影響與使用的技巧，請見issue 1790。


07-Sep-2021: 新增使用refines屬性指向certifier詮釋資料的範例，以呈現預期的連結，請見issue 1789。

07-Sep-2021: 新增對dcterms:date特性能用於指出評量進行時間的解釋，請見issue 1590。

09-June-2021: 釐清僅有數位的出版品，就算有分頁點標記及/或包含分頁清單時，也不該指定其分頁來源。


29-Apr-2021: 變更適用性識別碼，使用連字號與連接號以避免在純文字字串中造成困擾，請見issue 1455。

26-Mar-2021: 新增非規範章節，以具體描述何時該重新評估EPUB出版品，請見issue 1470。

12-Mar-2021: 將遞送章節改為非規範性，但新增一項注意事項指出法規（例如在歐盟）必須要遵守的規定。請見issue 1487。

08-Mar-2021: 添加目標使媒體覆蓋文件中par及seq元素的序列反應邏輯閱讀順序。請見issue 1556。

05-Mar-2021: 新增推薦，內容中從來源重製的所有頁面都該包含頁面標記，以及最佳實踐，為來源中的所有頁面都該包含頁面標記。請見issue 1502。

05-Mar-2021: 新增推薦，頁面列表中從來源重製的所有頁面都該包含連結，以及最佳實踐，頁面列表中所有來源的頁面都該包含連結。請見issue 1503。

05-Mar-2021: 重現調整EPUB規定章節架構，將頁面導覽以及媒體覆蓋標題中群組化的個別目標分開。請見issue 1458。

25-Feb-2021: 以更具彈性的文字字串取代用於回報符合1.0規格的IDPF URL。請見issue 1455。

19-Feb-2021: 更新對WCAG 2.0的參照，指向無日期的版本（除了特別指定WCAG 2.0版的適用性標準）。

01-Feb-2021: 變更對媒體覆蓋的推薦，將符合EPUB規格規定作為一項規定。請見issue 1486。

17-Nov-2020: 為certifierCredential及certifierReport特性新增refines屬性以及範例。請見issue 1410。

16-Nov-2020: 從發現性章節移除選擇性的無障礙附註性控制以及API詮釋資料參考資料。這些詮釋資料特性更適合用在閱讀系統上。請見issue 1327。

26-Sept-2020: 無障礙輔助性1.0規格的改版將被發布作為一項ISO標準，並初始草稿文字。

## C. 致謝

本章節為非規範性。

以下EPUB 3工作小組的成員對本規格的產製有所貢獻：

Juliette Alexandria (Access2online Inc.)
Luc Audrain (W3C Invited Expert)
Will AWAD (Newgen Knowledgeworks)
Sofia Bautista (Legible Media Inc.)
Laura Brady (W3C Invited Expert)
Leah Brochu (National Network for Equitable Library Service)
Matthew C. Chan (House of Anansi Press)
Yu-Wei Chang (Taiwan Digital Publishing Forum)
Fred Chasen (Scribd)
Garth Conboy (Google LLC)
Juan Corona (Legible Media Inc.)
Dave Cramer (W3C Invited Expert, chair)
Romain Deltour (DAISY Consortium)
Marisa DeMeglio (DAISY Consortium)
Brady Duga (Google LLC)
Reinaldo Ferraz (NIC.br - Brazilian Network Information Center)
John Foliot (W3C Invited Expert)
Teenya Franklin (Pearson plc)
Hadrien Gardeur (EDRLab)
Matt Garrish (DAISY Consortium)
Jen Goulden (Crawford Technologies)
Ivan Herman (W3C, staff contact)
Tetsu Hoshino (Kodansha, Publishers, Ltd.)
Norikazu Ishizu (Kadokawa Corporation)
Norihito IYENAGA (Kodansha, Publishers, Ltd.)
Ken Jones (Circular Software)
Deborah Kaplan (W3C Invited Expert)
Bill Kasdorf (Book Industry Study Group)
George Kerscher (DAISY Consortium)
Kazuhito Kidachi (Mitsue-Links Co., Ltd.)
Masakazu Kitahara (Voyager Japan, Inc.)
Toshiaki Koike (Voyager Japan, Inc.)
Ryo Kuroda (ACCESS CO., LTD.)
Charles LaPierre (Benetech)
Dan Lazin (Google LLC)
Laurent Le Meur (EDRLab)
Farrah Little (National Network for Equitable Library Service)
Karan Malhotra (Newgen Knowledgeworks)
Makoto Murata (DAISY Consortium)
Cristina Mussinelli (Fondazione LIA)
Yoichiro Nagao (Kodansha, Publishers, Ltd.)
Yoshinori Ohmura (SHUEISHA Inc.)
Rachel Osolen (National Network for Equitable Library Service)
Gregorio Pellegrino (Fondazione LIA)
Vijaya Gowri Perumal (Newgen Knowledgeworks)
Wendy Reid (Rakuten, Inc., chair)
Leonard Rosenthol (Adobe)
Shinobu Sato (Kadokawa Corporation)
Ben Schroeter (Pearson plc)
Daihei Shiohama (MEDIA DO Co., Ltd.)
Tzviya Siegman (Wiley)
Avneesh Singh (DAISY Consortium)
MOTOI SUZUKI (SHUEISHA Inc.)
Yutaka Suzuki (Kadokawa Corporation)
Kyrce Swenson (Pearson plc)
Shinya Takami (Kadokawa Corporation, chair)
Mateus Teixeira (W. W. Norton & Company)
Yukio Tomikura (Kodansha, Publishers, Ltd.)
Aimee Ubbink (Crawford Technologies)
Daniel Weck (DAISY Consortium)
Zheng Xu (Gardenia Corp, Rakuten, Inc.)
Fuqiao Xue (W3C)
Evan Yamanishi (W. W. Norton & Company)
Osamu Yoshiba (Kodansha, Publishers, Ltd.)
Junichi Yoshii (Kodansha, Publishers, Ltd.)
Naomi Yoshizawa (W3C)

## D. 參考資料

### D.1 規範性文件

[DCTERMS]
	DCMI Metadata Terms. DCMI Usage Board. DCMI. 20 January 2020. DCMI Recommendation. URL: https://www.dublincore.org/specifications/dublin-core/dcmi-terms/

[EPUB-3]
	EPUB 3. W3C. URL: https://www.w3.org/TR/epub/

[RFC2119]
	Key words for use in RFCs to Indicate Requirement Levels. S. Bradner. IETF. March 1997. Best Current Practice. URL: https://www.rfc-editor.org/rfc/rfc2119

[RFC8174]
	Ambiguity of Uppercase vs Lowercase in RFC 2119 Key Words. B. Leiba. IETF. May 2017. Best Current Practice. URL: https://www.rfc-editor.org/rfc/rfc8174

[schema-org]
	Schema.org. W3C Schema.org Community Group. W3C. 6.0. URL: https://schema.org/

[WCAG2]
	Web Content Accessibility Guidelines (WCAG) 2. W3C. URL: https://www.w3.org/TR/WCAG2/

[WCAG20]
	Web Content Accessibility Guidelines (WCAG) 2.0. Ben Caldwell; Michael Cooper; Loretta Guarino Reid; Gregg Vanderheiden et al. W3C. 11 December 2008. W3C Recommendation. URL: https://www.w3.org/TR/WCAG20/

### D.2 參考性文件 

[DAISYAudio]
	Navigable audio-only EPUB 3 Guidelines. URL: http://www.daisy.org/guidelines/epub/navigable-audio-only-epub3-guidelines

[EPUB-A11Y-10]
	EPUB Accessibility 1.0. Matt Garrish; George Kerscher; Charles LaPierre; Avneesh Singh. IDPF. 05 January 2017. URL: http://idpf.org/epub/a11y/accessibility-20170105.html

[EPUB-A11Y-TECH-11]
	EPUB Accessibility Techniques 1.1. Matt Garrish; George Kerscher; Charles LaPierre; Gregorio Pellegrino; Avneesh Singh. W3C. 30 September 2021. W3C Note. URL: https://www.w3.org/TR/epub-a11y-tech-11/

[MARC21]
	MARC 21 XML. URL: https://www.loc.gov/standards/marcxml/

[ONIX]
	ONIX for Books 3.0. URL: https://www.editeur.org/8/ONIX/

[OPF-201]
	Open Packaging Format 2.0.1. IDPF. 04 September 2010. URL: http://www.idpf.org/epub/20/spec/OPF_2.0.1_draft.htm

[URL]
	URL Standard. Anne van Kesteren. WHATWG. Living Standard. URL: https://url.spec.whatwg.org/

[WCAG]
	Web Content Accessibility Guidelines 1.0. Wendy Chisholm; Gregg Vanderheiden; Ian Jacobs. W3C. 5 May 1999. W3C Recommendation. URL: https://www.w3.org/TR/WAI-WEBCONTENT/