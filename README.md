## Systematization GitHub Stars

---

### Test URL

-  http://asdfasdfasdf

---

### Screenshots 

[](***.gif)

---

### Technology stack

- Basic < HTML_5 
- Basic < CSS_3 
- Basic < JavaScript : Programming language
- Basic < PHP : Programming language
- Ad < Docker : Virtualization container
- Ad < Laravel : PHP Framework
- Ad < Vue.js : Framework

---

###  Characteristics & Requirements 

- [x] The web application use `HTML_5` and `CSS_3` for page content and layout.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application have a consistent design/interface.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application is well-structured and logically organized. 

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] LogIn & LogOut < Default { `Username : test `; `Passwd : pass `}.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application utilize PHP and proper PHP techniques.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application properly use `GET` and `POST`.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] Supply appropriate and informative feedback if the information entered is not complete or correct.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application contain a page where there are multiple photos presented on the page. 

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application contain a page that contains a YouTube video embedded in the page.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application utilize JavaScript and proper JavaScript techniques.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application utilize jQuery and proper jQuery techniques.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application utilize Bootstrap interface elements.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

- [x] The web application utilize AJAX.

> File path : "/";
>
> Line : 0 ;
>
> Other prompt : " ";

### Usage

``` 
./a.out username > star_raw.json (根据用户名抓取该用户的Star.json) 
./a_1.out (根据star_raw.json筛选有用字段生成star.json 文件)
./b.out search > part Of star.json (在已知star.json的情况下根据部分词匹配合适的项目)
./c.out add -repo {repo_name} -tag {tag_name} 加入某repo的tag
./c.out del -repo {repo_name} -tag {tag_name} 删除某repo的tag
./c.out delall -repo {repo_name} 删除某repo的所有tag
./d.out add -repo {repo_name} -des {description string} 加入某repo的description
如果没有手动加入则制空
./d.out del -repo {repo_name} 删除某repo的所有description
./e.out 根据 [Json文件 | 数据库记录] > 生成 markdown 文档 : Readme.md 同时 
提交 star.lock.json
```

### Install 

#### without docker in Ubuntu

- Install Composer

```bash
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```

- Install Laravel

```bash
composer create-project laravel/laravel SysGithubStar ^5.5
```

- Install Apache

- 配置 Apache 配置文件

  ```
  cd /etc/apache2/
  cd sites-available/
  sudo vim 000-default.conf
  # 更改 为 
  DocumentRoot /var/www/html/SysGithubStar/public/
  ```

  ​

- Enable Apache rewrite mod ; make sure Laravel 's Route rules work.

  ```bash
  sudo a2enmod rewrite # 引入Mod
  sudo vim apache2.conf # 更改 apache 配置文件
  # 将 <Directory /var/www/> </Directory> 中 AllowOverride 项 改成 AllowOverride all
  service apache2 restart # 重启 apache
  ```

  ​

### With Docker

- Install Docker



---

### 项目组织

```
- composer 类文件 composer.json , composer.lock 
(PHP 项目包管理系统类似于 ruby:gem ; python:pip ; java:maven;javascript:npm)
- /public 放置 html js css
- /resource 放置 html 模板文件
- /vendor 放置 在 composer.json 中 描述的依赖库
- /routes 放置 描述 routes rules 的文件 
```













## Other

```
根据 GITHUB API：
Requests that return multiple items will be paginated to 30 items by default. You can specify further pages with the ?page parameter. For some resources, you can also set a custom page size up to 100 with the ?per_page parameter. Note that for technical reasons not all endpoints respect the ?per_page parameter, see events for example.
关于分页:
https://developer.github.com/v3/guides/traversing-with-pagination/

header 中 Link:
<https://api.github.com/user/24313133/starred?page=1&q=addClass+user%3Amozilla>; rel="prev", <https://api.github.com/user/24313133/starred?page=3&q=addClass+user%3Amozilla>; rel="next", <https://api.github.com/user/24313133/starred?page=8&q=addClass+user%3Amozilla>; rel="last", <https://api.github.com/user/24313133/starred?page=1&q=addClass+user%3Amozilla>; rel="first"
```



```
页面导航
/ -> index.php (上面字符串视频嵌入 下面是用过的人的截图和评论 中间是去主页面的按钮) -> 
-> systar_home.php (主功能区 搜索框 错误提示 通过 jQuery post UserName 到 返回 JSON ,根据返回的JSON javascript 构造 前端) (同时可以解析 经过用户处理的JSON 并显示出来) 用户可以给UNIT 添加 description 和 Tag）（为了根据界面逆向生成相应的JSON，需要一个新的parseHTML -> JSON 的javascript函数）（使用JSON 生成 Markdown 文件）
-> systar_fun.php (根据 POST 过来的数据 来 获取 JSON map 到 新 JSON)
```



- Enjoy & Cheers :)