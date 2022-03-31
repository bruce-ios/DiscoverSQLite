## SQLITE套件升級

1. 到專案目錄下先把 Pods / Podfile.lock / DiscoverSQLite.xcworkspace 刪除
2. 重新pod install
3. 打開 DiscoverSQLite.xcworkspace
4. Manage Schemes -> shared 打勾所要建制的 framework 
5. 回到專案目錄下打開終端機 `carthage build --no-skip-current --use-xcframeworks`
6. 成功後，回到主專案內呼叫
`carthage update DiscoverSQLite --platform iOS --use-xcframeworks`
