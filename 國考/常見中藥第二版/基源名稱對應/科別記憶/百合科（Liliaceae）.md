---
category: 中藥生藥學
tags:
  - 中藥科別
  - 百合科
created: 2025-03-20
updated: 2025-04-06 20:39
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-24
sr-interval: 18
sr-ease: 270
---
#首刷 #review 
>8種藥材
### 1.概念
- **百合科（Liliaceae）** 是一類主要分布於溫帶的**多年生草本植物**，許多成員具有**鱗莖**（如百合、鬱金香）或**根莖**（如黃精）。  
- **主要特性：**  
  - **地下器官發達**：多數具有**鱗莖、根莖或塊根**，如**百合（Lilium spp.）、黃精（Polygonatum sibiricum）**。  
  - **花朵對稱，花瓣與花萼合生**：典型代表如**鬱金香（Tulipa spp.）**。  
  - **部分植物具有藥用價值**：如**黃精（Polygonatum spp.）** 被用於滋補，**百合（Lilium spp.）** 具養陰潤肺之效。  

### 2.詞素拆解
- **Lili-**（來自拉丁文 *lilium*，意為「百合」）  
  - **Lily**（百合）：來自同一詞源，指**百合屬（Lilium）**植物。  
  - **Liliopsida**（單子葉植物綱）：以 *lilium* 命名，代表單子葉植物的典型結構，如**平行葉脈與三瓣花結構**。  
  - **命名原因：** 以 **百合（Lilium）** 為代表命名，該屬植物具有科的典型特徵。  

- **-aceae**（植物科名標準後綴）

**完整結構：**

- **Liliaceae = *Lili-*（百合）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **百合屬（Lilium）** 相關的整個植物科，即「百合科」，其成員通常具有**鱗莖、根莖、三瓣花結構**，並廣泛應用於**藥用與園藝**。 

#### 📌 相關藥材連結
?
- 百合
- 黃精



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

### 3.百合科（Liliaceae） 相關知識點


- **Lili-**（來自拉丁文 *lilium*，意為「百合」）  
- 很好猜