# Gallery-by-react
A photo  gallery project based on react from muke.

初学者，记录步骤:

```
yo --version //查看yo的版本
```

```
npm install -g generator-react-webpack //安装react-webpack
```
 
```
npm ls -g --repth-1 2>/dev/null | grep generator- //查看webpack的版本
 
 //本人结果如下:
 │ │ └── regenerator-runtime@0.9.6
├─┬ generator-react-webpack@3.3.4
├─┬ generator-reactpackage@0.0.4
│ │ └── regenerator-runtime@0.10.1
```

```
//当前目录初始化react项目
RITL-2:Gallery-by-react yuewen$ yo react-webpack Gallery-by-react
 ```
 
 ```
 npm start  //开启
 ```
 
 添加autoprefixer-loader
 ```
npm install autoprefixer-loader -save -dev
 ```
 
 修改配置文件`cfg/defaults.js`
 ```
{
  test: /\.scss/,
  loader: 'style-loader!css-loader!autoprefixer-loader?{browsers:["last 2 version"]}!sass-loader?outputStyle=expanded'
},
      
{
  test: /\.css$/,
  loader: 'style-loader!css-loader!autoprefixer-loader?{browsers:["last 2 version"]}'
},
 ```
 
 修改`styles/App.css`的后缀为`scss`
 
 修改`src/components/Main/.js`中的`require('styles/App.scss');`
 
 安装json-loader
 ```
 npm install --save-dev json-loader
 ```
