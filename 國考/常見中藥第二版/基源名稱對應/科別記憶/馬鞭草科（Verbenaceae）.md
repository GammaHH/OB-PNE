---
category: 中藥生藥學
tags:
  - 中藥科別
  - 馬鞭草科
created: 2025-03-21
updated: 2025-04-07 11:40
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-05
sr-interval: 28
sr-ease: 250
---
#首刷 #review
>一種中藥材
### 1.概念
- **馬鞭草科（Verbenaceae）** 是一類**主要由草本、灌木或小喬木組成的雙子葉開花植物科**，其成員多數含有**芳香精油、黃酮與生物鹼**，具有**藥用、芳香與園藝價值**，廣泛應用於**中藥、保健品、香料與園藝**。代表植物包括 **馬鞭草（Verbena officinalis）、大青（Clerodendrum cyrtophyllum）、海州常山（Clerodendrum inerme）、臭牡丹（Clerodendrum bungei）**。  
- **主要藥用特性：**  
  - **清熱解毒**：如 **馬鞭草（Verbena officinalis）**，富含**黃酮類與三萜類**，可**清熱利濕、活血散瘀**，適用於感冒發熱、*瘡癰腫毒*。  
  - **祛風除濕**：如 **大青（Clerodendrum cyrtophyllum）**，含有**生物鹼與酚類化合物**，可**祛風除濕、舒筋活絡**，適用於風濕痹痛、關節僵硬。  
  - **活血止痛**：如 **海州常山（Clerodendrum inerme）**，富含**揮發油與黃酮類**，可**活血化瘀、消腫止痛**，適用於跌打損傷、瘀血腫痛。  
  - **鎮靜安神**：如 **臭牡丹（Clerodendrum bungei）**，含有**類黃酮與苯丙素類**，可**鎮靜安神、抗焦慮**，適用於失眠、神經緊張。  

### 2.詞素拆解
- **Verben-**（來自拉丁文 *verbena*，意為「馬鞭草」）  
  - **Verbena**（馬鞭草屬）：代表馬鞭草科的模式屬，如 **Verbena officinalis（馬鞭草）**，以其藥用價值與歷史宗教用途聞名。  
  - `念起來也很像馬鞭`
  - **Verveine**（法語「馬鞭草」）：用於香水與芳香療法，來自同一詞源。  
  - **命名原因：** 以 **馬鞭草屬（Verbena）** 為代表命名，該屬植物普遍含有**芳香精油、藥用活性成分**

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Verbenaceae = *Verben-*（==馬鞭草屬==）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **馬鞭草屬（Verbena）** 相關的整個植物科，即「馬鞭草科」，其成員通常具有**清熱解毒、祛風除濕、活血止痛與鎮靜安神的藥用價值**，並廣泛應用於**中藥、保健品、香料與園藝**。 <!--SR:!2025-04-08,1,230-->  

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



### 3.馬鞭草科（Verbenaceae） 相關知識點
- **Verben-**（來自拉丁文 *verbena*，意為「馬鞭草」）  
  - **Verbena**（馬鞭草屬）：代表馬鞭草科的模式屬，如 **Verbena officinalis（馬鞭草）**，以其藥用價值與歷史宗教用途聞名。  
  `念起來也很像馬鞭`




