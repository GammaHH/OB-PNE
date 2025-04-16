---
created: 2025-03-25 12:01
updated: 2025-04-14 18:03
---
d# General-企劃
1. 從網路上輸入題目(阿摩)
2. 貼上題目 + 解析 餵AI讓他輸出固定格式[[#GPT桌面版]]
	- 如果有圖片的話需要手動輸入圖片
	- **結束後需要檢查原題目有沒有圖片**
3. 進行閃卡練習及不斷修正筆記備註(邊做題邊修正)[[#Spaced Repetition]]
4. 反覆進行
5. [ ] 多工協作與合併(可選)[[#(選)多工協作與合併[Obsidian git]、[Github Desktop]]]
6. 專案追蹤[Updated time on edit] 
- 外觀、字體設置(暗黑模式不傷眼/自訂義外觀)[隨峰體]、[外觀瀏覽>Prism, Style settings設定分享]  [[#(選)外觀、字體設置]]

1. [ ] 工作流配置選項[Outliner]、[Better Export PDF] - 直接安裝就有用，需要學一下快捷鍵
2. [ ] [[#(選)自帶背景音樂配置[Soundscapes]]]
3. [ ] 自定義Callout、管理Callout輸入[Callout manager] - 這個提示有相關指引

- [[#(選)個人辭典[Various Complement]]] - 設定好就能用，提示有寫
- 自定義目錄/搜尋腳本[Dataview/Dataviewjs] - 這個之後才會用到，會搭配GPT進行編譯




# 貼上題目 + 解析
- 搜尋考卷

```
藥劑學 專技高考
```
![[Pasted image 20250325220953.png]]
- 複製範圍
![[Pasted image 20250325184506.png]]
- 將題目加在[[#Prompt]]後面(第一批訊息要prompt，後面理論上不用)
- 因為最近AI好像被限速了，所以可以先建立複製框用來複製(**此步驟參見提示的模板插件安裝及設定篇**)
![[Pasted image 20250325222259.png]]
- 上圖中使用的模板(記得找我要)，可以從旁邊的索引欄中顯示
![[Pasted image 20250325222546.png]]
- 將訊息依序丟入AI中...
- 進行整體檢查(此步驟可以連動[Custom frames])，記得要註冊阿摩歐！
![[Pasted image 20250325224337.png]]
- 逐一貼上阿摩的免費詳解，或是打上自己的理解
- **享受 Space repetition 帶來的效益及打亂順序的詞卡們**

##### 題目
- **需要事先告知年分**
![[Pasted image 20250325192004.png]]
- 如果題目輸出對了記得**按讚**
![[Pasted image 20250325192032.png]]
- 題目之間一定要有換行
- **一次給10題**對於整理階段算是最高效率，但如果要生成詳解的話建議一次一題
- 複選題需要標示在題號後面，像這樣

##### 113-1(32) (**複選題**)
```Question
有關「崩散度試驗」之敘述，下列何者錯誤？
```  
(A) 維持37±0.5℃恆溫，篩網為20號篩  
(B) 網架升降頻率每分鐘29～32週期  
(C) 網架提升高度為5.3～5.7公分  
(D) 篩網應浸在液面下2.5公分  
?  
答案：A,D  
說明：  
##### 解析
- 後面再加上解析

###### Prompt(請這邊整個複製)

請完全依照以下格式產生題目：
題目格式：
##### (年份，像是113-1、114-2)(題號，是題目內容一開始的編號)113-1(1) (如果是複選題需要在年份和題號後面加上"(**複選題**)")
```Question
(題幹，像是)甘油之密度為1.25 g/mL，量取1 kg之甘油，其體積為若干？
```
(A) 80 cL
(B) 80 dL
(C) 125 dL
(D) 125 cL
?(必須要有問號在這)
答案：A
說明：(這邊不需要產生內容)
(這邊必需要換行)
???(必須要有三個問號在這)
(兩題之間不需要有分隔線)

需要加工的題目內容：


###### 示例：正確的格式應該要像是這樣

當然可以，以下是根據你提供的新格式，整理後的三題題目：  

##### 113-1(3)  
```Question
「Phenobarbital elixir」配方中，添加 glycerin 之主要目的為何？
```  
(A) 增進 phenobarbital 之溶解度  
(B) 作為保濕劑以減少水分蒸發  
(C) 提供防腐效果避免微生物孳生  
(D) 作為甜味劑以增進口感  
?  
答案：A  
說明：  

##### 113-1(4)  
```Question
依據中華藥典之規定，下列醑劑何者是以蒸餾法製備？
```  
(A) 複方橙皮醑（compound orange spirit）  
(B) 芳香氨醑（aromatic ammonia spirit）  
(C) 薄荷醑（peppermint spirit）  
(D) 芳香醑（aromatic spirit）  
?  
答案：D  
說明：  

##### 113-1(5)  
```Question
Isopropyl rubbing alcohol於一般非特定對象使用最適當之濃度為何？
```  
(A) 60%  
(B) 70%  
(C) 80%  
(D) 91%  
?  
答案：B  
說明：

###### 示例：正確的`輸入`格式應該要像是這樣
###### 21
```
(這前面是Prompt)

21.經皮給藥後，由外層到深層，依序要經過那些細胞層？①stratum corneum ②stratum lucidum ③stratum granulosum ④stratum spinosum ⑤stratum germinativum
(A) ①②③④⑤
(B) ①③②④⑤
(C) ①④③⑤②
(D) ②①④③⑤
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：A22.祕魯香膠（Peru balsam）應先與下列何種成分研合，再添加入軟膏基劑？
(A) 蓖麻油
(B) 甜杏油
(C) 棉籽油
(D) 礦物油
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：A23.實務上，進行噴霧乾燥時，若提高乾燥溫度，下列敘述何者最適當？
(A) 粉末易黏結使顆粒變大
(B) 不影響顆粒大小
(C) 顆粒較易粉碎
(D) 粉末黏結使沉降速度加快
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：C24.疏水性藥物製備為硬膠囊劑時，可於配方中添加輔助成分，以減少藥物在腸中結塊而不易擴散之現象，下列 何者不具此作用？
(A) sodium starch glycolate
(B) sodium lauryl sulfate
(C) methylcellulose
(D) croscarmellose
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：C複選題
25.有關硬膠囊劑之敘述，下列何者最適當？
(A) 可以充填某些液體成分，例如脂肪油或揮發油
(B) 所謂適當之充填，通常係指其粉粒能填滿至膠囊蓋
(C) 正常的膠囊殼含 6～10%的水分
(D) 一般膠囊殼呈透明狀，通常係因其殼內含明膠、水、蔗糖、及甘油所致
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：AD26.下列何種研磨機，研磨過程最適用於對熱不安定的藥品？
(A) 錘擊式粉碎機（impact crushers）
(B) 顎式粉碎機（jaw crusher）
(C) 流能磨（fluid-energy mill）
(D) 球磨機（ball mill）
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：C27.有關發泡顆粒劑之敘述，下列何者最適當？
(A) 應貯存於易開啟之廣口容器中
(B) 基本成分常包含酒石酸、檸檬酸及碳酸鈉
(C) 對於鹽類性藥品通常具矯味作用
(D) 主成分通常為難溶性藥品
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：C28.有關散劑與顆粒劑的比較，下列敘述何者最不適當？
(A) 於靜置時，顆粒劑通常較不易結塊或硬化
(B) 於大氣中，顆粒劑通常較不易受潮
(C) 顆粒劑的表面積比相同體積的粉末小，因此不容易濕潤再製成其他劑型
(D) 顆粒劑通常比散劑容易製成溶液劑或懸浮劑
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：C29.下列何者不需要執行崩散度試驗？
(A) 延遲釋放腸溶膜衣錠（delayed-release enteric-coated tablets）
(B) 舌下錠（sublingual tablets）
(C) 口腔片（buccal tablets）
(D) 於規定間隔時間分次釋離藥品之錠劑（extended-release dosage forms）
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：D30.下列何種錠片劑型在高程度壓錠（a high degree of compression）下完成製備，使其可以緩慢溶解釋出活性成 分？
(A) enteric-coated granular tablet
(B) chewable tablet
(C) lozenge tablet
(D) sublingual tablet
專技 - 藥劑學(包括生物藥劑學)#3222 -112年 - 112-1 專技高考_藥師(一)：藥劑學與生物藥劑學#113163
答案：C
```


# 詳細執行步驟解說

### [GPT桌面版]
- 下載網址-**微軟商城**
https://apps.microsoft.com/detail/9NT1R1C2HH7J?hl=neutral&gl=TW&ocid=pdpshare


### [Spaced Repetition]
>一個OB插件：分為卡片和筆記複習兩種，該插件會為你自動排程該複習的項目，進行反轉卡片或筆記複習。
>- 可搭配快捷鍵實現無限次複習，潛力無窮


- 下載啟用後，進入配置

> 共有兩種複習系統： 1. 卡片 2.筆記
##### 卡片
![[Pasted image 20250325151940.png]]

1. 用`貼上`的方式輸入分組標籤(不輸入也可以)，這部分我沒用他也會自動幫我偵測卡片(**把*下面的選項打開*就可以不用輸入標籤**，但會依照資料夾結構進行分組)所以==筆記一定要放入資料夾中才讀得到==，在同一資料夾的筆記視為同一卡組
2. 同樣也是用貼上的方式進行編輯
	- 排序部分我建議亂序
	- 後面為自訂義選項，依照自己習慣改(可以用尋找與取代功能修正)

##### 筆記
![[Pasted image 20250325153838.png]]

3. 忽略資料夾部分我建議要把模板類資料夾忽略
4. 建議開啟
5. 建議開啟，不然要設置快捷鍵，然後每天複習完之後要關掉，不然分頁會越累積越多('''O$_>$O)
- 對了需要事先將需要複習的筆記加上 `#review` 標籤才行(也可以自訂標籤)

##### Scheduling
![[Pasted image 20250325162844.png]]


##### User Interface
![[Pasted image 20250325163119.png]]
- 高度80


##### 相關快捷設定(可選，也可手動輸入)
- 進入快捷鍵
- 在輸入欄輸入 `Spaced Repetition`
![[Pasted image 20250325181823.png]]

##### 實機介面
- 筆記複習
![[Pasted image 20250325154743.png]]

- 翻轉卡片介面(閃卡, Flashc cards, Anki)
1. 先打開 ribbons 中的複習卡片
2. 選擇要複習的卡組
3. 複習吧！


![[Pasted image 20250325164203.png]]

![[Pasted image 20250325164318.png]]
4. 可以直接在介面中進行編輯
![[Pasted image 20250325164310.png]]

### 專案追蹤[Updated time on edit]
> 一個紀錄檔案創建時間和修改時間的插件

- 設置如下：
1. 全域設定應排除的資料夾
2. 開啟記錄創建時間的功能和設定其 Front-matter 變數 `created`、`updated`
3. 按下 Update all files 將 Front-matter 加入至所有檔案中

![[Pasted image 20250325181120.png]]

### (選)多工協作與合併[Obsidian git]、[Github Desktop]
>Obsidian git 現已改名成 Git ，為 Github Desktop 在Obsidian 的UI接口，方便使用者進行常規更新

> Github Desktop 為 Github 的桌面應用程式，專門為了 .md 等程式碼文件設計的版本控制軟體，可以自由回復任一尚未儲存的段落

- 這個步驟有點麻煩，而且目前只被我用在單人備分用，沒有試過多人協作，需要找時間測一下

### (選)自帶背景音樂配置[Soundscapes]
> 為筆記軟體添加背景音樂的東西，僅支援YT和本地資料

- ID部分為網址的尾碼
![[Pasted image 20250325181459.png]]

![[Pasted image 20250325181557.png]]

### (選)外觀、字體設置
##### 字體設置
> 隨峰體安裝，就直接打開來裝就是了。裝完從外觀中調整，像這樣

![[Pasted image 20250325182910.png]]
- 編輯器建議開啟選項：
![[Pasted image 20250325183005.png]]

##### 外觀
> 我採用的是 Prism 深藍模式，沒有採用原來的標題顏色配置，相關設定值如下
- 記得還要安裝 Style settings 插件才會運行歐！
```
{
  "obsidian-prism-theme@@pt-fade-inactive-tabs": true,
  "obsidian-prism-theme@@pt-icons-accent": true,
  "obsidian-prism-theme@@color-schemes-dt": "pt-color-scheme-indigo-dt",
  "obsidian-prism-theme@@color-scheme-style-dt": "pt-color-scheme-style-border-dt",
  "obsidian-prism-theme@@dark-accent-color-preset": "pt-accent-color-purple-dt",
  "obsidian-prism-theme@@highlight-text-accent-dt": "pt-highlight-text-custom-dt",
  "obsidian-prism-theme@@highlight-text-accent-custom-dt": "#FFD800",
  "obsidian-prism-theme@@color-accent-text-dt": "#D2FF00",
  "obsidian-prism-theme@@color-accent-tint-dt": "#FFFF00",
  "obsidian-prism-theme@@color-accent-base-dt": "#FFD800",
  "obsidian-prism-theme@@pt-focused-mode": true,
  "obsidian-prism-theme@@focused-mode-style": "pt-focused-style-popout-only",
  "obsidian-prism-theme@@text-italic-color-dt": "var(--color-orange-text)",
  "obsidian-prism-theme@@text-bold-color-dt": "var(--color-yellow-text)",
  "obsidian-prism-theme@@graph-line-color-dt": "var(--color-mint-text)",
  "obsidian-prism-theme@@graph-line-custom-color-dt": "#0080FF",
  "obsidian-prism-theme@@graph-unresolved-color-dt": "var(--color-orange-text)",
  "obsidian-prism-theme@@graph-unresolved-custom-color-dt": "#FFB900",
  "obsidian-prism-theme@@inline-title-color-dt": "var(--text-normal)",
  "obsidian-prism-theme@@h1-text-color-dt": "var(--color-cyan-text)",
  "obsidian-prism-theme@@h2-text-color-dt": "var(--color-mint-text)",
  "obsidian-prism-theme@@h3-text-color-dt": "var(--color-green-text)",
  "obsidian-prism-theme@@h4-text-color-dt": "var(--color-yellow-text)",
  "obsidian-prism-theme@@h5-text-color-dt": "var(--color-orange-text)",
  "obsidian-prism-theme@@h6-text-color-dt": "var(--color-pink-text)",
  "obsidian-prism-theme@@pt-colored-folders": true,
  "obsidian-prism-theme@@graph-tag-color-dt": "var(--graph-tag-custom-color-dt)",
  "obsidian-prism-theme@@graph-tag-opacity-dt": 1,
  "obsidian-prism-theme@@text-italic-bold-color-dt": "var(--color-red-text)",
  "obsidian-prism-theme@@dark-mark-highlight-text-color-preset": "pt-highlight-text-default-dt",
  "obsidian-prism-theme@@graph-highlight-line-color-lt": "var(--graph-highlight-line-custom-color-lt)",
  "obsidian-prism-theme@@pt-status-bar-style": "pt-status-bar-position-fixed",
  "obsidian-prism-theme@@graph-highlight-line-custom-color-lt": "#FFC666",
  "obsidian-prism-theme@@graph-fill-focused-color-dt": "var(--interactive-accent-text)",
  "obsidian-prism-theme@@dark-mark-highlight-style": "pt-highlight-style-borderandfilled-dt",
  "obsidian-prism-theme@@graph-highlight-line-opacity-lt": 0.6,
  "obsidian-prism-theme@@graph-highlight-opacity-dt": 1,
  "obsidian-prism-theme@@graph-highlight-line-opacity-dt": 0.6,
  "obsidian-prism-theme@@pt-disable-mark-highlight-styling": true,
  "obsidian-prism-theme@@graph-highlight-line-color-dt": "var(--graph-highlight-line-custom-color-dt)",
  "obsidian-prism-theme@@graph-highlight-color-dt": "var(--graph-highlight-custom-color-dt)",
  "obsidian-prism-theme@@graph-highlight-custom-color-dt": "#FFD000",
  "obsidian-prism-theme@@graph-highlight-line-custom-color-dt": "#FFD000",
  "obsidian-prism-theme@@light-mark-highlight-text-color-preset": "pt-highlight-text-default-lt"
}
```

- CSS檔案安裝
就直接把附帶的 snippets 資料夾丟到 .Obsidian就可以了
![[Pasted image 20250325183507.png]]


### (選)個人辭典[Various Complement]
> 快速輸入和自訂義個人辭典

- 設定因個人而異，需要自己設置快捷鍵