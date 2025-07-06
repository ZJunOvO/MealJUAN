# GitHub 仓库重命名指南

## 当前状态
- 旧仓库名: `start666`
- 新仓库名: `MealJUAN`
- 中文名: 卷餐谋

## 步骤1: 在GitHub网站上重命名仓库

1. 访问你的GitHub仓库页面: https://github.com/ZJunOvO/start666
2. 点击仓库页面顶部的 **Settings** (设置) 选项卡
3. 向下滚动到 **Repository name** (仓库名称) 部分
4. 在文本框中将 `start666` 改为 `MealJUAN`
5. 点击 **Rename** (重命名) 按钮
6. 确认重命名操作

## 步骤2: 更新本地仓库的远程URL

重命名后，你需要更新本地仓库的远程URL：

```bash
# 更新远程URL
git remote set-url origin https://github.com/ZJunOvO/MealJUAN.git

# 验证更改
git remote -v
```

## 步骤3: 推送更改到新的仓库

```bash
# 切换到主分支
git checkout main

# 合并当前分支的更改
git merge cursor/clear-and-rename-github-repository-3e2e

# 推送到新的仓库
git push origin main
```

## 步骤4: 清理本地分支 (可选)

```bash
# 删除临时分支
git branch -d cursor/clear-and-rename-github-repository-3e2e
```

## 注意事项

- 重命名后，所有指向旧仓库的链接都会自动重定向到新仓库
- 如果你有其他协作者，需要通知他们更新他们的本地仓库URL
- 如果有任何CI/CD配置或其他服务集成，也需要更新相应的配置

## 仓库描述建议

在GitHub仓库设置中，建议添加以下描述：
- 英文描述: `MealJUAN - An intelligent dining solution platform`
- 中文描述: `卷餐谋 - 智能餐饮解决方案平台`

## 项目标签建议

为仓库添加以下标签 (Topics):
- `restaurant`
- `dining`
- `food-service`
- `meal-management`
- `智能餐饮`
- `餐厅管理`