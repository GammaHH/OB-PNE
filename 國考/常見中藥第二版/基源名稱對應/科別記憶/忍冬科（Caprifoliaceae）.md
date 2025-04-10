---
category: 中藥生藥學
tags:
  - 中藥科別
  - 忍冬科
created: 2025-03-21
updated: 2025-04-07 19:30
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-07
sr-interval: 30
sr-ease: 290
---
#首刷 #review
> 一種中藥材
### 1.概念
- **忍冬科（Caprifoliaceae）** 是一類**主要由雙子葉木本植物組成的植物科**，成員包括**藤本、灌木或小喬木**，分布於**北半球溫帶地區**，尤其以東亞物種多樣性最高。  
- 植物多具**對生葉、腋生花序、花冠筒狀或唇形、果實漿果狀或堅果狀**等特徵。  
- 藥用價值高，代表植物如 **忍冬（Lonicera japonica）**，其花蕾即為中藥「金銀花」，具**清熱解毒、抗菌消炎**等功效。

### 2.詞素拆解
- **Caprifoli-**  
  源自拉丁文 *Caprifolium*，由 *caper*（山羊）+ *folium*（葉）組成，意為「山羊之葉」。  
  - **Capri-** = 山羊（來自 *caper*）  
  - **-foli-** = 葉（來自 *folium*）  
  - 命名可能源於早期觀察到**山羊喜食忍冬類植物的葉片**，因此以此命名  
  - **Caprifolium**：即「忍冬」的拉丁俗名，現多歸入屬名 *Lonicera*  

- **-aceae**  
  植物科名標準後綴，表示「某某科」

**完整結構：**
- **Caprifoliaceae** = *Caprifoli-*（意為「山羊喜食之葉」的忍冬屬名詞根）+ *-aceae*（植物科後綴）  
→ 指與 **忍冬屬（Lonicera／Caprifolium）** 相關的整個植物科，即「忍冬科」。其成員多具**清香花朵與漿果狀果實**，部分種類廣泛應用於**中藥（如金銀花）、庭園植物與香藥草領域**。

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


### 3.忍冬科（Caprifoliaceae） 相關知識點

- **Caprifoli-**  
  源自拉丁文 *Caprifolium*，由 *caper*（山羊）+ *folium*（葉）組成，意為「山羊之葉」。  
  - **Capri-** = 山羊（來自 *caper*）  
  - **-foli-** = 葉（來自 *folium*）  


### 4.閃卡區


- 忍冬科:::（Caprifoliaceae） <!--SR:!2025-03-31,4,290!2025-03-30,3,270-->

- - **Caprifoli-**  
??
  源自拉丁文 *Caprifolium*，由 *caper*（山羊）+ *folium*（葉）組成，意為「山羊之葉」。  
  - **Capri-** = 山羊（來自 *caper*）  
  - **-foli-** = 葉（來自 *folium*）  
  - 命名可能源於早期觀察到**山羊喜食XX植物的葉片**，因此以此命名  
  - **Caprifolium**：即「XX」的拉丁俗名，現多歸入屬名 *Lonicera* <!--SR:!2025-03-31,4,290!2025-03-30,3,270-->  

- **Capri-** = ==山羊==（來自 *caper*）  

- **-foli-** = ==葉==（來自 *folium*）  