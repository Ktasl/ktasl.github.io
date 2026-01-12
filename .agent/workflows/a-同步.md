---
description: Safe Git Sync - 推送本地 commits 並同步 dev/main 分支
---

# Safe Git Sync Workflow

## ⚠️ 安全檢查
在同步前確保本地 commit 都已推送，避免遺失工作。

---

## 步驟

### 1. 檢查是否有未 commit 的變更
```bash
git status
```
> 如果有未 commit 的變更，請先使用 `/發佈` 或手動 commit/push

### 2. 確認目前分支
```bash
git branch --show-current
```

### 3. 推送 dev 到 remote (若存在)
```bash
# Check if dev branch exists before pushing
if git show-ref --verify --quiet refs/heads/dev; then
    echo "Pushing dev branch..."
    git push origin dev
else
    echo "Dev branch not found, skipping push."
fi
```

### 4. 同步 main 分支
```bash
git checkout main
```

```bash
# Update main from remote first (using rebase to handle divergence)
git pull --rebase origin main
```

```bash
# Merge latest dev into main (If dev exists)
if git show-ref --verify --quiet refs/heads/dev; then
    echo "Merging dev into main..."
    git merge dev
else
    echo "Dev branch not found, skipping merge."
fi
```

```bash
// turbo
git push origin main
```

### 5. 切回 dev 分支 (若存在)
```bash
if git show-ref --verify --quiet refs/heads/dev; then
    git checkout dev
else
    echo "Dev branch not found, staying on main."
fi
```

---

> [!WARNING]
> 如果有未推送的 commits，請先執行 `git push origin dev` 再同步！
