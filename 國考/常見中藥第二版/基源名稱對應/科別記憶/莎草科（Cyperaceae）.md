---
category: 中藥生藥學
tags:
  - 中藥科別
  - 莎草科
created: 2025-03-21
updated: 2025-04-08 08:37
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-08
sr-interval: 30
sr-ease: 270
---
#首刷 #review
>一種中藥材
### 1.概念
- **莎草科（Cyperaceae）** 是一類**主要由草本植物組成的單子葉植物科**，與禾本科外觀相似，但通常具有**三稜形的莖、無節間、葉三列排列**等明顯特徵。廣泛分布於**全球濕地、水田、沼澤與草原地區**。  
- 本科植物多具有**發達的地下莖（根莖或塊莖）**，常用於**中藥、編織與環境修復**。  
- 代表藥用植物包括：  
  - **香附（Cyperus rotundus）**：為中藥常用的理氣藥，有**疏肝解鬱、調經止痛**作用  
  - **莎草（Cyperus spp.）**：部分種類用於藥用或民間療法  

### 2.詞素拆解
- **Cyper-**  
  來自拉丁文 *Cyperus*，該詞源自古希臘文 *kypeiros*（κύπειρος），意為「莎草、一種香根草」  
  - *Cyperus*：莎草屬，是該科模式屬，廣泛分布於全球熱帶與溫帶地區  
  - 詞根與古代對香草植物（如紙莎草）之稱呼有關  
  - 英文 *cyperaceous*（莎草科的）與此同源  

- **-aceae**  
  植物科名標準後綴，表示某某植物科  

**完整結構：**
- **Cyperaceae** = *Cyper-*（莎草屬名 *Cyperus*，源於希臘語「香草、莎草」）+ *-aceae*（植物科後綴）  
→ 指與 **莎草屬（Cyperus）** 相關的整個植物科，即「莎草科」，其成員常具有**三稜形莖、發達地下莖與濕地適應性**，其中部分種類如**香附**被廣泛用於中藥理氣調經，也常見於民俗編織與水土保持用途中。  

#### 📌 相關藥材連結

- [[香附]]


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


### 3.莎草科（Cyperaceae） 相關知識點

- **Cyper-**  
  來自拉丁文 *Cyperus*，該詞源自古希臘文 *kypeiros*（κύπειρος），意為「莎草、一種香根草」  
  - 英文 *cyperaceous*（莎草科的）與此同源  

### 4.閃卡區

