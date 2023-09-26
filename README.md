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

***
* 创建模块
  ```
  nest g mo [文件目录]
  eg: nest g mo posts --no-spec
  ```
* 创建控制器
  ```nest g co [文件目录]
  eg: nest g co posts --no-spec
  ```
* 创建服务类
  ```
  nest g service [文件目录]
   eg:nest g service posts --no-spec
  ```

