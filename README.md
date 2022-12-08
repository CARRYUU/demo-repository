# Welcome to our Git Practice Time!

Let's add your github in our contributors lists!

### Contributors

- [xxrjun](https://github.com/xxrjun)

### How to?

1. 把 `practice-git` 這個遠端 repo 複製到本地

   ```bash
   git clone https://github.com/CARRYUU/practice-git.git
   ```

   進入該 folder

   ```bash
   cd practice-git
   ```

   打開 VS Code 之類的文字編輯器修改 `README.md` 檔案

2. 切換分支到 `develop`

   ```bash
   git checkout develop
   ```

3. 使用 [Markdown](https://markdown.tw/) 語法把自己的 github 加入 contributors 的行列吧! (檔案位置 `./README.md`)。範例如下

   ```markdown
   - [xxrjun](https://github.com/xxrjun)
   ```

4. `git add` → `git commit` → `git push`

   ```bash
   git add README.md
   git commit -m "docs: add <PLACE_YOUR_GITHUB_NAME> to `README.md`"
   git push origin develop
   ```

VSCode 會提示沒有權限是否要 fork 並且發 PR，這時按 OK

等到至少三個人過目(Code Review)都沒問題就可以 merge pull request 囉!
