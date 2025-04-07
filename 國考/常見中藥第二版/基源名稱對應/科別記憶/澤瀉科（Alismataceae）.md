---
category: 中藥生藥學
tags:
  - 中藥科別
  - 澤瀉科
created: 2025-03-21
updated: 2025-04-07 10:10
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-28
sr-interval: 21
sr-ease: 250
---
#首刷 #review
>一種中藥材
### 1.概念
- **澤瀉科（Alismataceae）** 是一類**主要由水生或沼澤生草本植物組成的單子葉植物科**，多生長於**淡水濕地、水田或湖泊邊緣**。植株常具**肥厚塊莖、劍形葉、乳白色汁液**，並具有良好的**藥用與生態調節功能**。  
- 中藥中的 **澤瀉（Alisma orientale / Alisma plantago-aquatica）** 為該科代表性藥用植物，其**塊莖**入藥，用於**利水滲濕、健脾降脂**等用途。

### 2.詞素拆解
- **Alismat-**  
  來自拉丁文屬名 *Alisma*，源自古希臘語 *αλισμα*（álisma），意指「水生植物」或「水田草」。  
  - *Alisma*：澤瀉屬，該屬植物葉片多呈劍形或橢圓狀，生於水中。  
  - 詞根與拉丁語 *aqua*（水）含義相近，皆指與「水」相關的植物。  

- **-aceae**  
  植物科名標準後綴，用來表示「某某植物科」。

**完整結構：**
- **Alismataceae** = *Alismat-*（水生植物屬名 Alisma）+ *-aceae*（植物科後綴）  
→ 指與 **澤瀉屬（Alisma）** 相關的整個植物科，即「澤瀉科」，其成員大多生於**濕地或水邊，具水生適應性與藥用根莖**，如澤瀉具有**利水消腫、健脾滲濕**的效果，為中醫重要利水滲濕藥。

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



### 3.澤瀉科（Alismataceae） 相關知識點
- 來自拉丁文屬名 *Alisma*，源自古希臘語 *αλισμα*（álisma），意指「水生植物」或「水田草」。  

- 詞根與拉丁語 *aqua*（水）含義相近，皆指與「水」相關的植物。  

### 4.閃卡區


- **Alismat-**  、澤瀉科（Alismataceae）
??
  來自拉丁文屬名 *Alisma*，源自古希臘語 *αλισμα*（álisma），意指「水生植物」或「水田草」。  
  - 詞根與拉丁語 *aqua*（水）含義相近，皆指與「水」相關的植物。 <!--SR:!2025-03-30,3,230!2025-04-02,6,250--> 

- 澤瀉科:::（Alismataceae） <!--SR:!2025-04-01,5,230!2025-04-01,5,230-->