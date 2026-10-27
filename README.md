# devkit-recipes-repo
Safe devkit recipes, no unsafe toolchains, download safe devkit recipes from here
# devkit-recipe-repo 格式规范 
1. 所有的配方都要在文件夹里，配方所在的文件夹命名格式应该是`所有者@Repo name` 
2. 配方的文件名必须是`年-月-日.json` 
3. 文件夹里不可以有除配方外的任何东西
# Devkit cipe repo format specification
1. All formulas should be in a folder, and the naming format of the folder where the formula is located should be `Owner@Repo name`
2. The file name of the recipe must be `YYYY-MM-DD.json`
3. The folder cannot contain anything other than the recipe
# 声明
即使是这样，我们仍然无法保证绝对安全，因为仓库的源代码可能有问题，构建脚本可能有问题，所有强烈建议在构建前使用`devkit devlop YYYY-MM-DD.json`先配置好环境，然后认真检查源代码，最后使用`devkit build`构建
# Declaration
Even so, we still cannot guarantee absolute security as there may be issues with the source code of the repository and the build script. Therefore, we strongly recommend using `devkit devlop YYYY-MM-DD.json` to configure the environment before building, carefully check the source code, and finally use `devkit build` to build
