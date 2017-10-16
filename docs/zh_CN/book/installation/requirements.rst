.. index::
    single: System Requirements

系统要求
===================

Here you will find the list of system requirements that have to be adhered to be able to use **Sylius**.
在这里，您将找到使用**Sylius**所必需系统要求列表。
首先，看一下 `运行Symfony的要求 <http://symfony.com/doc/current/reference/requirements.html>`_.

参阅 `LAMP栈 <https://en.wikipedia.org/wiki/LAMP_(software_bundle)>`_ 和 `MAMP栈 <https://en.wikipedia.org/wiki/MAMP>`_.

操作系统
-----------------

运行Sylius的推荐操作系统是Unix系统 - **Linux, MacOS**.

Web服务器和配置
----------------------------

在生产环境中，建议使用2.2版本及以上的Apache Web服务器。

在开发时，推荐使用由Symfony封装的PHP的内置Web服务器。

`在这里 <http://symfony.com/doc/current/cookbook/configuration/web_server_configuration.html>`_ 可以查看完整的Web服务器配置参考。

PHP必需的模块和相关配置
--------------------------------------

**PHP 版本**:

+---------------+-----------------------+
| PHP           | ^7.1                  |
+---------------+-----------------------+

**PHP 扩展**:

+-------------+---------------------------+
| `gd`_       | No specific configuration |
+-------------+---------------------------+
| `exif`_     | No specific configuration |
+-------------+---------------------------+
| `fileinfo`_ | No specific configuration |
+-------------+---------------------------+
| `intl`_     | No specific configuration |
+-------------+---------------------------+

**PHP 配置**:

+---------------+-----------------------+
| memory_limit  | ≥1024M                |
+---------------+-----------------------+
| date.timezone | Europe/Warsaw         |
+---------------+-----------------------+

.. warning::

    使用您当地的时区，例如America/Los_Angeles或Europe/Berlin。 有关所有可用时区的列表，请参阅 http://php.net/manual/en/timezones.php .

数据库
--------

默认情况下，数据库连接已预先配置为使用以下MySQL配置：

+---------------+-----------------------+
| MySQL         | 5.x                   |
+---------------+-----------------------+

.. note::

    当然，您也可以使用其他任何 RDBMS，例如 PostgreSQL.

访问权限
-------------

大多数应用程序文件夹和文件只需要读权限，但是一些文件夹还需要Apache/Nginx用户的写权限：

* var/cache
* var/logs
* web/media

你可以在 `Symfony - 设置权限 <http://symfony.com/doc/current/setup/file_permissions.html>`_ 部分阅读如何设置这些权限.

.. _`gd`: http://php.net/manual/en/book.fileinfo.php
.. _`exif`: http://php.net/manual/en/book.exif.php
.. _`fileinfo`: http://php.net/manual/en/book.fileinfo.php
.. _`intl`: http://php.net/manual/en/book.intl.php
