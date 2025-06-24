# SimonAKing-HomePage

[English Version](<README.md>)


## 项目简介

> 一个现代优雅的个人主页，具有流体动画背景、响应式设计和流畅的页面过渡效果。

![preview](https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExMncyb3oyc21zc3czejU3cGk4M2tiNTdkaTM0N3FodGVpZmU5azNxaCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/fhXFCZEogq39rOpKUi/giphy.gif)

[在线浏览](http://simonaking.com)

嗯哼，你想为网站装上如此酷炫的主页吗?

下面就让我们开始吧！


## 安装步骤

```sh
git clone https://github.com/SimonAKing/HomePage.git
cd HomePage
npm install
npm run dev
```



## 功能特性

1. 高度封装了页面中的所有的信息
2. 使用 [WebGL-Fluid-Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation/) 作为背景
3. 使用 `less` 作为 `css` 预处理器
4. 使用 `pug` 作为 `html` 预处理器
5. 使用 `gulp` 作为构建工具, 并以配置好构建脚本
6. 令人舒服的动画 , 以及漂亮的 `UI`
7. 响应式，无缝支持移动端
8. 所引用的 `css` 与 `js` 文件总共超不过 `18.5` kb!
9. 延迟响应切换页面事件
10. 还有很多特性留给你探索...



## 项目结构

根据项目特点,一共分为两大类 ：
1. `intro` 首屏
2. `main` 副屏

相应的函数，样式，配置也是根据此标准来的。



## 基本配置

配置文件 `config.json` 中的每一项键名 , 都与相应的组件名所对应。

比如：

```json
{
	"head": {
		"title": "SimonAKing",
		"description": "Category:Personal Blog",
		"favicon": "favicon.ico"
	}
}

```
上面的配置信息就对应着下面 `layout/head.pug` 组件中的信息。
```html
head
	title #{head.title}
	meta(charset="utf-8")
	meta(name="Description" content=`${head.description}`)
	link(rel="icon" href=`${head.favicon}` type="image/x-icon")
```



## 高级配置

### WebGL-Fluid-Simulation

首页使用[WebGL-Fluid-Simulation](https://github.com/PavelDoGreat/WebGL-Fluid-Simulation/)作为背景。

如需关闭，请设置`intro.background: false`。

### supportAuthor

配置信息默认开启了 `supportAuthor` 选项，即支持作者。

所有的支持项如下：

1. 会在首页右上角显示 `章鱼猫`
2. 控制台会打印作者的站点信息

如需关闭，请设置`intro.supportAuthor: false`。

### 图标的替换
项目中的图标，全部来自 [阿里巴巴矢量图标库](https://www.iconfont.cn)

替换步骤如下:

1. 请选择好你的图标，添加到项目后，把颜色全部调成白色。
2. 点击 Font Class 方式
3. 复制生成的链接中的内容
4. 替换 文件 `css/common/icon.less` 中的内容 ，其中 `icon` 选择器中的内容必须保留。
5. 配置 `config.json` 文件中的相应项 `main.ul.*.icon`

```css
.icon {
	display: block;
	width: 1.5em;
	height: 1.5em;
	margin: 0 auto;
	fill: currentColor;
	font-family: 'iconfont' !important;
	font-size: inherit;
	font-style: normal;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}
```



## 项目部署

在根目录下执行`npm run build` 后，会将项目文件生成到 `dist` 目录。

然后，你可以将`dist`目录部署到你喜欢的服务器托管商。

下面以`GithubPage` 举例：

1. 新建 `你的用户名.github.io` 仓库

2. ```sh
   cd dist
   git init
   git add -A
   git commit -am"init"
   git remote add origin https://github.com/你的用户名/你的用户名.github.io.git
   git push -f origin master
   ```

3. 然后在`Github`设置好仓库的`GithubPage` 选项

4. 访问 `你的用户名.github.io` 即可浏览啦！



假如你之前的`用户名.github.io`仓库已经有内容了,可以新建另一个的仓库，比如`blog`。

再将所占用项目迁移到`blog`，并设置好这个仓库的`GithubPage` 选项。

而这个仓库即成为了一个子目录`用户名.github.io/blog`。

如此一来，你的`用户名.github.io`仓库便可留给首页了！



## 赞助
开发一个优秀的项目，离不开大量时间和精力的投入。

如果此项目给你带来了帮助，欢迎赞助,`star`。

谢谢！
