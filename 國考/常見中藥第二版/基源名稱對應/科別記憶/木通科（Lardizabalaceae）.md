---
category: 中藥生藥學
tags:
  - 中藥科別
  - 木通科
created: 2025-03-21
updated: 2025-04-07 19:45
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-30
sr-interval: 23
sr-ease: 250
---
#首刷 #review

> 一種中藥材
### 1.概念
Lar-di-za-ba-la-ceae
- **木通科（Lardizabalaceae）** 是一類**主要由木質藤本或灌木組成的雙子葉植物科**，大多數物種分布於**東亞（特別是中國、日本、韓國）與南美的溫帶至亞熱帶地區**。  
- 該科植物常具有**攀緣性、堅韌的莖、革質葉片與具藥用或食用價值的果實**，例如中藥常用的 **木通（Akebia quinata）**。  

- **藥用特性與應用特點：**  
  - **清熱利尿**：如木通，具有通淋利尿作用，用於濕熱所致的小便不利、淋證。  
  - **通絡止痛**：活血通經，常用於風濕痹痛、月經不調等。  
  - **潤腸通便**：果實含糖量高，有潤腸效果；部分種子含油，可入藥或食用。  

### 2. 詞素拆解

- **Lardizabal-**：來自植物學命名傳統，以18世紀西班牙外交官兼植物愛好者 **Miguel de Lardizábal y Uribe** 命名的模式屬 **Lardizabala** 為詞源  
  - **Lardizabala**：拉丁化專有名詞，用於命名該屬植物
  - 該屬植物如 *Lardizabala biternata* 為南美原生的攀緣植物，有觀賞與食用價值

- **-aceae**：植物科名標準後綴  
  - 用於構成所有被子植物科名（如 Rosaceae、Fabaceae、Asteraceae 等）



**完整結構：**  
- **Lardizabalaceae = Lardizabal-（紀念人名 Lardizábal）+ -aceae（植物科後綴）**  
- **意義**：指與 Lardizabala 屬相關的植物科，即「木通科」，包含多種攀緣性灌木或藤本植物，兼具藥用、觀賞與食用價值。

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



### 3.木通科（Lardizabalaceae） 相關知識點




### 4.閃卡區


- 木通科:::（Lardizabalaceae） <!--SR:!2025-03-28,1,210!2025-04-04,8,250-->


- **Lardizabal-**、木通科（Lardizabalaceae）
??
- 來自植物學命名傳統，以18世紀西班牙外交官兼植物愛好者 **Miguel de Lardizábal y Uribe** 命名的模式屬 **Lardizabala** 為詞源  
  - **Lardizabala**：拉丁化專有名詞，用於命名該屬植物
  - 該屬植物如 *Lardizabala biternata* 為南美原生的攀緣植物，有觀賞與食用價值 <!--SR:!2025-03-29,2,230!2025-04-28,21,270-->