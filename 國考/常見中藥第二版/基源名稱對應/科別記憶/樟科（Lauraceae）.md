---
category: 中藥生藥學
tags:
  - 中藥科別
created: 2025-03-20
updated: 2025-04-06 22:30
source:
  - 常用中藥第二版
Abstract: 中藥詞卡
sr-due: 2025-04-24
sr-interval: 18
sr-ease: 270
---
#首刷 #review 
### 1.概念
- **樟科（Lauraceae）** 是一類**主要由喬木與灌木組成的雙子葉開花植物科**，以**芳香精油、揮發性物質與藥用價值**著稱，廣泛應用於**中藥、香料、木材與精油提取**。代表植物包括 **樟樹（Cinnamomum camphora）、肉桂（Cinnamomum verum）、牛樟（Cinnamomum kanehirae）、月桂（Laurus nobilis）、鱗皮楠（Lindera aggregata）**。  
- **主要藥用特性：**  
  - **行氣活血**：如 **肉桂（Cinnamomum verum）**，富含**桂皮醛（Cinnamaldehyde）與桂皮酸**，可**溫中補陽、行氣活血**，適用於脾胃虛寒、血行不暢。  
  - **驅風散寒**：如 **樟樹（Cinnamomum camphora）**，其樟腦成分可**通竅祛風、消腫止痛**，適用於風濕痹痛、跌打損傷。  
  - **健胃消食**：如 **月桂（Laurus nobilis）**，富含**芳香精油與黃酮**，可**促進消化、健脾開胃**，適用於消化不良、腸胃脹氣。  
  - **解毒抗菌**：如 **鱗皮楠（Lindera aggregata）**，含**生物鹼與黃酮類化合物**，可**清熱解毒、消炎抗菌**，適用於感冒發熱、細菌感染。  

### 2.詞素拆解
- **Laur-**（來自拉丁文 *laurus*，意為「月桂樹」）  
  - **Laurus**（月桂屬）：代表樟科的模式屬，如 **Laurus nobilis（月桂）**，以其芳香葉片與藥用價值聞名。  
  - **Laurel**（英語「月桂」）：直接來自拉丁文 *laurus*，象徵榮耀與勝利，如「桂冠詩人（Poet laureate）」。  
  - **命名原因：** 以 **月桂屬（Laurus）** 為代表命名，該屬植物具有**芳香精油與藥用特性**。  

- **-aceae**（植物科名標準後綴）  

**完整結構：**
- **Lauraceae = *Laur-*（月桂屬）+ *-aceae*（植物科後綴）**  
- **意義**：指與 **月桂屬（Laurus）** 相關的整個植物科，即「樟科」，其成員通常具有**芳香精油、抗菌消炎、藥用與經濟價值**，並廣泛應用於**中藥、食品、香精與木材領域**。  

#### 📌 相關藥材連結




```dataviewjs
const excludeTags = ["中藥科別","中藥生藥學"];
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
          const tagsToShow = p.tags?.filter(t => !excludeTags.includes(t) && t !== tag) ?? [];
          return `${p.file.link}　${tagsToShow.join("、")}`;
        })
      );
    }
  }
} else {
  dv.header(5, "相關藥物（0）");
  dv.paragraph("沒有找到與本藥材具有相同標籤的其他筆記。");
}
```




### 3.樟科（Lauraceae） 相關知識點


