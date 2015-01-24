---
layout: post
title: cocos2d-x 3.x 中用到的c11特性
category: linux
---

## 回调函数指针传递

在从ccMacros.h中定义了CC_CALLBACK_n系列宏，其中n为0~4，表示包裹回调函数指针的参数个数。

以触摸事件为例：

    void Test::initListener()
    {
        auto listener = EventListenerTouchOneByOne::create();
        listener->onTouchBegan = CC_CALLBACK_2(Test::onTouchBegan, this);
        listener->onTouchMoved = CC_CALLBACK_2(Test::onTouchMoved, this);
        listener->onTouchEnded = CC_CALLBACK_2(Test::onTouchEnded, this);
        listener->onTouchCancelled = CC_CALLBACK_2(Test::onTouchCancelled, this);
    }

## Lambda表达式

语法格式：[捕捉块](参数)->返回值类型{主体}

其中捕捉块是指显示指定闭包中函数需要捕捉的变量，其中包括6种表达方式：

[=]表示通过值传递捕捉所有变量;

[&]表示通过引用传递捕捉所有变量;

[var]表示通过值捕捉变量var,不捕捉其他变量;

[&var]表示通过引用捕捉var,不捕捉其他变量;

[=,&var]表示默认通过值捕捉，变量var引用捕捉;

[&,var]表示默认通过引用捕捉，变量var值捕捉

    void TestLayer::initListener(Node* node)
    {
        int var = 10;
        auto listener = EventListenerTouchOneByOne::create();
        listener->onTouchBegan = [&](Touch* touch, Event* event)->bool {
            var = 20;
            return true;
        }
        CCLOG("var : %d", var);
        this->_eventDispatcher->addEventListenerWithSceneGraphPriority(listener, node);
    }


