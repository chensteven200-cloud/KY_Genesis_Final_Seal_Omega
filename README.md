

# KY_Genesis_Final_Seal_Omega
# 1. 啟動 SSH Agent
eval "$(ssh-agent -s)"

# 2. 新增 SSH 金鑰（若尚未產生請先使用 ssh-keygen）
ssh-add ~/.ssh/id_ed25519

# 3. 設定 Git 使用者資訊（如尚未設定）
git config --global user.name "chensteven200-cloud"
git config --global user.email "your_email@example.com"  # ← 替換為你 GitHub 帳號綁定的 email

# 4. 設定遠端為 SSH 格式
git remote remove origin
git remote add origin git@github.com:chensteven200-cloud/KY_Genesis_Final_Seal_Omega.git

# 5. 切換分支為 main
git branch -M main

# 6. 推送本地內容到 GitHub 倉庫
git push -u origin main