---
category: 中藥生藥學
tags:
  - 中藥科別
  - 葫蘆科
created: 2025-03-21
updated: 2025-04-07 10:42
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-13
sr-interval: 6
sr-ease: 230
---
#首刷 #review
>一種中藥材
### 1.概念
- **葫蘆科（Cucurbitaceae）** 是一類**主要由一年生攀緣性草本植物組成的雙子葉植物科**，廣泛分布於**熱帶與亞熱帶地區**，是**重要的蔬果與藥用植物來源**之一。  
- 本科植物通常具有**蔓莖、卷鬚、合瓣花與漿果型果實**，果實多為可食用或藥用的**瓜類、瓠瓜類或苦瓜類**，葉片多為掌狀分裂。  
- 代表植物包括：  
  - **苦瓜（Momordica charantia）**：清熱解毒、降血糖  
  - **冬瓜（Benincasa hispida）**：利水消腫、清熱化痰  
  - **栝蔞（Trichosanthes kirilowii）**：化痰散結、潤燥通便  
  - **黃瓜（Cucumis sativus）、南瓜（Cucurbita spp.）、西瓜（Citrullus lanatus）**：食療與保健用途廣泛

### 2.詞素拆解
- **Cucurbit-**  
  來自拉丁文 *cucurbita*，意為「葫蘆、南瓜類植物」  
  - 此詞指稱所有**葫蘆狀、瓜狀果實的蔓生植物**  
  - 相關英語詞如：  
    - *Cucumber*（黃瓜）、*gourd*（葫蘆）、*zucchini*（櫛瓜）皆屬此類植物  
  - 屬名如 *Cucurbita*（南瓜屬）即直接延伸自此詞根  

- **-aceae**  
  植物科名標準後綴，表示某某科  

**完整結構：**
- **Cucurbitaceae** = *Cucurbit-*（==指瓜類植物的屬名與形態特徵==）+ *-aceae*（植物科後綴）  
→ 指與 **Cucurbita 屬（南瓜屬）** 與其他瓜類植物相關的整個植物科，即「葫蘆科」。該科成員以**攀緣莖、掌狀葉、可食果實與藥用根莖果實**為主要特徵，是**藥食兩用、農業經濟與藥理研究中極具價值的植物類群**。 <!--SR:!2025-04-10,3,250-->  

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


### 3.葫蘆科（Cucurbitaceae） 相關知識點

- **Cucurbit-**  
  來自拉丁文 *cucurbita*，意為「==葫蘆、南瓜類植物==」 <!--SR:!2025-04-10,3,269-->  
  
  - 此詞指稱所有**葫蘆狀、瓜狀果實的蔓生植物**  


### 4.閃卡區

- *cucurbita* 像是(英文)::*Cucumber*（黃瓜） <!--SR:!2025-04-18,11,270-->
