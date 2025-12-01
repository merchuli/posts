---
layout: post
title: "Upload large files to github"
---

## GitHub 一般檔案上限
- 單一檔案上限：100 MB
- Repo 建議上限：約 1 GB

## 如何上傳超過 100 MB 的檔案？
Step1: 安裝 Git LFS
```sh
brew install git-lfs
```

Step2: 初始化 Git LFS
```sh
git lfs install
```

Step3: 指定要用 LFS 管理的檔案類型
```sh
git lfs track "*.zip"
git lfs track "*.mp4"
```
> Git 會建立 .gitattributes 檔案。

Step4: 正常 Git 操作
```sh
git add .
git commit -m "some message"
git push
```

### 其他
GitHub Free 的 LFS Limits 是 2 GB

## Reference
[1] [git-lfs](https://git-lfs.com/)

[2] [Github LFS Limits](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-git-large-file-storage)

