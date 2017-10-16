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

生产环境或``prod``是您的生产网站环境。 它使用适当的缓存，并且比其他环境快得多。 它使用生产API并会真实发送所有电子邮件。

要在``prod``环境中运行Sylius控制台，可以将以下参数添加到每个命令调用中：

.. code-block:: bash

   $ bin/console --env=prod --no-debug cache:clear

你可以通过在网站根目录(``web/``)或者``/``目录下的``/app.php``文件来访问生产模式下的网站.

Staging
-------

Staging环境或``staging``是商店上线之前的最后一步。
在这里，您应该测试所有新功能，以确保一切正常工作。
它几乎是生产环境的准确副本，只是使用不同的数据库，并关闭了电子邮件。

要在``staging``环境中运行Sylius控制台，可以将以下参数添加到每个命令调用中：

.. code-block:: bash

   $ bin/console --env=staging --no-debug cache:clear

你可以通过在网站根目录(``web/``)或者``/``目录下的``/app_staging.php``文件来访问生产模式下的网站.

测试
----

测试环境或称``test``，用于自动化测试。 大多数时候你不会直接访问它。

要在``test``环境中运行Sylius控制台，可以将以下参数添加到每个命令调用中：

.. code-block:: bash

   $ bin/console --env=test cache:clear

最后的想法
--------------

你可以通过阅读 `this cookbook article <http://symfony.com/doc/current/cookbook/configuration/environments.html>`_ 来了解更多关于 Symfony 环境的内容.
