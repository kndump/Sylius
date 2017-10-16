The Book
========

针对开发者如何灵活使用Sylius的一份指南. 你可以在这里找到Sylius平台使用到的所有概念.
帮助你理解Sylius是如何工作的.

介绍
------------

介绍部分旨在描述 Sylius 的哲学. 同时也会教你一些在安装它之前的环境问题.

.. toctree::
    :hidden:

    introduction/index

.. include:: /book/introduction/map.rst.inc

安装
------------

安装章节当然是在你的机器上安装Sylius的综合指南，但它也提供了关于在你的项目中升级Sylius的一般说明。

.. toctree::
    :hidden:

    installation/index

.. include:: /book/installation/map.rst.inc

架构
------------

了解Sylius内部组织原则的关键。 在这里您将了解资源层(Resource layer)、状态机(State machine)、事件(vent)
和一些非电子商务相关但是在Sylius中被采用的概念，如电子邮件或夹具(Fixtures)。

译者注：Fixtures 是测试中非常重要的一部分。他们的主要目的是建立一个固定/已知的环境状态以确保测试 可重复并且按照预期方式运行

.. toctree::
    :hidden:

    architecture/index

.. include:: /book/architecture/map.rst.inc

配置
-------------

了解了Sylius的架构基础知识，我们将介绍三个最重要的概念 - 渠道(Channels)、区域(Locales)和货币(Currencies)。
必须先配置这些内容，才能启动和运行Sylius应用程序。

.. toctree::
    :hidden:

    configuration/index

.. include:: /book/configuration/map.rst.inc

顾客
---------

本章将详细介绍Sylius处理用户、顾客和管理员的方式。
还有一个专门针对顾客地址管理的子章节。

.. toctree::
    :hidden:

    customers/index

.. include:: /book/customers/map.rst.inc

产品
--------

这是一份帮助了解Sylius产品处理及其周边概念的指南。
阅读关于协会(Associations)、评论(Reviews)、属性(Attributes)、分类(Taxons)等部分。

.. toctree::
    :hidden:

    products/index

.. include:: /book/products/map.rst.inc

购物车 & 订单
--------------

在本章中，您将了解到关于Sylius订单所需的一切。
这个概念还和一些额外的概念相结合，例如促销(promotions)，付款(payments)，出货(shipments)或结帐(checkout)。

如果你正在找Sylius中处于``cart``状态的订单，你也需要阅读本章节。

.. toctree::
    :hidden:

    orders/index

.. include:: /book/orders/map.rst.inc

主题
------

你会在这里学习自定义Sylius主题的基础知识。如何改变自己店铺的主题？继续学习吧！

.. toctree::
    :hidden:

    themes/index

.. include:: /book/themes/map.rst.inc