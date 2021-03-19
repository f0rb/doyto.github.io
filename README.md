# DoytoQuery——一个Java实现的OSM框架

[![License](https://img.shields.io/:license-apache-brightgreen.svg)](https://www.apache.org/licenses/LICENSE-2.0.html) [![Maven Central](https://maven-badges.herokuapp.com/maven-central/win.doyto/doyto-query/badge.svg)](https://maven-badges.herokuapp.com/maven-central/win.doyto/doyto-query/) [![Sonar Stats](https://sonarcloud.io/api/project_badges/measure?project=win.doyto%3Adoyto-query&metric=alert_status)](https://sonarcloud.io/dashboard?id=win.doyto%3Adoyto-query) [![Code Lines](https://sonarcloud.io/api/project_badges/measure?project=win.doyto%3Adoyto-query&metric=ncloc)](https://sonarcloud.io/component_measures?id=win.doyto%3Adoyto-query&metric=ncloc) [![Coverage Status](https://sonarcloud.io/api/project_badges/measure?project=win.doyto%3Adoyto-query&metric=coverage)](https://sonarcloud.io/component_measures?id=win.doyto%3Adoyto-query&metric=coverage)

## 项目介绍

DoytoQuery是一个Java实现的OSM框架。OSM是 Object SQL Mapping 的缩写，不同于传统的ORM框架只负责将表列映射为Entity对象，OSM框架将一条SQL语句的三个部分——表列，表名，查询条件——分别映射为三个对象——Entity对象，IdWrapper对象，Query对象。

DoytoQuery通过将Query对象映射成WHERE语句，简化了JPA和MyBatis里拼接查询SQL的复杂写法，然后结合增删改语句的生成，抽象出DataAccess接口，替代了JPA里的JpaRepository和MyBatis里的Mapper，再在DataAccess接口的基础上封装了Service层和Controller层的常用操作，最终形成了一个开发效率更高的OSM框架。

## 功能列表：

* [Generate SQL by a query object](https://github.com/f0rb/doyto-query/wiki/Query-Suffix)
* Single table CRUD
* Dynamic table CRUD
* Service level cache
* EntityAspect extension
* Join/GroupBy Query
* Validation
* Dialect extension
* MemoryDataAccess for TDD
* UserId injection
* [Associative Service Template](https://github.com/f0rb/doyto-query/wiki/Associative-Service-Template)

[DoytoQuery Manual](https://github.com/f0rb/doyto-query/wiki/DoytoQuery%E4%BD%BF%E7%94%A8%E6%89%8B%E5%86%8C)

