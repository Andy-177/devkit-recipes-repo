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
# 安全配方(Safe recipe)
安全配方是配方下载的内容里没有由开发者自己写的构建脚本，比如xxx.bat这种，当然源代码里的不算，比如build.gradle，但是不允许通过download，unpack，unzip的方式加我外部脚本用于构建。同时构建用的工具链应该都是官方的链接，而不能是自己的链接，链接必须来自官方项目或官网，且工具链里不能含有自己写的不知名工具链。所有的安全配方都会列到安全配方列表里供参考。但即使这样，安全配方任然不一定安全，依然强烈建议检查。

The secure recipe does not include the build scripts written by the developer themselves in the downloaded recipe content, such as xxx.bat. Of course, this does not include the source code, such as build.gradle. However, it is not allowed to add external scripts for building through download, unpack, or unzip methods. At the same time, the toolchain used for building should all be official links, not self-made links. The links must come from official projects or official websites, and the toolchain should not contain unknown tools written by oneself. All secure recipes will be listed in the secure recipe list for reference. But even so, the secure recipe is still not necessarily safe, and it is strongly recommended to check.

# 安全配方列表(Safe recipe list)
  - amd989@Symlinker
