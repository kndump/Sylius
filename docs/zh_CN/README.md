Sylius 文档
====================

这个目录包含了 Sylius 的文档 - 解耦的电子商务平台, 参见 [**docs.sylius.org**](http://docs.sylius.org). 

文档部署在 [readthedocs.org](http://readthedocs.org).

Sylius on Twitter
-----------------

如果你想随时关注所有更新, [在 twitter 上关注 Sylius 官方账号 ](http://twitter.com/Sylius).

Issues（问题）
------

本文档使用 [GitHub issues](https://github.com/Sylius/Sylius/issues).

构建
-----

在提交之前测试文档:

* [安装 `pip`, Python 包管理器](https://pip.pypa.io/en/stable/installing/)

* 安装文档依赖: 

    `$ pip install -r requirements.txt`
    
    这可以保证你获取的 Sphinx 版本号 >=1.4.2!

* 安装 [Sphinx](http://www.sphinx-doc.org/en/stable/)

    `$ pip install Sphinx`
    
    译者注：还需要执行 `pip install git+https://github.com/fabpot/sphinx-php.git` 以安装 Sphinx 对 php 的支持
    否则会报错误 [Extension error: Could not import extension sensio.sphinx.bestpractice (exception: cannot import name 'upper')](https://github.com/phpbb/documentation/issues/57)

* 进入 `docs` 目录执行 `$ sphinx-build -b html . build`，在 `build` 目录查看生成的 HTML 文件.

作者
-------

查看 [贡献者列表](http://github.com/Sylius/Sylius/contributors).
