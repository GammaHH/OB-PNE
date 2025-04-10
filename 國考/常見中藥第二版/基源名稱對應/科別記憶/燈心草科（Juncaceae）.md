---
category: 中藥生藥學
tags:
  - 中藥科別
  - 燈心草科
created: 2025-03-21
updated: 2025-04-09 21:54
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-09
sr-interval: 30
sr-ease: 290
---
#首刷 #review
> 一種中藥材
### 1.概念
- **燈心草科（Juncaceae）** 是一類**主要由多年生草本植物組成的單子葉植物科**，常見於**濕地、沼澤或河岸地帶**。其特徵為**中空柔軟的圓柱形莖、葉細長且具鞘、花細小不顯眼**。  
- 代表藥用植物為 **燈心草（Juncus effusus）**，在中藥中常以其**莖髓**入藥，具**清心火、利尿通淋**之功效，適用於心煩失眠、小便短赤等症。 

### 2.詞素拆解
- **Junc-**  
  來自拉丁文 *juncus*，意為「燈心草、濕地草本植物」。  
  - *Juncus*（燈心草屬）：為燈心草科的模式屬，如 *Juncus effusus（燈心草）*，常見於水邊，莖細直柔軟，可作燈芯或藥用。  
  - 該詞與拉丁語 *jungere*（**結合、綁住，Junction**）同源，因古時常用此類植物來製繩或編織。  

- **-aceae**  
  植物科名標準後綴，表示「某某科」。  

**完整結構：**
- **Juncaceae** = *Junc-*（燈心草屬）+ *-aceae*（植物科後綴）  
→ 指與 **燈心草屬（Juncus）** 相關的整個植物科，即「燈心草科」，其成員多為**生於濕地的草本植物**，具**莖中空、柔軟可用作燈芯與藥材**等特性，常用於**清心火、==利尿通淋==的中藥應用**中。   

???
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



### 3.燈心草科（Juncaceae） 相關知識點




### 4.閃卡區




- **Junc-**  、燈心草科（Juncaceae）
??
  來自拉丁文 *juncus*，意為「XX」。  
  - 如 *Juncus effusus*，常見於水邊，莖細直柔軟，可作燈芯或藥用。  
  - 該詞與拉丁語 *jungere*（結合、綁住）同源，因古時常用此類植物來製繩或編織。 <!--SR:!2025-04-20,11,290!2025-04-13,4,281-->  
???