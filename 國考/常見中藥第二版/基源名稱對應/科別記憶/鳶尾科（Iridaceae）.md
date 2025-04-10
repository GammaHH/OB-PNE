---
category: 中藥生藥學
tags:
  - 中藥科別
  - 鳶尾科
created: 2025-03-21
updated: 2025-04-10 09:33
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-10
sr-interval: 30
sr-ease: 310
---
#首刷 #review
### 1.概念
- **鳶尾科（Iridaceae）** 是一類**主要由多年生草本植物組成的單子葉植物科**，廣泛分布於**全球溫帶與熱帶地區，尤其以非洲南部物種最為豐富**。  
- 本科植物多具有**球莖、根莖或塊莖**等儲藏器官，葉多為**劍形、二列排列**，花大而美麗，常作為**觀賞花卉、香料或藥用植物**。  
- 代表植物包括：  
  - **鳶尾（Iris spp.）**：部分種根可入藥或製香（鳶尾根）  
  - **番紅花（Crocus sativus）**：花柱可製成名貴香料「藏紅花」  
  - **唐菖蒲（Gladiolus spp.）**：主要作觀賞花卉  

### 2.詞素拆解
- **Irid-**  
  來自希臘文 *Ἶρις*（Iris），原意為「彩虹」，亦是希臘神話中**彩虹女神之名**  
  - 命名意涵：形容鳶尾花**花色豐富、艷麗如虹**  
  - *Iris*：模式屬名稱，即「鳶尾屬」  

- **-aceae**  
  植物科名標準後綴，表示某某植物科  

**完整結構：**
- **Iridaceae** = *Irid-*（來自希臘的「彩虹」，指鳶尾屬 Iris）+ *-aceae*（植物科後綴）  
→ 指與 **鳶尾屬（Iris）** 相關的整個植物科，即「鳶尾科」，其成員多具**地下儲藏器官與艷麗花朵**，廣泛應用於**觀賞園藝、香料製作（如藏紅花）與部分藥用領域**，是兼具美學與實用性的植物家族。 <!--SR:!2025-03-31,4,290-->
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


### 3.鳶尾科（Iridaceae） 相關知識點

- **Iridaceae** = *Irid-*（來自希臘的「彩虹」，指鳶尾屬 Iris）+ *-aceae*（植物科後綴）  
→ 指與 **鳶尾屬（Iris）** 相關的整個植物科，即「鳶尾科」，其成員多具**地下儲藏器官與艷麗花朵**，廣泛應用於**觀賞園藝、香料製作（如藏紅花）與部分藥用領域**，是兼具美學與實用性的植物家族。


### 4.閃卡區

- **Iridaceae** = *Irid-*（==來自希臘的「彩虹」，指鳶尾屬 Iris==）+ *-aceae*（植物科後綴）  
→ 指與 **鳶尾屬（Iris）** 相關的整個植物科，即「鳶尾科」，其成員多具**地下儲藏器官與艷麗花朵**，廣泛應用於**觀賞園藝、香料製作（如藏紅花）與部分藥用領域**，是兼具美學與實用性的植物家族。 <!--SR:!2025-04-14,4,292-->
