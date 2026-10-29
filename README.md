# devkit-recipes-repo
DevKit recipe repository, centralized storage for DevKit recipes, security not guaranteed

# devkit-recipe-repo 格式规范

1. 所有的配方都要在文件夹里，配方所在的文件夹命名格式应该是`所有者@仓库名`。
2. 文件夹里只能有配方、配方所需的资产以及README.md说明文件，资产即用于辅助构建或初始化环境的脚本等文件的集合，资产必须是zip格式。
3. 配方要可以正常构建。
4. 开发环境，即帮你配置工具链而不构建或者配方模板只用将文件夹的命名改成`所有者$模板名`即可。
5. 如果是供多个配方公用的资产算作模板，使用模板的命名规则即可，模板里面并不是必须要有配方，模板也可以是纯资产。

# devkit-recipe-repo Format Specification

1. All recipes must be placed in a folder. The folder name should follow the format of "Owner@Repository Name".
2. Only recipes, the assets required for the recipes, and a README.md documentation file can be in the folder. The assets are a collection of files used to assist in building or initializing the environment. The assets must be in zip format.
3. The recipe must be able to be built normally.
4. Development environment, which helps configure the toolchain without building or the recipe template only needs to change the folder naming to "Owner$Template Name".
5. If the assets are for common use by multiple recipes, they are considered as templates. The naming rule for templates can be used, and the template does not necessarily have to contain a recipe. The template can also be pure assets.

# 声明
我们只负责集中配方和进行少量的安全检查，强烈建议在构建前使用`devkit devlop 文件名.json`先配置好环境，然后认真检查源代码，最后使用`devkit build`构建

# Disclaimer
We are only responsible for centralizing the configuration and performing minimal safety checks. We strongly recommend setting up your environment first using `devkit develop FileName.json`, carefully reviewing the source code, and then building with `devkit build`.

# 安全配方(Safe recipe)
安全配方是配方下载的内容里没有由开发者自己写的构建脚本，比如xxx.bat这种，当然源代码里的不算，比如build.gradle，但是不允许通过download，unpack，unzip的方式加我外部脚本用于构建。同时构建用的工具链应该都是官方的链接，而不能是自己的链接，链接必须来自官方项目或官网，且工具链里不能含有自己写的不知名工具链。所有的安全配方都会列到安全配方列表里供参考。但即使这样，安全配方任然不一定安全，依然强烈建议检查。

The secure recipe does not include the build scripts written by the developer themselves in the downloaded recipe content, such as xxx.bat. Of course, this does not include the source code, such as build.gradle. However, it is not allowed to add external scripts for building through download, unpack, or unzip methods. At the same time, the toolchain used for building should all be official links, not self-made links. The links must come from official projects or official websites, and the toolchain should not contain unknown tools written by oneself. All secure recipes will be listed in the secure recipe list for reference. But even so, the secure recipe is still not necessarily safe, and it is strongly recommended to check.

安全配方列表只包含用于构建的配方，不包含模板

The safe recipe list only includes formulas for building, not templates.

# 安全配方列表(Safe recipe list)
  - amd989@Symlinker
