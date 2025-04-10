---
category: 中藥生藥學
tags:
  - 中藥科別
  - 銀杏科
created: 2025-03-21
updated: 2025-04-07 19:38
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-07
sr-interval: 30
sr-ease: 290
---
#首刷 #review
>一種中藥材
### 1.概念
- **銀杏科（Ginkgoaceae）** 是**裸子植物門（Gymnospermae）中極為古老的單科單屬單種植物分類群**，僅包含**銀杏（Ginkgo biloba）** 一種，並被譽為**植物界的活化石**。  
- 銀杏科的植物在**白堊紀（約1.45億年前）**就已經出現，曾經廣泛分布於全球，但現今僅存銀杏樹，主要生長於中國，並被廣泛種植於**藥用、園藝與觀賞**用途。  
- 其葉片呈現**扇形，葉脈二叉分裂**，與現存其他裸子植物完全不同，這也是銀杏科的獨特標誌之一。  

### 2.詞素拆解
- **Ginkgo-**  
  來自日語「銀杏（ぎんきょう）」，最早由西方植物學者拼寫錯誤為 *Ginkgo*，但此拼法被沿用至今。  
  - **Ging**（ぎん）= 銀，指銀杏種子（銀杏果）成熟後呈銀白色。  
  - **Kyo**（きょう）= 杏，指其種仁形似杏仁。  
  - **Biloba** = 來自拉丁文 *bi-*（二）+ *loba*（裂片），指其**葉片二裂的特徵**。  

- **-aceae**  
  - 植物科名標準後綴，表示某科植物的分類。  

**完整結構：**
- 銀杏科（Ginkgoaceae）這個名稱由 **Ginkgo**（銀杏屬）+ **-aceae**（科）組成，指與**銀杏屬相關的整個植物科**。

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


### 3.銀杏科（Ginkgoaceae） 相關知識點
- **Ginkgo-**  
  來自日語「銀杏（ぎんきょう）」，最早由西方植物學者拼寫錯誤為 *Ginkgo*，但此拼法被沿用至今。  
  - **Ging**（ぎん）= 銀，指銀杏種子（銀杏果）成熟後呈銀白色。  
  - **Kyo**（きょう）= 杏，指其種仁形似[[杏仁]]。  

### 4.閃卡區


- 銀杏科::Ginkgoaceae <!--SR:!2025-04-18,11,270-->

- **Ging**（ぎん）::銀 <!--SR:!2025-04-22,15,290-->

- **Kyo**（きょう）::杏 <!--SR:!2025-04-22,15,290-->