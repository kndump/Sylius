.. index::
   single: Installation via Vagrant

使用Vargrant安装Sylius
===============================

.. warning::

    本篇文档假设你熟悉PHP的依赖管理工具 `Composer`_, 且你已经全局安装了它 `Composer installed globally`_.
    关于 `Vagrant <https://www.vagrantup.com/about.html>`_ 和 `安装 Vagrant <https://www.vagrantup.com/docs/installation/>`_ 的基础知识也是必须的。

什么是 Vagrant?
---------------

Vagrant是构建完整开发环境的工具.
对Sylius来说, Vagrant将帮助您快速在计算机上构建完整的应用程序。

.. tip::

    参阅 `Vagrant <https://www.vagrantup.com/about.html>`_.
    参阅 `安装 Vagrant <https://www.vagrantup.com/docs/installation/>`_.

如何使用Vagrant安装Sylius?
------------------------------------

2. 克隆`Sylius/Vagrant <https://github.com/Sylius/Vagrant>`_ 仓库到 ``/sylius/`` 目录:

.. code-block:: bash

    $ git clone git@github.com:Sylius/Vagrant.git sylius

3. 进入到 ``/sylius/`` 目录，并构建Vagrant:

.. code-block:: bash

    $ cd sylius
    $ vagrant up

4. 在 ``etc/hosts`` 文件中添加对 sylius.dev 的解析:

.. code-block:: bash

    # etc/hosts
    10.0.0.200      sylius.dev www.sylius.dev

现在，你就可以通过 ``http://sylius.dev/app_dev.php`` 来访问Sylius应用了.

.. _Composer: http://packagist.org
.. _`Composer installed globally`: http://getcomposer.org/doc/00-intro.md#globally
