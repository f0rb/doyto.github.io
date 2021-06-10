# DoytoQuery——第二代ORM框架的Java实现

[![License](https://img.shields.io/:license-apache-brightgreen.svg)](https://www.apache.org/licenses/LICENSE-2.0.html) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/win.doyto/doyto-query/badge.svg)](https://maven-badges.herokuapp.com/maven-central/win.doyto/doyto-query/) [![Sonar Stats](https://sonarcloud.io/api/project_badges/measure?project=win.doyto%3Adoyto-query&metric=alert_status)](https://sonarcloud.io/dashboard?id=win.doyto%3Adoyto-query) [![Code Lines](https://sonarcloud.io/api/project_badges/measure?project=win.doyto%3Adoyto-query&metric=ncloc)](https://sonarcloud.io/component_measures?id=win.doyto%3Adoyto-query&metric=ncloc) [![Coverage Status](https://sonarcloud.io/api/project_badges/measure?project=win.doyto%3Adoyto-query&metric=coverage)](https://sonarcloud.io/component_measures?id=win.doyto%3Adoyto-query&metric=coverage)

## 项目介绍

DoytoQuery是第二代ORM框架的一个Java实现。

## 第二代ORM框架概述

**核心理念：将SQL语句映射为对象进行数据库访问操作**

**1. 一条SQL语句最多映射为三个对象**

1. WHERE语句映射为Query对象
   * 每条查询语句都包含了隐式分页和排序
   * 查询字段可以通过以下三种方式映射为条件语句
     * 字段后缀映射
     * 嵌套查询注解
     * 自定义查询注解
2. SELECT语句映射为Entity对象
3. 水平分表的动态表名由IdWrapper对象确定

**2. SQL访问语句可以归为三类**

1. 单表增删查改
   * 基于上述三个对象映射单表的增删查改语句
2. 中间表操作
   * 表结构类似，变量部分有3个：表名，左表外键列名，右表外键列名
   * 只有增删查操作，没有修改操作
   * 根据上述变量可以生成对应的增删查语句
3. 聚合/连接查询
   * 只有查询操作
   * 复用Query对象生成查询语句
   * Entity对象的字段的注解用于拼接SELECT语句
   * 在Entity对象上使用注解拼接JOIN和GROUP BY语句

## 功能列表：



[DoytoQuery Manual](https://github.com/f0rb/doyto-query/wiki/DoytoQuery%E4%BD%BF%E7%94%A8%E6%89%8B%E5%86%8C)

