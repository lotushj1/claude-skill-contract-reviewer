# Contract Reviewer Skill 合約審核助手

A Claude Code skill for reviewing contracts in Traditional Chinese. Quickly extracts key terms, highlights unfair clauses, and generates structured summaries.

一個用於審閱合約的 Claude Code 技能。快速提取關鍵條款、標記不公平內容、產出結構化摘要報告。

---

## ✨ Features 功能特色

- 📋 **自動提取合約重點** — 雙方資訊、費用、日期、義務一目瞭然
- ⚠️ **風險條款標記** — 自動識別高/中風險條款並提供修改建議
- 🟢 **有利條款辨識** — 標出對你有保障的條款
- 📝 **結構化摘要報告** — 便於存檔與後續查閱
- 🇹🇼 **繁體中文優化** — 針對台灣常見合約用語設計

---

## 📦 Installation 安裝

將 skill 資料夾複製到你的 Claude Code skills 目錄：

```bash
cp -r contract-reviewer ~/.claude/skills/user/
```

或手動下載後放入 skills 目錄。

---

## 🚀 Usage 使用方式

### 觸發方式

- 上傳合約 PDF 檔案
- 直接貼上合約文字
- 使用觸發詞：
  - 「審合約」「看合約」「合約重點」
  - `contract review`

### 快速指令

| 指令 | 功能 |
|------|------|
| `/review` | 完整審閱，輸出摘要報告 |
| `/summary` | 只輸出重點摘要 |
| `/risk` | 只檢查風險條款 |
| `/compare` | 比較兩份合約差異 |

---

## 📊 Output Example 輸出範例

審閱後會產出結構化報告，包含：

```
📋 合約摘要報告
├── 🏢 雙方資訊（名稱、統編、聯絡人）
├── 💰 費用條款（金額、付款時間、方式）
├── 📅 重要日程（生效日、交付日、終止日）
├── ⚖️ 雙方義務
├── ⚠️ 特別注意事項
│   ├── 🔴 高風險條款
│   ├── 🟡 中風險條款
│   └── 🟢 對你有利的條款
└── ✅ 審核結論與建議行動
```

---

## 🔍 Risk Patterns 風險檢查項目

### 🔴 高風險條款
- 單方面修改權
- 無上限賠償責任
- 過高違約金（超過 30%）
- 廣泛的智財移轉
- 競業禁止條款
- 無條件終止權僅給一方

### 🟡 中風險條款
- 模糊的工作範圍
- 無限修改義務
- 自動續約條款
- 過長的保密期限
- 片面的驗收標準

---

## 📁 File Structure 檔案結構

```
contract-reviewer/
├── SKILL.md              # 主要技能定義與輸出格式
└── references/
    └── risk-patterns.md  # 風險模式參考資料庫
```

---

## ⚠️ Disclaimer 免責聲明

此工具僅供參考，不構成法律建議。重要合約請諮詢專業律師。

This tool is for reference only and does not constitute legal advice. Please consult a professional lawyer for important contracts.

---

## 📄 License

MIT

---

## 🤝 Contributing

歡迎提交 Issue 或 PR 來改善這個 Skill！

- 新增更多風險模式
- 支援更多合約類型
- 改善輸出格式
