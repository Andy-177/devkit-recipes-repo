# devkit-recipes-repo
DevKit recipe repository, centralized storage for DevKit recipes, security not guaranteed
# devkit-recipe-repo 格式规范 
1. 所有的配方都要在文件夹里，配方所在的文件夹命名格式应该是`所有者@仓库名` 
2. 配方的文件名必须是`年-月-日.json` 
3. 文件夹里不可以有除配方外的任何东西
4. 配方要可以正常构建
5. 开发环境，即帮你配置工具链而不构建或者配方模板只用将文件夹的命名改成`所有者$模板名`即可
# devkit-recipe-repo Formatting Guidelines  
1. All recipes must be placed in folders, and the folder name should follow the format `Owner@Repo Name`.  
2. The recipe file name must be in the format `Year-Month-Day.json`.  
3. No files other than the recipe should exist within the folder.  
4. Recipes must build successfully.  
5. For development environments—where you only configure the toolchain without building—or for recipe templates, simply rename the folder to `Owner$TemplateName`.
# 声明
我们只负责集中配方和进行少量的安全检查，强烈建议在构建前使用`devkit devlop YYYY-MM-DD.json`先配置好环境，然后认真检查源代码，最后使用`devkit build`构建
# Disclaimer  
We are only responsible for centralizing the configuration and performing minimal safety checks. We strongly recommend setting up your environment first using `devkit develop YYYY-MM-DD.json`, carefully reviewing the source code, and then building with `devkit build`.
