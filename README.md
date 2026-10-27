# devkit-recipes-repo
Safe devkit recipes, no unsafe toolchains, download safe devkit recipes from here
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
即使是这样，我们仍然无法保证绝对安全，因为仓库的源代码可能有问题，构建脚本可能有问题，所有强烈建议在构建前使用`devkit devlop YYYY-MM-DD.json`先配置好环境，然后认真检查源代码，最后使用`devkit build`构建
# Declaration
Even so, we still cannot guarantee absolute security as there may be issues with the source code of the repository and the build script. Therefore, we strongly recommend using `devkit devlop YYYY-MM-DD.json` to configure the environment before building, carefully check the source code, and finally use `devkit build` to build
