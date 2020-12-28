# Taigi-TPS 台語方音輸入法

> 配方： **℞ yuren-tw/rime-taigi-tps**

1. 本方案基於 RIME 輸入法引擎
2. `taigi_tps.schema.yaml` 為方案配置檔
3. `taigi_yu.dict.yaml` 為特製台語字典檔，詳見下方說明。

## 鍵盤配置

本方案以大千式注音符號為基礎，適合熟悉注音輸入法的使用者。
（與大千式配置不同的符號在下圖以紅色粗體字表示）

![](./keyboard_layout.png)

| 配置差異   | <kbd>Z | <kbd>T | <kbd>G | <kbd>B | <kbd>I | <kbd>, | <kbd>O | <kbd>. | <kbd>M | <kbd>/ | <kbd>- | <kbd>5 | <kbd>7 |
|:---------:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| **大千式** | ㄈ |  ㄔ  | ㄕ | ㄖ | ㄛ | ㄝ | ㄟ | ㄡ | ㄩ | ㄥ |  ㄦ  |  ㄓ  | 輕聲 |
| **本方案** | ㆠ | ㆢㆡ | ㄫ | ㆣ | ㆦ | ㆤ | ㆰ | ㆲ | ㆬ | ㆭ | 鼻音 | ７聲 | 入聲 |


## 輸入方式與功能

本方案採用台語方音符號來輸入，基本輸入順序語注音輸入法的「聲母 + 韻母 + 聲調」類似。

> [方音符號](https://zh.wikipedia.org/wiki/臺灣方音符號)是以[注音符號](https://zh.wikipedia.org/wiki/注音符號)為基礎來擴充的一種標音符號，主要用於標註台灣話。

- 方音符號區分 `ㄐ`、`ㄑ`、`ㄒ`、`ㆢ` 與 `ㄗ`、`ㄘ`、`ㄙ`、`ㆡ`，熟悉台羅、白話字的使用者請多注意
  - 本方案中，`ㆢ` 與 `ㆡ` 合併在同一個鍵位
- 韻母 `ㆱ` 較為罕見，能以 `ㆦㆬ` 或 `ㆰ` 來輸入，後者也較適合某些腔調習慣
- 鼻化韻母的輸入方式為「韻母 + 鼻音鍵 `ｎ`」
  - 例如以 `ㄚｎ` 來輸入 `ㆩ`
  - 也能單以鼻音鍵 `ｎ` 代表所有鼻化韻母，不適合輸入單字
- 入聲調輸入方式有兩種：（本方案輸入時不區分第四調與第八調）
  - 結合韻母 + 入聲鍵 `．`：與前方韻母結合，較接近傳統韻書習慣，且減少按鍵數
    - 純母音：例如以 `ㄚ．` 來輸入 `ㄚㆷ`
    - ㆬ韻尾：例如以 `ㆰ．` 來輸入 `ㄚㆴ`
    - ㄯ韻尾：例如以 `ㄢ．` 來輸入 `ㄚㆵ`
    - ㆭ韻尾：例如以 `ㄤ．` 來輸入 `ㄚㆻ`
    - `ㆬ`、`ㆭ`：例如以 `ㆬ．` 來輸入 `ㆬㆷ`
    - 也能單以入聲鍵 `．` 代表所有「韻母 + 入聲」，不適合輸入單字
  - 對應聲母 + 入聲鍵 `．`：例如以 `ㄅ．` 來輸入 `ㆴ`
- 可直接輸入變調後的聲調，方便思考
  - 例如以 `ㄏㄨㆤˉㄑㄧㄚˉ` 來輸入 `ㄏㄨㆤˋㄑㄧㄚˉ`（火車）
  - 例如以 `ㆠㄚˋㄨㄢˊ` 來輸入 `ㆠㄚㆷㄨㄢˊ`（肉丸）
- 支援下列常見的音變
  - 以 `ㄌ` 來輸入 `ㆢ`、`ㆡ`
  - 以 `ㆤㄣ`（en）來輸入 `ㄧㄢ`（ien、ian）
  - 以 `ㆤㆵ`（et）、`ㄧㆤㆵ`（iet）來輸入 `ㄧㄚㆵ`（iat）
- 下列拼音能用注音符號中發音相似的鍵位組合來輸入
  - 以 `ㄨㆭ`（注音 `ㄨㄥ` /ʊŋ/）來輸入 `ㆲ` /ɔŋ/
  - 以 `ㆬㆭ`（注音 `ㄩㄥ` /iʊŋ/）來輸入 `ㄧㆲ` /iɔŋ/
  - 台語存在 `ㄅㆭ`（例如：飯）與 `ㄅㆲ`（例如：磅）的差別，此處不提供相似音輸入（注音 `ㄅㄥ`）以避免歧義


## 台語字典

本方案字典檔採用的字詞來源為[教育部臺灣閩南語常用詞辭典](https://twblg.dict.edu.tw/)（[資料檔 @ GitHub](https://github.com/g0v/moedict-data-twblg)）。

為了方便輸入法方案設計，字典採用特製的拼音，大小寫有特殊意義。如有增修字典的需求請多注意。
