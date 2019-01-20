# xu-design 一个VUE UI 组件库
作者：再睡一夏

``` bash
# mkdir xu-design
创建xu-design文件夹

# cd xu-design & touch READMD.md
进入到xu-design文件夹，然后创建READMD.md文件

# vi READMD.md
使用vim编辑READMD.md文件，添加仓库信息，编辑完成后Esc+:wq保存退出

# git init
有两种取得 Git 项目仓库的方法。 第一种是在现有项目或目录下导入所有文件到 Git 中； 第二种是从一个服务器克隆一个现有的 Git 仓库。
如果你打算使用 Git 来对现有的项目进行管理，只需要进入该项目目录并输入：`git init`命令来初始化仓库

# git add .
使用命令 git add + 文件名 开始跟踪一个文件。 所以，要跟踪 README 文件，运行：`git add README`
使用`git add .`命令会把目录下所有文件的变化提交到暂存区，包括文件内容修改(modified)以及新文件(new)，但不包括被删除的文件。

# git commit -m 'init'
将暂存区的所有修改提交到当前分支

# git push
把当前分支推送到远程仓库

# npm init
npm init用来初始化生成一个新的package.json文件，该文件定义了项目的配置信息，还有项目依赖的模块。
package.json存在时，直接运行命令:npm install 或者 npm install xxx --save会自动将package.json中记录的项目依赖的模块安装到node-modules文件夹下。

# npm i vue
npm 6.0版本开始不需要加--save,默认和面会加上--save
npm i是npm install的简写

# npm i -D parcel-bundler
如果一个包是给用户使用的npm i 后面是不用加-D(这个D是devDependencies，即developer dependencies，开发者依赖的意思)，如果是给开发者使用的包后面就要加上-D
```
