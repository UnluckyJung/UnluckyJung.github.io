---
title: 데이터베이스 에서의 객체와 스키마
date: 2020-11-13-16:00
categories:
- DB

tags:
- MYSQL
- DB


---

## 데이터베이스 에서의 객체와 스키마.
> `DB객체`는 DB객체, `스키마`는  DB객체를 담고 있는 그릇

---

## 객체
> OOP에서의 객체 vs DB에서의 객체

* OOP언어의 객체와 혼돈해서는 안된다.
* DB에서의 객체는 말그대로, 데이터 베이서 내의 `객체` 를 뜻하는것이다.
    * 여기서 이야기하는 `객체`는 `테이블`과 같이 데이터 베이스안에 정의하는 **모든것**을 뜻한다.
* `SQL명령` 의 경우 데이터 베이스 안에 존재하는것이 아니므로, **객체가 아니다**

---

## 스키마
> 그릇, `DDL` 명령으로 정의되어진다.

* 객체를 담는 그릇이다.
* 위에서 객체의 예시로 `테이블` 를 들었다.
* 그렇다면, `테이블`을 담고있는 `그릇`이 되는것이다.
    * `MYSQL` 같은경우는, `CREATE DATABASE` 명령으로 만들어진 `데이터베이스`가 `스키마`가 되는것이다.

---

## Reference
* [SQL 첫걸음](http://www.yes24.com/Product/Goods/22744867)