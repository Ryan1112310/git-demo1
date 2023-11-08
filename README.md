### git指令筆記  

> 作者:  
- Ryan.F


> 建立時間
- 2023/11/08

- 版本號
	- git version

- 建立基本資訊
	- git config --global user.name ryan
	- git config --global user.email a0932952126@gmail.com

- 顯示設定資訊
	- git config —-list

- 設定控管程式碼倉庫
	- git init

- 本地資訊
	- cat .git/config

- 建立區域基本資料
	- git config user.name ryan1
	- git config user.email a09329521261@gmail.com

- 將檔案加入暫存區
	- git add file-name
	- U -> A

	- git add .
		- 一次將所以檔案加入暫存器

- 觀察GIT狀態
	- git status
	- U==> untrack
	- A==> add

- 檢視控管內容
	- git cat-file -t shal
		- t(型態)
		- p(內容)
		- s(大小)

- 檢視暫存器內容
	- git ls-files -s
		- s shal編碼
- 暫存區修改
	- 修改後恢復(command+z)
	- git checkout file-name

	- 修改後確認
		- git add file-name

- 版本提交
	- git commit -m “註解”

- 檢視commit狀態
	- git log
	- git log —oneline

- 刪除後可以使用
	- git checkout 進行恢復
	- git add 進行確認
	- git commit 進行提交

- 最後一次的commit提交
	- git commit —amend
		- vim
			- i ==>插入(本文修改)
		- esc
			- :
			- w ==>儲存
			- q ==>離開

			- Mac用法
				- c ==>進入編輯狀態  
				- esc ==>退出編輯狀態  
				- ZZ ==>保存並退出vim  

GIT-
=================================

- 暫存區手動刪除恢復
	- git checkout file-name

- 暫存區==>工作區
	- git reset head file-name (A->U)

- 倉庫區手動刪除的恢復
	- git checkout file-name

-倉庫區/暫存區==>工作區
	- git rm —cached file-name

- 倉庫區 git -rm file-name 
	- 恢復跟確認都要下
		-g it reset head file-name
			- git checkout
			- git add

GIT-BRANCH
=================================
- 觀察目前分支狀態
	-git branch

- 產生分支
	- git branch test

- 切換分支(master=>test)
	- git checkout test
	- HEAD=>test

- 刪除分支
	- git checkout master
	- git branch -D branch-name

- 產生跟切換分支
	- git checkout -b test

Commit 切換
=================================
- git checkout commit-object

- 新增/修改
	1.新增branch (git checkout -b dev)
	2.修改內容
	3.git add .
	4.git commit -m “提交更新”
	5.git checkout master
	6.git merge dev
	6-1.衝突處理(如果有)
	7.git commit -m “merge提交”
	8.git branch -D dev

- git reflog
	- 取得目前所有commit-object

- Ios系統步驟
	1.新增branch (git checkout -b dev)
	2.修改內容
	3.git add .
	4.git commit -m “提交更新”
	5.git checkout master
	6.git merge dev(會直接把新舊檔合併)
	7.git branch -D dev

git reset
=================================
- git reset —hard commit-object
	- 名義上後面新增/修改的檔案都會被刪除
- git rest —mixed commit-object
	- A->U

- git rest —soft commit-object
	- 恢復在暫存區
- git reflog
	- git rest (checkout) commit-object

git remote
=================================
- git remote add origin url
	- 加入遠端url(倉庫)

- git remote -v
	- 檢視所有淵端的url

- git remove origin
	- 移除遠端url

git push
=================================
- git push
	- 將本地端資料上傳到遠端
	
	- 第一次
		- git push -u origin master

- git commit —amend
	- 修改最近一次的commits

- git push -f (force)
	- 不管衝突，直接覆蓋遠端  

	### 繪製表格 Tables

| 專案        | 價格   |  數量  |
| --------   | -----:  | :----:  |
| 計算機      | $1600   |   5     |
| 手機        |   $12   |   12   |
| 管線        |    $1    |  234  |

