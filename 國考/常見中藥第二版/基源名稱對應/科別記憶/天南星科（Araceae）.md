---
category: 中藥生藥學
tags:
  - 中藥科別
  - 天南星科
created: 2025-03-21
updated: 2025-04-09 14:34
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-05-09
sr-interval: 30
sr-ease: 290
---
#首刷 #review
> 一種中藥材
### 1.概念
- **天南星科（Araceae）** 是一類**主要由草本植物組成的單子葉開花植物科**，其成員多數具有**肉穗花序（Spadix）與佛焰苞（Spathe）**，部分含有**草酸鈣結晶、黏液與生物鹼**，廣泛應用於**中藥、觀賞植物、食品與工業用途**。代表植物包括 **[[半夏]]（Pinellia ternata）、天南星（Arisaema heterophyllum）、滴水蓮（Spathiphyllum spp.）、魔芋（Amorphophallus konjac）、海芋（Zantedeschia aethiopica）**。  
- **主要藥用特性（部分品種具刺激性，需經炮製處理）：**  
  - **燥濕化痰**：如 **[[半夏]]（Pinellia ternata）**，富含**生物鹼與揮發油**，可**燥濕化痰、降逆止嘔**，適用於痰多咳嗽、嘔吐反胃（需炮製後使用）。  

### 2.詞素拆解
- **Ar-** 「Arum」這個字來自古希臘語的 ἄρον（aron），意思是**「**辣根植物**」或「根莖辛辣的植物」
- 「星」在這裡是中藥名的古典命名，與天文無關喔！
- 多用於祛風化痰、解毒散結的中藥材

- **-aceae**（植物科名標準後綴）

**完整結構：**
- **Araceae = *Ar-*（天南星屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **天南星屬（Arum）** 相關的整個植物科，即「天南星科」，其成員通常具有**肉穗花序與佛焰苞、燥濕化痰、祛風止痙、潤腸通便與消腫解毒的藥用價值**，並廣泛應用於**中藥、食品、觀賞植物與工業用途**。

#### 📌 相關藥材連結

- [[半夏]] - 不可生用有毒，可以用生薑解毒

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


### 3.天南星科（Araceae） 相關知識點

- **Ar-** 「Arum」這個字來自古希臘語的 ἄρον（aron），意思是**「**辣根植物**」或「根莖辛辣的植物」
- 「星」在這裡是中藥名的古典命名，與天文無關喔！



