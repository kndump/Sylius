.. index::
   single: Environments

理解环境
==========================

每个Sylius应用程序都是代码和一组配置的组合，这些配置决定了代码应该如何运行。
这些配置可以定义正在使用的数据库，是否应该缓存某些内容，或者详细的日志应该如何记录。
在Symfony中，“环境”的思想是使用多种不同配置可以运行相同的代码库。
例如，开发环境应该使用让开发变得更容易和更友好的配置，而生产环境应该使用一组针对速度进行优化的配置。

开发
-----------

开发环境或``dev``，顾名思义，应该用于开发目的。 它比生产慢得多，因为它使用的缓存很少，并且对每个请求进行了大量处理。
但是，它允许您在添加新功能或快速修复Bug时，不用担心每次修改后都要清除缓存。

默认情况下，Sylius控制台应用运行在``dev``环境下。
您可以通过``web/``目录下的``/app_dev.php``文件访问dev模式下的网站。（在您的网站根目录下）

生产
----------

Production environment or ``prod`` is your live website environment. It uses proper caching and is much faster than other environments. It uses live APIs and sends out all e-mails.

To run Sylius console in ``prod`` environment, add the following parameters to every command call:

.. code-block:: bash

   $ bin/console --env=prod --no-debug cache:clear

You can access the website in production mode via the ``/app.php`` file in your website root (``web/``) or just ``/`` path. (on Apache)

Staging
-------

Staging environment or ``staging`` is the last line before the shop will go to the production. Here you should test all new features to ensure that everything works as expected.
It's almost an exact copy of production environment but with different database and turned off e-mails.

To run Sylius console in ``staging`` environment, add the following parameters to every command call:

.. code-block:: bash

   $ bin/console --env=staging --no-debug cache:clear

You can access the website in staging mode via the ``/app_staging.php`` file in your website root (``web/``) or just ``/`` path. (on Apache)

Test
----

Test environment or ``test`` is used for automated testing. Most of the time you will not access it directly.

To run Sylius console in ``test`` environment, add the following parameters to every command call:

.. code-block:: bash

   $ bin/console --env=test cache:clear

Final Thoughts
--------------

You can read more about Symfony environments in `this cookbook article <http://symfony.com/doc/current/cookbook/configuration/environments.html>`_.
