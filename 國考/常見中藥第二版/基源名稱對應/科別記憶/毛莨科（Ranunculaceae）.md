---
category: 中藥生藥學
tags:
  - 中藥科別
created: 2025-03-11
updated: 2025-04-06 22:26
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-06
sr-interval: 30
sr-ease: 290
---
#首刷 #review 
### 1.概念
- **毛茛科（Ranunculaceae）** 主要為草本植物，包含許多具有藥用價值的種類，如 **白芍（Paeonia lactiflora）** 和 **附子（Aconitum carmichaelii）**。  
- **主要特性：**  
  - 根部常含 **皂苷（Saponins）** 與 **生物鹼（Alkaloids）**，部分具藥用價值，如 **白芍**（補血、活血）與 **附子**（大毒，經炮製後入藥）。  
  - 花朵鮮豔，種類繁多，如 **銀蓮花（Anemone）**、**鐵線蓮（Clematis）** 等觀賞植物。  
  - 部分植物含劇毒，影響神經系統，如 **烏頭（Aconitum spp.）**。  

### 2.詞素拆解
- **Ranuncula-**（來自拉丁文 *ranunculus*，意為「小青蛙」）  
  - **Ranunculus**（毛茛屬）：因部分植物生長於潮濕環境，像青蛙棲息的地方，故得名。  
  - **Rana**（青蛙）：同源詞，如 **Rana temporaria**（歐洲褐蛙）。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Ranunculaceae = *Ranuncula*（毛茛屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **毛茛屬（Ranunculus）** 相關的整個植物科，即「毛茛科」，包含眾多藥用與觀賞植物，部分具毒性。  


#### 📌 相關藥材連結
- 白芍



```dataviewjs
// ---------- 標籤推薦區塊（以列表呈現） ----------
const excludeTags = ["中藥科別","中藥生藥學"];
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
        pages.map(p => {
          const tagsToShow = p.tags?.filter(t => !excludeTags.includes(t) && t !== tag) ?? [];
          return `${p.file.link}　${tagsToShow.join("、")}`;
        })
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥材具有相同標籤的其他筆記。");
}
```





### 3.毛莨科（Ranunculaceae） 相關知識點




