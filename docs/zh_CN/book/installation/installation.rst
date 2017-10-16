.. index::
   single: Installation

安装
============

Sylius主程序可以直接面向用户使用，也可以作为您定制电子商务应用程序的基础。

.. warning::

    本篇文档假设你熟悉PHP的依赖管理工具 `Composer`_, 且你已经全局安装了它 `Composer installed globally`_.

.. note::

    如果你只下载了 Composer 的 phar 归档文件, 本指南中使用  ``composer``的地方，你应该用 ``php composer.phar``.

.. tip::

    如果你更习惯在 **Vagrant** 下工作，参阅 :doc:`本指南 </book/installation/vagrant_installation>`.

安装一个Sylius新项目
-------------------------------

要使用Sylius的标准版本创建一个新项目, 执行如下命令:

.. code-block:: bash

    $ composer create-project sylius/sylius-standard acme

.. note::

    确保使用高于7.1的PHP版本。使用较旧的PHP版本将导致安装较旧版本的Sylius。

这将在``acme``目录中创建一个新的Symfony项目。
当安装好所有的依赖关系，你将通过交互式脚本将配置写入``parameters.yml``文件。
请按照步骤一步步操作。
执行结束后，在执行以下命令：

.. code-block:: bash

    $ cd acme # 进入新建的acme目录
    $ php bin/console sylius:install

这个软件包在vendor目录涵盖了所有的 ``sylius/sylius`` 包, 所以你可以轻松的更新，并专注于你的定制化开发。

.. warning::

    在``sylius:install``命令执行期间，你会被要求提供一下重要信息. 当然它也提供了一些默认选项, 默认**币种**(USD), 默认**地区**(English - US).
    你稍后可以在``parameters.yml``文件中修改他们.
    配置好之后，所有的价格将以美元为币种整数存储在数据库中，所有的产品也会被翻译为英文名称。

安装 assets
-----------------

为了看到一个功能齐全的前端页面，你需要安装assets.

**Sylius** 已经自带了 ``Gulpfile.js`` 文件, 因此你只需要使用 `Yarn`_ 安装 `Gulp`_ 即可.

.. note::

    我们推荐使用稳定版本 (`^1.0.0`) 的 `Yarn`_.

安装好Yarn之后，进入到项目目录，执行:

.. code-block:: bash

    $ yarn install

然后，你只需要执行如下简单的命令，即可使用gulp安装视图:

.. code-block:: bash

    $ yarn run gulp

当然，如果你已经全局安装了Gulp，只需要执行:

.. code-block:: bash

    $ gulp

访问商店
------------------

.. tip::

    我们强烈推荐执行 ``php bin/console server:start 127.0.0.1:8000`` 命令, 以使用Symfony内建的web服务器.
    然后，便可以用浏览器访问 ``http://127.0.0.1:8000`` 就可以看到商店了.

.. note::

    本机的8000端口可能已经被其他进程占用.
    如果你想尝试其他端口，可以使用命令 ``php bin/console server:start 127.0.0.1:8081``.
    如果要了解更多关于内建服务器的内容，参阅 `这里 <http://symfony.com/doc/current/cookbook/web_server/built_in.html>`_.

您可以使用在安装过程中提供的凭据以管理员身份登录。
现在，您可以使用干净的Sylius了。

访问管理后台
----------------------------------

.. note::

    你可以通过访问 ``/admin`` 链接来打开管理员面板.
    记住你需要使用在安装Sylius时提供的管理员身份凭据来登录.

如何开始开发? - 项目结构
--------------------------------------------

在成功安装了 **Sylius-标准版** 之后，你可能就要在Sylius框架内进行开发了.

在项目的根目录，你会看到如下这些重要的子目录:

* ``app/config/`` - 你可以在这里添加yaml配置文件, 包括路由(routing), 安全(security), 状态机(state machines) 等配置.
* ``var/logs/`` - 应用的日志
* ``var/cache/`` - 应用的缓存
* ``src/`` - 你可以把自己的定制逻辑放置在这里的 ``AppBundle`` 目录
* ``web/`` - 项目的资源(assets)文件

.. tip::

    正如之前提到的，我们基于Symfony，所以我们采用了它的架构方法。
    参阅 `Symfony 文档 <http://symfony.com/doc/current/quick_tour/the_architecture.html>`_.
    参阅 `项目架构最佳实践 <http://symfony.com/doc/current/best_practices/creating-the-project.html#structuring-the-application>`_.

贡献
------------

.. tip::

    如果你想为Sylius贡献源码 - 请参见 :doc:`贡献指南 </contributing/index>`

.. _Gulp: http://gulpjs.com/
.. _Yarn: https://yarnpkg.com/lang/en/
.. _Composer: http://packagist.org
.. _`Composer installed globally`: http://getcomposer.org/doc/00-intro.md#globally
