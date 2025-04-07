---
category: 中藥生藥學
tags:
  - 中藥科別
  - 鹿科
created: 2025-03-20
updated: 2025-04-06 22:05
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-14
sr-interval: 8
sr-ease: 210
---
#首刷 #review 
>一種中藥材
### 1.概念
- **鹿科（Cervidae）** 是一類**主要由偶蹄目（Artiodactyla）中型至大型草食性哺乳動物組成的動物科**，其特徵為**雄性（部分雌性）具有角（鹿角）、四肢修長、適應森林與草原環境**，廣泛應用於**中藥、保健品、皮革與野生動物保護**。代表物種包括 **梅花鹿（Cervus nippon）、馬鹿（Cervus elaphus）、麋鹿（Elaphurus davidianus）、馴鹿（Rangifer tarandus）、白尾鹿（Odocoileus virginianus）**。  
- **主要藥用特性：**  
  - **補腎壯陽、強筋骨**：如 **鹿茸（Cervus spp.）**，富含**膠原蛋白、雄激素、胺基酸**，可**補腎助陽、強筋健骨**，適用於腎虛陽痿、腰膝酸軟。  
  - **補血益精**：如 **鹿血（Cervus spp.）**，含有**鐵、蛋白質與多肽類**，可**補血養氣、提高耐力**，適用於氣血虛弱、貧血。  
  - **滋養皮膚**：如 **鹿胎盤（Cervus spp.）**，富含**生長因子與激素**，可**促進組織修復、延緩衰老**，適用於內分泌失調、皮膚衰老。  
  - **抗炎消腫**：如 **鹿骨（Cervus spp.）**，富含**磷酸鈣與膠原蛋白**，可**強壯筋骨、祛風除濕**，適用於風濕關節炎、骨質疏鬆。  



### 2. 詞素拆解

- **Cervid-**（來自拉丁文 *cervus*，意為「鹿」）  
　- 例如：**Cervus elaphus**（馬鹿）、**Cervus nippon**（梅花鹿）等屬名都來自此詞根。  
　- 在英語中，*cervid* 也可作為「鹿類動物」的泛稱。

- **-idae**（動物科名標準後綴）  
　- 常見於動物分類，如 **Felidae（貓科）**、**Canidae（犬科）**、**Bovidae（牛科）** 等，指該生物所屬的「科」。


**完整結構：**  
- **Cervidae = *Cervid-*（鹿屬）+ *-idae*（動物科後綴）**  
- **意義**：指與 **鹿屬（Cervus）** 相關的整個動物科，即「鹿科」，其成員通常具有**鹿角、草食性、適應森林與草原環境**，並廣泛應用於**中藥、保健品、皮革與野生動物保護**。

#### 📌 相關藥材連結

- [[鹿茸]]

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
        pages.map(p => {
          const tagsToShow = p.tags.filter(t => !excludeTags.includes(t));
          return `${p.file.link}　${tagsToShow.join("、")}`;
        })
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥物具有相同標籤的其他筆記。");
}
````

### 3.鹿科（Cervidae） 相關知識點

- 鹿科::Cervidae
