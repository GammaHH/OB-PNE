---
category: 中藥生藥學
tags:
  - 中藥科別
  - 遠志科
created: 2025-03-20
updated: 2025-04-07 19:45
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-02
sr-interval: 25
sr-ease: 250
---
 #review 
>一種中藥材
### 1.概念
- **遠志科（Polygalaceae）** 是一類**以草本、灌木或少數喬木為主的雙子葉開花植物科**，其中許多成員具有**生物鹼與皂苷類化合物**，常用於**藥用、保健與園藝**。代表植物包括 **遠志（Polygala tenuifolia）、苦遠志（Polygala sibirica）、千層塔（Polygala myrtifolia）**。  
- **主要藥用特性：**  
  - **安神益智**：如 **遠志（Polygala tenuifolia）**，富含**遠志皂苷（Onjisaponins）與生物鹼**，可**寧心安神、益智健腦**，適用於失眠、健忘、神經衰弱。  
  - **祛痰止咳**：如 **苦遠志（Polygala sibirica）**，含有**三萜皂苷與揮發油**，可**溫肺化痰、鎮咳平喘**，適用於咳嗽痰多、氣喘。  
  - **抗炎消腫**：如 **千層塔（Polygala myrtifolia）**，富含**黃酮與多酚類**，可**清熱解毒、抗菌抗炎**，適用於感染性炎症與腫脹疼痛。  
  - **強心健脾**：部分遠志屬植物具有**強心作用**，可**促進血液循環、增強體力**，適用於脾虛乏力者。  

### 2.詞素拆解
- **Polygala-**（來自希臘文 *πολύς*（polys）「多」+ *γάλα*（gala）「奶」）  
  - **Polygala**（遠志屬）：代表遠志科的模式屬，如 **Polygala tenuifolia（遠志）**，因傳統上認為該屬植物能**促進奶牛泌乳**而得名。  
  - **Poly-**（多）：來自希臘文 *πολύς*（polys），意為「多數的」。  
  - **Gala**（奶）：來自希臘文 *γάλα*（gala），意為「乳汁」。  
  - **命名原因：** 遠志屬植物傳統上**被認為能促進奶牛泌乳**，因此以 *Polygala* 命名。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Polygalaceae = *Polygala-*（遠志屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **遠志屬（Polygala）** 相關的整個植物科，即「遠志科」，其成員通常具有**健腦安神、祛痰止咳、促進泌乳的藥用特性**，並廣泛應用於**中藥、保健品與園藝領域**。  

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


### 3.遠志科（Polygalaceae） 相關知識點

- **Polygala-**（來自希臘文 *πολύς*（polys）「多」+ *γάλα*（gala）「奶」）  
  - **Polygala**（遠志屬）：代表遠志科的模式屬，如 **Polygala tenuifolia（遠志）**，因傳統上認為該屬植物能**促進奶牛泌乳**而得名。  
  - **Poly-**（多）：來自希臘文 *πολύς*（polys），意為「多數的」。  
  - **Gala**（奶）：來自希臘文 *γάλα*（gala），意為「乳汁」。  


- **Polygala-**（來自希臘文 *πολύς*（polys）「X」+ *γάλα*（gala）「==奶==」）  即遠志科（Polygalaceae）詞源

- **Polygala-**（來自希臘文 *πολύς*（polys）「==多==」+ *γάλα*（gala）「X」）  即遠志科（Polygalaceae）詞源