# AI Releases

This repository is the official public download and update channel for AI.

這個儲存庫只提供 AI 的正式安裝檔與自動更新資料，不包含原始碼。

## Download / 下載

Open [Releases](https://github.com/SmallSideOUO/AI-release/releases/latest) and download `AI-Setup-<version>.exe`.

第一次安裝後，後續版本可在應用程式的「設定 → 軟體更新」中檢查、下載並安裝。

## Authenticity / 檔案驗證

Release notes include the SHA-256 checksum of the Windows installer. If the checksum differs, do not run the file.

目前安裝檔未使用付費的 Windows 程式碼簽章憑證，因此 Windows SmartScreen 可能在第一次啟動時顯示提醒。

## AI 1.0.14 模型更新

1.0.14 搭載第一輪 RookieAI YOLOv8s Apex 續訓模型；全新設定的信心門檻為 0.5。
原有設定會保留，既有使用者可以在 GUI 調整信心門檻。
模型在離線測試中改善了中小型與一般人物辨識、減少隊友誤判；最小人物仍需更多資料，且仍存在背景誤判。

模型源自 [Passer1072/RookieAI_yolov8](https://github.com/Passer1072/RookieAI_yolov8)，
續訓使用 [PSImera/apex_enemy_detect](https://huggingface.co/datasets/PSImera/apex_enemy_detect)
（[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)）及
[enemy-allies-tags v2](https://universe.roboflow.com/apex-v2xop/enemy-allies-tags/dataset/2)
（[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)）。
這份模型提供非商業使用，並保留原作者與資料來源署名；安裝包內含完整模型來源說明。
[Ultralytics 模型及框架授權](https://www.ultralytics.com/license)亦適用於其相關元件。

TensorRT 引擎在 RTX 3070 / TensorRT 11.2.1.2 上匯出，其他硬體或執行環境可能需要重新匯出模型。

