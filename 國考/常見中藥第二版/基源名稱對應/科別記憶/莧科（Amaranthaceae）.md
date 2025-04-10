---
category: 中藥生藥學
tags:
  - 中藥科別
  - 莧科
created: 2025-03-21
updated: 2025-04-08 09:27
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-01
sr-interval: 24
sr-ease: 250
---
#首刷 #review
>一種中藥材
### 1.概念
- **莧科（Amaranthaceae）** 是一類**由草本、灌木甚至部分喬木組成的雙子葉植物科**，廣泛分布於全球熱帶至溫帶地區，尤其常見於**乾燥、鹽鹼土或貧瘠地區**。  
- 本科植物多具**抗旱、抗鹽能力強、莖葉富含營養或藥用成分**的特性，部分種類可作為**糧食作物、蔬菜、飼料、藥材與觀賞植物**。  
- 代表植物包括：  
  - **莧菜（Amaranthus spp.）**：可食用與藥用，富含鐵與膳食纖維  
  - **青葙（Celosia argentea）**：中藥青葙子，有清肝明目之效  
  - **藜（Chenopodium spp.）**：如藜麥（Quinoa），現代營養食品中的超級穀物之一  

### 2.詞素拆解
- **Amaranth-**  
  來自希臘文 *amarantos*（ἀμάραντος），意為「不凋謝的、不枯萎的」  
  - *a-*：否定前綴，表示「不」  
  - *maraino*：枯萎、凋零  
  - *Amaranthus*（莧屬）：模式屬名稱，形容其花序**色彩鮮艷、持久不凋的特性**  
  - 在文學與神話中，*amaranth* 常象徵「==永恆之花==」   

- **-aceae**  
  植物科名標準後綴，表示某植物分類為「科」  

**完整結構：**
- **Amaranthaceae** = *Amaranth-*（不凋花屬名 Amaranthus）+ *-aceae*（植物科後綴）  
→ 指與 **莧屬（Amaranthus）** 相關的整個植物科，即「莧科」。其成員通常具有**耐旱、耐鹽、花期長、藥食兼用等特性**，不僅是**傳統蔬菜與中藥來源**，也是**現代健康飲食與糧食替代研究的重要對象**。  

#### 📌 相關藥材連結


```dataviewjs
const excludeTags = ["中藥科別","中藥生藥學"];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

let allCandidates = dv.pages()
  .where(p => p.tags && p.file.name !== dv.current().file.name);

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




### 3.莧科（Amaranthaceae） 相關知識點

- **Amaranth-**  
  來自希臘文 *amarantos*（ἀμάραντος），意為「不凋謝的、不枯萎的」  
  - *a-*：否定前綴，表示「不」  
  - *maraino*：枯萎、凋零  


### 4.閃卡區

- *a-*::否定前綴，表示「不」 

- *maraino*::枯萎、凋零 

- 莧科::（Amaranthaceae） <!--SR:!2025-03-30,4,270!2025-03-30,4,270-->