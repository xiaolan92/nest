# 创建nest项目

```
npx @nestjs/cli new project-name

```

***

* 全局路由前缀
  
```
  async function bootstrap() {
  const app = await NestFactory.create(AppModule);
  app.setGlobalPrefix('api'); // 设置全局路由前缀
  await app.listen(9080);
}
bootstrap();
```




```
* 创建模块
  nest g mo [文件目录]
  eg: nest g mo posts --no-spec

* 创建控制器

  nest g co [文件目录]
  eg: nest g co posts --no-spec
  

* 创建服务类

  nest g service [文件目录]
  eg:nest g service posts --no-spec


* 生成新资源

nest g res feature/user --no-spec && nest g res feature/post --no-spec


```

***


* typeorm-model-generator生成entity实体类。

```
  npm i -g typeorm-model-generator
```

在工程目录中添加
src/modules/entities目录
在工程目录下的package.json中添加

```
  "scripts": {
      "db": "rimraf ./src/modules/entities & npx typeorm-model-generator -h 10.86.10.41 -d li -p 3306 -u root -x root -e mysql -o ./src/modules/entities --noConfig true --ce pascal --cp camel"
  }

```

```
-h host mysql的主机名
-d 数据库名
-p 端口号默认3306
-u 用户名
-x 密码
之后会再/src/modules/entities目录下生成对应的entity，方便的很。

```

