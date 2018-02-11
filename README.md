# store
用于存放相关知识点，汇总，方便以后整理和查阅，总结
# webpack
是收把项目当作一个整体，通过一个给定的的主文件，webpack将从这个文件开始找到你的项目的所有依赖文件，使用loaders处理它们，最后打包成一个或多个浏览器可识别的js文件
#### 1、配置压缩、js打包   uglifyjs-webpack-plugin
   配置入口（多）、出口（多）
  //入口文件的配置项    entry:{
        entry:'./src/entry.js',
        //这里我们又引入了一个入口文件
        entry2:'./src/entry2.js'
    },
    //出口文件的配置项    output:{
        //输出的路径，用了Node语法
        path:path.resolve(__dirname,'dist'),
        //输出的文件名称
        filename:'[name].js'
    },
    //模块：例如解读CSS,图片如何转换，压缩    module:{},
    //插件，用于生产模版和各项功能    plugins:[],
    //配置webpack开发服务功能    devServer:{}
#### 2、服务和热更新 webpack-dev-server
#### 3、Css文件打包|less文件|sass文件打包和分离
     Css分离与图片路径处理，处理html中引入的<Img>图片
     Html文件发布 html-webpack-plugin
#### 4、自动处理css3的前缀、消除未使用的css进行打包、babel支持解析es6、react等浏览器不识别的语言
#### 5、打包后调试、开发和生产环境并行设置
#### 6、模块化配置，把入口文件单独提出来
#### 7、打包第三方类库、通过watch自动打包。打包公共代码和第三方库
抽离公共的模块CommonsChunkPlugin
#### 8、集中拷贝静态资源
#### 9、Json配置文件使用，webpack3.x不需要引入json-loader
