# Welcome to our Git Practice Time!

Let's add your github in our contributors lists!

Website: [CarryU Contributors](https://carryu-contributors.netlify.app/)

html and css is borrowed from [Devcrud](https://www.free-css.com/free-css-templates/page284/dorang)

Written by [xxrjun](https://github.com/xxrjun)

## Contributors


- [Joe-qwe](https://github.com/Joe-qwe)

- [xxrjun](https://github.com/xxrjun)


- [leontzou](https://github.com/leontzou)

- [Elly520](https://github.com/Elly520)

- [carrie57](https://github.com/carrie57)

- [Hank](https://github.com/HankLiu20)



## How to?

### 不同版本？ 建立 Branch!

鼓勵大家了解原理看這 → [Click me](https://git-scm.com/book/zh-tw/v2/%E4%BD%BF%E7%94%A8-Git-%E5%88%86%E6%94%AF-%E7%B0%A1%E8%BF%B0%E5%88%86%E6%94%AF)

1. 複製 `practice-git` 專案到本地並進入該專案

   ```bash
   $ git clone git@github.com:CARRYUU/practice-git.git
   $ cd practice-git
   ```

2. 檢查一下本地 branch 有哪些

   ```bash
   $ git branch
   ```

   理論上只會有 main。想要看遠端 repo 全部的 branch 就要打

   ```bash
   $ git branch -a
   ```

3. 讓本地也追蹤 develop 這個 branch 吧 (開發時大家會 PR 到 develop，等到確定都可以執行才會跟 main 合併)

   ```bash
   $ git checkout develop
   ```

4. 建立一個以自己帳號名稱命名新分支(=在目前提交上新增了一個指標)。

   像我就會是 `xxrjun-branch`

   ```bash
   $ git branch YOURNAME-branch
   ```

5. 切換分支

   ```bash
   $ git checkout YOURNAME-branch
   ```

   可以使用 `git branch -b` 同時達成建立與切換分支

6. 更新自己的分支與 `develop` 一樣 (為避免未來共同開發時你的分支落後太多 commit 導致合併衝突，平常要繼續開發的第一步驟就是先做更新)

   ```bash
   $ git checkout -a
   $ git pull --rebase origin develop
   ```

   如果 rebase 後，你修改的程式碼於提交的這段期間上游的程式碼也被改了，那仍然會發生衝突，這時候打開文字編輯器如(VSCode)處理衝突。接著將更改預存 (Stage) 起來 ，然後執行  `git rebase --continue` 。

   `--rebase` 引數可以用來確保在本機 Commit 過的更新被重新套用在 Pull 的分支的  **最前端**
    ，這也是我們在 PR 工作流程裡通常會做的方式。這樣一來，在開啟 Pull Request 時，你的分支與上游  `develop`分支的差別就只會有你的 Commit。

### 完成第一次 PR 吧!

記得要在自己的 branch 上哦，因為 `main` 、 `develop` 都是受保護分支，連我都不能直接 push!

1. 打開把自己的 github 加入 contributors 的行列吧! (檔案位置 `./README.md`)。範例如下

   ```markdown
   - [xxrjun](https://github.com/xxrjun)
   - [Elly520](https://github.com/Elly520)
   ```

2. `git add` → `git commit`

   ```bash
   $ git add README.md
   $ git commit -m "docs: add <PLACE_YOUR_GITHUB_NAME> to `README.md`"
   ```

3. (Optional) 打開 `index.html` 到約 40 行的地方複製貼上並將名稱跟連結改成自己的 GitHub

   ```html
   <a href="https://github.com/xxrjun">
     <button
       class="btn btn-theme-color modal-toggle"
       style="font-size: 20px;
     "
     >
       xxrjun
     </button>
   </a>
   ```

   一樣 add → commit

   ```bash
   $ git add index.js
   $ git commit -m "feat: add xxrjun into index.html
   ```

4. 這邊 push 需要設定路徑，之後遠端 repo 才會追蹤這個 branch，範例如下

   ```bash
   $ git push --set-upstream upstream xxrjun-branch
   ```

5. 到 GitHub 上發 PR!
