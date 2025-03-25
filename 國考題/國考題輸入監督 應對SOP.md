---
created: 2025-03-25 12:01
updated: 2025-03-25 18:18
---
# General-企劃
1. 從網路上輸入題目(阿摩)
2. 貼上題目 + 解析 餵AI讓他輸出固定格式[GPT桌面版]
	- 如果有圖片的話需要進行單題送AI轉文字
3. 進行閃卡練習及不斷修正筆記備註(邊做題邊修正)[Spaced Repetition]
4. 反覆進行
5. [ ] 多工協作與合併(可選)[Obsidian git]、[Github Desktop]
6. 專案追蹤[Updated time on edit]
- 外觀、字體設置(暗黑模式不傷眼/自訂義外觀)[隨峰體]、[外觀瀏覽>Prism, Style settings設定分享]

1. [ ] 工作流配置選項[Outliner]、[Better Export PDF]
2. [ ] 自帶背景音樂配置[Soundscapes]
3. [ ] 自訂義Callout、管理Callout輸入[Callout manager]

- 個人辭典[Various Complement]
- 自定義目錄/搜尋腳本[Dataview]




# 貼上題目 + 解析
##### 題目
- 需要告知題號年分
- 如果題目輸出對了記得按讚
- 題目之間一定要有空格
- 一次給5題比較可以確保均一度
##### 解析
- 後面再加上解析

###### Prompt

請完全依照以下格式產生題目：
題目格式：
> ###### (年份，像是113-1、114-2)(題號，是題目內容一開始的編號)**113-1(1)**
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
(該格式不需要有換行、兩題之間不需要有分隔線)

需要加工的題目內容：


###### 示例：正確的格式應該要像是這樣

當然可以，以下是根據你提供的新格式，整理後的三題題目：  

> ###### 113-1(3)  
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

> ###### 113-1(4)  
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

> ###### 113-1(5)  
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




# 詳細執行步驟解說

### [GPT桌面版]
- 下載網址-**微軟商城**
https://apps.microsoft.com/detail/9NT1R1C2HH7J?hl=neutral&gl=TW&ocid=pdpshare


### [Spaced Repetition]
>一個OB插件：分為卡片和筆記複習兩種，該插件會為你自動排程該複習的項目，進行反轉卡片或筆記複習。
>- 可搭配快捷鍵實現無限次複習，潛力無窮


- 下載啟用後，進入配置
##### 卡片
![[Pasted image 20250325151940.png]]

1. 用`貼上`的方式輸入分組標籤(不輸入也可以)，這部分我沒用他也會自動幫我偵測卡片(**把下面的打開就可以不用輸入標籤**，但會依照資料夾結構進行分組)
2. 同樣也是用貼上的方式進行編輯
	- 排序部分我建議亂序
	- 後面為自訂義選項，依照自己習慣改(可以用尋找與取代功能修正)

##### 筆記
![[Pasted image 20250325153838.png]]

3. 忽略資料夾部分我建議要把模板類資料夾忽略
4. 建議開啟
5. 建議開啟，不然要設置快捷鍵，然後每天複習完之後要關掉，不然分業會越累積越多('''O$_>$O)
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


### (選)自帶背景音樂配置[Soundscapes]
> 為筆記軟體添加背景音樂的東西，僅支援YT和本地資料

- ID部分為網址的尾碼
![[Pasted image 20250325181459.png]]

![[Pasted image 20250325181557.png]]