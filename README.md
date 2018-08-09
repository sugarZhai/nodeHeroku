# nodeHeroku
node的一个爬虫示例部署上线
最近看了一篇博客，看到了node爬虫的简单demo还有如何部署上线的内容，简单的罗列了一下流程  
1、引用node中cheerio、superagent插件实现爬虫  
2、增加Procfile文件   
web: node app.js  
//app.js
app.listen(process.env.PORT || 5000)  

3、接下来去herkou网站注册账号https://www.heroku.com/ 需要翻墙，而且未绑定信用卡用户只能有5个app部署限额
4、下载它的工具包https://toolbelt.heroku.com/
5、heroku create 文件一定要在根目录下  
6、git remote -v 随机分配git仓库给我们，然后执行git remote -v之后会有远程heroku仓库展示
7、git push heroku master  
8、heroku open 自动生成的路径就是最后部署上线的路径，可做API接口使用

最后部署上线会有一个随机的域名https://safe-reef-69064.herokuapp.com/

