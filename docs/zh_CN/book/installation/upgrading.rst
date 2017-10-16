.. index::
   single: Upgrading

升级
=========

Sylius会不时发布新版本。 每个版本都对应一个 `UPGRADE <https://github.com/Sylius/Sylius/blob/1.0/UPGRADE-1.0.md>`_ 文件，
这对于升级过程是很有帮助的，特别是对于主要版本，可能会破坏向后兼容性。

**通过修改** ``composer.json`` **文件来更新Sylius库约束:**

.. code-block:: yaml

    {
        ...

        "require": {
            "...": "...",

            "sylius/sylius": "^1.0@beta",

            "...": "...",
        },

        ...
    }

**然后执行** ``composer update`` **命令:**

.. code-block:: bash

    $ composer update sylius/sylius

如果这导致出现依赖性错误，则可能意味着其他Sylius所依赖的库也必须升级。
使用如下命令可以帮助您升级Sylius依赖关系。

.. code-block:: bash

    $ composer update sylius/sylius --with-dependencies

如果这并没有起作用，就应该调试一下版本冲突，查看一下你的``composer.json``文件内容.

**最终要使一切工作顺利完成，记得检查Sylius的UPGRADE文件的说明。**

**更重要的一件事情，要执行数据库迁移:**

.. code-block:: bash

    $ bin/console doctrine:migrations:migrate

.. tip::

    检查一下迁移文件是否存在于 ``app/migrations`` 目录.
    如果没有的话，使用 ``vendor/sylius/sylius/app/migrations/`` 目录下的迁移文件替换该目录下的文件.

根据upgrade文件说明并执行完数据库迁移后，你的升级工作也就完成了.
