---
category: 中藥生藥學
tags:
  - 中藥科別
created: 2025-03-20
updated: 2025-04-06 21:27
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-25
sr-interval: 19
sr-ease: 270
---
#首刷 #review 
>五種藥材
### 1.概念
- **薑科（Zingiberaceae）** 主要為**多年生草本植物**，根莖發達，富含**揮發油**、**黃酮類化合物**與**辛辣成分**，在**中藥、食療、香料**領域應用廣泛。  
- **主要藥用特性：**  
  - **溫中散寒**：如 **[[生薑]]（Zingiber officinale）**，可**發汗解表、溫胃止嘔**，常用於治療感冒、胃寒、噁心。  
  - **活血通絡**：如 **薑黃（Curcuma longa）**，含**薑黃素（Curcumin）**，能**抗氧化、抗炎、促進血液循環**，常用於風濕關節疼痛。  
  - **理氣消食**：如 **砂仁（Amomum villosum）**，可**健脾行氣、化濕止瀉**，多用於消化不良、脾胃虛寒。  
  - **芳香開竅**：如 **高良薑（Alpinia galanga）**，具辛香氣味，可**溫中散寒、止痛**，適用於胃寒疼痛、腹脹。  

### 2.詞素拆解
- **Zingiber-**（來自希臘文 *ζιγγίβερις*，經拉丁化為 *zingiberis*，意為「薑」）  
  - **Zingiber**（薑屬）：該屬植物以**辛辣氣味與地下莖結構**為主要特徵，如 **Zingiber officinale（[[生薑]]）**。  
  - **Ginger**（英語「薑」）：直接來自拉丁文 *zingiberis*，經古法語 *gingibre* 演變而來。  
  - **命名原因：** 以 **薑屬（Zingiber）** 為代表命名，該屬植物普遍含有**揮發油與辛辣成分**。  

- **-aceae**（植物科名標準後綴） 

**完整結構：**
- **Zingiberaceae = *Zingiber-*（薑屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **薑屬（Zingiber）** 相關的整個植物科，即「薑科」，其成員通常具有**發達的地下莖、芳香精油、辛辣風味**，並廣泛應用於**藥用、調味與保健養生**。  

#### 📌 相關藥材連結

- [[生薑]]

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

### 3.薑科（Zingiberaceae） 相關知識點

- Zingiber 就是薑，有G的辣(Gin**ger**dione, Sho**ga**ol, Zin**ger**one)；有Bo(ber波)的香(Bisa**bo**lene, zingi**ber**ene（薑烯）, Zingi**ber**ol（薑醇）)


