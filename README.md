**說明**

- 一般開發會有兩個主要分枝：master (main) 跟 develop。main 給客戶使用的上線版本，不能隨意改動。而 develop 類似 alpha 版本，給內部的人員測試。確定沒問題才會合併到 main
- 本地指的是自己的電腦，遠端指的是網路上放代碼地方 (Github, Bitbucket)

**流程**

開發新功能前先切換到開發 (develop) 分枝 : `git checkout develop`

1. 本地: 開發分枝
    - 同步本地與遠端分枝內容: `git pull` (類似同步雲端硬碟)
    - 開新的分枝: `git checkout -b <對接7-11超取服務>` (避免同時開發多個功能，混淆才需要這麼做)
2. 本地: 新的分枝
    - 開發新功能
    - 查看分枝檔案修改狀態: `git status`
    - 將修改加入緩存區: `git add .`
    - 確定修改並給予總結: `git commit -m "完成對接 7-11 超取服務"`
    - 同步本地與遠端分枝內容: `git push` or `git push --set-upstream origin xxx`
3. 遠端: Github.com
    - 開 Pull Request (PR) 將新的分枝合併到開發分枝
    - 同事查看給予回饋
    - 合併到開發分枝
4. 本地: 新的分枝
    - 切換到開發分枝: `git checkout develop`
    - 回到步驟 1
