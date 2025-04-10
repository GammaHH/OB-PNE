---
category: 中藥生藥學
tags:
  - 中藥科別
  - 敗醬科
created: 2025-03-21
updated: 2025-04-09 13:55
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-09
sr-interval: 30
sr-ease: 290
---
#首刷 #review
> 一種中藥材
> 
>  - 生藥有講
### 1.概念
- **敗醬科（Valerianaceae）** 是一類**主要由草本植物組成的雙子葉植物科**，現代分類中常被併入**[[忍冬科（Caprifoliaceae）]]**，但在傳統分類仍常單獨列出。主要分布於**北半球溫帶至高山地區**。  
- 植物具有**對生葉、花冠筒狀、有特殊氣味的根部**等特徵，多具**鎮靜安神、活血消腫、抗痙攣等藥用功效**。  
- 代表藥用植物包括：  
  - **敗醬草（Patrinia scabiosaefolia）**：清熱解毒、消癰排膿  
  - **纈草（Valeriana officinalis）**：鎮靜助眠、緩解焦慮（西方草藥常用）  

### 2.詞素拆解
- **Valerian-**  
  來自拉丁文 *valere*，意為「==健康、有力、強壯==」  
  - *Valeriana*：**纈草**屬，是該科的模式屬，具有強烈根香與鎮靜作用  
  - 詞根 *valer-* 可見於英語 *valor（勇氣）*、*valuable（有價值的）*，語意皆與「強健、良好狀態」有關 <!--SR:!2025-04-13,4,282-->   

???

- **-aceae**  
  植物科名標準後綴，表示某某科 

**完整結構：**
- **Valerianaceae** = *Valerian-*（纈草屬，意為「強健、健康的」）+ *-aceae*（植物科後綴）  
→ 指與 **Valeriana 屬** 相關的整個植物科，即「敗醬科」，其成員多具**特殊根香、生理調節作用與抗炎解毒特性**，常用於**中藥（敗醬草）與西方草藥（纈草）**領域，具有鎮靜安神與清熱排膿等多重療效。 

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


### 3.敗醬科（Valerianaceae） 相關知識點

- **Valerianaceae** = *Valerian-*（纈草屬，意為「強健、健康的」）+ *-aceae*（植物科後綴）  


### 4.閃卡區

???

- **Valerian-**  、敗醬科（Valerianaceae）
??
  來自拉丁文 *valere*，意為「健康、有力、強壯」  
  - *Valeriana*：纈草屬，是該科的模式屬，具有強烈根香與鎮靜作用  
  - 詞根 *valer-* 可見於英語 *valor（勇氣）*、*valuable（有價值的）*，語意皆與「強健、良好狀態」有關 <!--SR:!2025-04-13,4,282!2025-04-12,3,262-->   

???


- 敗醬科（Valerianaceae），代表藥用植物：
?
  - **敗醬草（Patrinia scabiosaefolia）**：清熱解毒、消癰排膿  
  - **纈草（Valeriana officinalis）**：鎮靜助眠、緩解焦慮（西方草藥常用） <!--SR:!2025-04-25,16,310-->

???