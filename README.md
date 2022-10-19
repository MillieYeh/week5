# week5
### 要求三: SQL CRUD
- 使用 INSERT 指令新增一筆資料到 member 資料表中，這筆資料的 username 和 password 欄位必須是 test。接著繼續新增至少 4 筆隨意的資料。
```SQL
insert into member(name, username, passwork, follower_count) values("millie", "test", "test", 800);
insert into member(name, username, passwork, follower_count) values("coco", "coco123", "ccc", 1600);
insert into member(name, username, passwork, follower_count) values("egg", "egg456", "eee", 350);
insert into member(name, username, passwork, follower_count) values("pai", "pai789", "ppp", 2200);
```
![image](https://github.com/MillieYeh/week5/blob/main/image/3-1-add_data.png)

- 使用 SELECT 指令取得所有在 member 資料表中的會員資料。
```SQL
select * from member;
```
![image](https://github.com/MillieYeh/week5/blob/main/image/3-2-member1.png)

- 使用 SELECT 指令取得所有在 member 資料表中的會員資料，並按照 time 欄位，由近到遠排序。
```SQL
select * from member order by time desc;
```
![image](https://github.com/MillieYeh/week5/blob/main/image/3-3-member2.png)

- 使用 SELECT 指令取得 member 資料表中第 2 ~ 4 共三筆資料，並按照 time 欄位，由近到遠排序。
```SQL
select * from member order by time desc limit 1,3;
```
![image](https://github.com/MillieYeh/week5/blob/main/image/3-4-member3.png)

- 使用 SELECT 指令取得欄位 username 是 test 的會員資料。
```SQL
select * from member where username = "test";
```
![image](https://github.com/MillieYeh/week5/blob/main/image/3-5-test1.png)

- 使用 SELECT 指令取得欄位 username 是 test、且欄位 password 也是 test 的資料。
```SQL
select * from member where username = "test" and passwork = "test";
```
![image](https://github.com/MillieYeh/week5/blob/main/image/3-6-test2.png)

- 使用 UPDATE 指令更新欄位 username 是 test 的會員資料，將資料中的 name 欄位改成 test2。
```SQL
update member set name = 'test2' where username = 'test';
```
![image](https://github.com/MillieYeh/week5/blob/main/image/3-7-test3.png)
