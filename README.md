# ToCC Wiki — Public Site

呢個repo係「眾城紀事」（ToCC Wiki）嘅**發布層**，基於 [Quartz](https://quartz.jzhao.xyz) 靜態網站產生器，透過 GitHub Pages 對外發布。

## 呢個repo唔係咩

**唔存放任何私隱／未篩選嘅wiki內容。** 原始 Obsidian vault（城鎮、NPC、PC、後記、世界設定等全部資料）存放喺另一個 **private** repo：[`othersakura/ToCC-Wiki`](https://github.com/othersakura/ToCC-Wiki)。

## 運作方式

1. `content/` 資料夾喺build時透過 GitHub Actions checkout `ToCC-Wiki` repo 嘅內容（見 `.github/workflows/deploy.yaml`），本機開發時呢個資料夾預設係空嘅
2. 只有 frontmatter 標明 `publish: true` 嘅頁面先會出現喺最終網站（opt-in模式，見 `quartz.config.yaml` 入面嘅 `explicit-publish` plugin），避免漏標而外洩私隱內容
3. Deploy workflow 會喺 push 去 main、每30分鐘排程、或者手動觸發時執行

## 治理

呢個repo嘅協作流程同 `ToCC-Wiki` 一致：branch → commit → PR → human review → human merge。詳見 `ToCC-Wiki` repo 入面嘅《眾城紀事籌備錄》治理原則章節。
