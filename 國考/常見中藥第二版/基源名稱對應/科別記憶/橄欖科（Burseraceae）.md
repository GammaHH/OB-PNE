---
category: 中藥生藥學
tags:
  - 中藥科別
  - 橄欖科
created: 2025-03-21
updated: 2025-04-08 09:27
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-08
sr-interval: 30
sr-ease: 270
---
> 一種中藥材
### 1.概念
- **橄欖科（Burseraceae）** 是一類**主要由熱帶與亞熱帶地區的喬木或灌木組成的雙子葉植物科**，廣泛分布於**非洲、美洲熱帶與東南亞地區**。  
- 本科植物最具特徵的是其**樹幹或樹皮富含芳香樹脂（如==乳香、沒藥==）**，常用於**薰香、製香水、藥用、宗教儀式與保健品**，具有重要的**藥理與經濟價值**。 
  
- 代表植物包括：  
  - **乳香樹（Boswellia spp.）**：產出乳香（Frankincense）  
  - **沒藥樹（Commiphora spp.）**：產出沒藥（Myrrh）  
  - **Bursera spp.**：屬名來自本科名稱，產樹脂且具香氣  

### 2.詞素拆解
- **Burser-**  
  源自模式屬 *Bursera*，以瑞典植物學家 **Joachim Burser**（1583–1639）命名，以表彰其對植物研究的貢獻。  
  - **Bursera**：為本科的命名依據與典型屬，分布於中美洲，樹皮具香氣與藥用樹脂  
  - 此屬命名屬於「人名獻名型」，並非源自拉丁／希臘語詞根  

- **-aceae**  
  植物科名標準後綴，表示某某植物科的分類單元  

**完整結構：**
- **Burseraceae** = *Burser-*（紀念 Joachim Burser 的屬名 Bursera）+ *-aceae*（植物科後綴）  
→ 指與 **Bursera 屬** 相關的整個植物科，即「橄欖科」，其成員多為**富含芳香樹脂的熱帶喬木或灌木**，尤以**乳香與沒藥**為代表，廣泛應用於**藥用、保健、香料與宗教儀式**中，為人類文明史上極具地位的植物類群之一。  


#### 📌 相關藥材連結


```dataviewjs
const excludeTags = ["中藥科別","中藥生藥學"];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

let allCandidates = dv.pages()
  .where(p => p.file?.path?.startsWith("國考/") && p.tags && p.file.name !== dv.current().file.name);


// 先分出 multi 和 single
let multiMatch = [];
let singleMatch = [];

for (let p of allCandidates) {
  const matchCount = currentTags.reduce((acc, tag) => acc + (p.tags.includes(tag) ? 1 : 0), 0);
  if (matchCount >= 2) {
    multiMatch.push(p);
  } else if (matchCount === 1) {
    singleMatch.push(p);
  }
}

// 建立 singleMatch 的分類 group
let singleGroups = {};
for (let p of singleMatch) {
  let matchedTag = currentTags.find(tag => p.tags.includes(tag));
  if (matchedTag) {
    if (!singleGroups[matchedTag]) singleGroups[matchedTag] = [];
    singleGroups[matchedTag].push(p);
  }
}

// 合併總筆數（無重複）
let multiPaths = new Set(multiMatch.map(p => p.file.path));
let totalUnique = new Set([...multiMatch, ...singleMatch].map(p => p.file.path)).size;

dv.header(5, `相關藥物（共 ${totalUnique} 筆）`);

if (multiMatch.length > 0) {
  dv.header(6, `▸ ${currentTags.join("、")}（${multiMatch.length}）`);
  dv.list(
    multiMatch.map(p => {
      const tagsToShow = p.tags.filter(t => !excludeTags.includes(t));
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}

// 顯示單一標籤命中分類後的筆記
for (let [tag, pages] of Object.entries(singleGroups)) {
  dv.header(6, `▸ ${tag}（${pages.length}）`);
  dv.list(
    pages.map(p => {
      const tagsToShow = p.tags.filter(t => !excludeTags.includes(t) && t !== tag);
      return `${p.file.link}　${tagsToShow.join("、")}`;
    })
  );
}
if (multiMatch.length === 0 && Object.keys(singleGroups).length === 0) {

  dv.paragraph("沒有找到與本藥材具有相同標籤的其他筆記。");
}

```



### 3.橄欖科（Burseraceae） 相關知識點

- **Burser-**  
  源自模式屬 *Bursera*，以瑞典植物學家 **Joachim Burser**（1583–1639）命名，以表彰其對植物研究的貢獻。  
  - **Bursera**：為本科的命名依據與典型屬，分布於中美洲，樹皮具香氣與藥用樹脂  
  - 此屬命名屬於「人名獻名型」，並非源自拉丁／希臘語詞根  


### 4.閃卡區

- 橄欖科:::（Burseraceae） 


- **Burser-**  、橄欖科（Burseraceae）
??
  源自模式屬 *Bursera*，以瑞典植物學家 **Joachim Burser**（1583–1639）命名，以表彰其對植物研究的貢獻。  
  - **Bursera**：為本科的命名依據與典型屬，分布於中美洲，樹皮具香氣與藥用樹脂  
  - 此屬命名屬於「人名獻名型」，並非源自拉丁／希臘語詞根 <!--SR:!2025-03-30,3,267!2025-04-04,8,250-->  