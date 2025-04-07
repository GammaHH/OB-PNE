---
category: 中藥生藥學
tags:
  - 中藥科別
  - 麻黃科
created: 2025-03-21
updated: 2025-04-06 21:36
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-29
sr-interval: 23
sr-ease: 250
---
#首刷 #review
> 一種中藥材
### 1. 概念
- **麻黃科（Ephedraceae）** 是一類**主要由灌木或亞灌木組成的裸子植物科**，其成員多數含有**生物鹼**，具有**藥用價值**，廣泛應用於**中藥**。代表植物包括 **草麻黃（Ephedra sinica）、木賊麻黃（Ephedra equisetina）、中麻黃（Ephedra intermedia）**。 

- **主要藥用特性：**  
  - **發汗解表**：如 **草麻黃（Ephedra sinica）**，富含**麻黃鹼（ephedrine）**，可**發汗解表、宣肺平喘**，適用於感冒風寒、咳嗽氣喘等症狀。 

  - **利尿消腫**：如 **木賊麻黃（Ephedra equisetina）**，含有**偽麻黃鹼（pseudoephedrine）**，可**利尿消腫**，適用於水腫、小便不利等症狀。 

  - **止咳平喘**：如 **中麻黃（Ephedra intermedia）**，含有**麻黃鹼**，可**止咳平喘**，適用於咳嗽、氣喘等症狀。 

### 2. 詞素拆解

- **Ephedr-**（來自拉丁文 *Ephedra*，意為「麻黃屬」）  
  - **Ephedra**（麻黃屬）：代表麻黃科的模式屬，如 **Ephedra sinica（草麻黃）**，以其藥用價值聞名。 

- **-aceae**（植物科名標準後綴）  

**完整結構：**

- **Ephedraceae = *Ephedr-*（麻黃屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **麻黃屬（Ephedra）** 相關的整個植物科，即「麻黃科」，其成員通常具有(3)**==發汗解表、利尿消腫、止咳平喘==的藥用價值**，並廣泛應用於**中藥**。 

#### 📌 相關藥材連結


```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["中藥科別"];
const currentTags = dv.current().tags?.filter(t => !excludeTags.includes(t)) ?? [];

let tagMatches = dv.pages()
  .where(p => p.tags && p.file.name !== dv.current().file.name)
  .filter(p => p.tags.some(tag => currentTags.includes(tag)));

let tagGroups = {};

for (let tag of currentTags) {
  tagGroups[tag] = tagMatches.filter(p => p.tags.includes(tag));
}

let totalMatched = Object.values(tagGroups).reduce((acc, pages) => acc + pages.length, 0);

if (totalMatched > 0) {
  dv.header(5, `相關藥物（共 ${totalMatched} 筆）`);
  for (let [tag, pages] of Object.entries(tagGroups)) {
    if (pages.length > 0) {
      dv.header(6, `▸ ${tag}（${pages.length}）`);
      dv.list(
        pages.map(p => p.file.link)
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}
````

### 3.麻黃科（Ephedraceae） 相關知識點




### 4.閃卡區


