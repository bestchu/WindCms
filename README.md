
WindCms是一套基于October,Laravel 二次开发，简单易用的CMS，通过简单的配置后开箱即可使用。

[![Build Status](https://travis-ci.org/octobercms/october.svg?branch=develop)](https://travis-ci.org/octobercms/october)
[![License](https://poser.pugx.org/october/october/license.svg)](https://packagist.org/packages/october/october)

### 学习使用WindCms

英文文档，请参照[october](http://octobercms.com/docs)
中文文档，正在完善中。

### 安装使用

1. 下载WindCms并解压

   ```
   curl -o WindCms.zip https://codeload.github.com/bestchu/WindCms/zip/master
   ```

2. 解压文件到指定目录
   ```
   unzip WindCms.zip -d WindCms
   ```

3. 进入WindCms目录

   ```
   cd WindCms/WindCms-master/
   ```

4. 安装系统依赖包,composer安装使用请参照[composer中文网](http://docs.phpcomposer.com/)

   ```
   composer update
   ```

5. 配置PHP 命令行工具

   ```
   #修改php.cmd文件中的 G:\phpStudy\php55n\php.exe 文你的项目需要使用的php版本文件路径
   ```

6. 为应用程序生成新的key

   ```
   php artisan key:generate
   ```

7. 配置数据库连接方式

   ```
   #编辑config/database.php文件，配置需要使用的数据库连接方式
   'connections' => [
     '配置名称' => [
       //配置选项
       'driver'    => 'mysql',//数据库类型
       'host'      => 'localhost',//主机地址
       'port'      => '',//数据库端口
       'database'  => 'database',//数据库名称
       'username'  => 'root',//用户名
       'password'  => 'root',//密码
       'charset'   => 'utf8',//数据库字符集
       'collation' => 'utf8_unicode_ci',//数据库校验字符集
       'prefix'    => '',//表前缀
     ]
   ]
   # 配置 default 为数据库配置名称
   'default' => '配置名称'
   ```

8. 还原填充数据库

   ```
   php artisan october:up
   ```

9. 启动Web Server

   ```
   php -S localhost:8080 server.php
   ```

10. 访问Cms管理后台 [http://localhost:8080/backend](http://localhost:8080/backend)

   ```
   #默认用户名 admin
   #默认密码 admin
   ```

### 开发学习

> 二次开发，请先学习laravel框架，中文学习文档地址：[laravel中文网](http://www.golaravel.com/)
>
>    开发索引
>
> 1. [Ajax开发](http://octobercms.com/docs/cms/ajax)
>
> 2. 模板 [语法](http://octobercms.com/docs/markup/templating) ,更多语法请参照[twig模板引擎语法](docs/template/twig.md)
>

### 联系我

你能通过以下方式联系到我:

* [QQ](tencent://message/?uin=419412545&Site=github.com&Menu=yes) 419412545
* [邮箱](mail://newi@qq.com) newi@qq.com

### License

请遵循october开源许可 [MIT license](http://opensource.org/licenses/MIT).

### 编码规范

请遵循以下编码规范

* [PSR 4 Coding Standards](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-4-autoloader.md)
* [PSR 2 Coding Style Guide](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-2-coding-style-guide.md)
* [PSR 1 Coding Standards](https://github.com/php-fig/fig-standards/blob/master/accepted/PSR-1-basic-coding-standard.md)
