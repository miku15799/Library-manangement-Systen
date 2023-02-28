# Library-manangement-Systen
create database test;

CREATE TABLE IF NOT EXISTS librarian (
  id int(5) NOT NULL AUTO_INCREMENT,
  name varchar(100) NOT NULL,
  password varchar(100) NOT NULL,
  email varchar(100) NOT NULL,
  address varchar(200) NOT NULL,
  city varchar(100) NOT NULL,
  contact varchar(20) NOT NULL,
  PRIMARY KEY (id)
)

INSERT INTO librarian (id,name,password,email,address,city,contact) VALUES
(1, 'Prabhakar', 'ppp', 'prabhakar@gmail.com', 'javatpoint', 'noida', '9998328238'),
(4, 'sumedh', 'sumesh', 'sumesh@gmail.com', 'Kuch Bhi', 'noida', '93823932823'),
(6, 'abhi', 'abhi', 'abhi@gmail.com', 'javatpoint', 'noida', '92393282323');



CREATE TABLE issuebooks (
  id int(11) NOT NULL AUTO_INCREMENT,
  bookcallno varchar(50) NOT NULL,
  studentid int(11) NOT NULL,
  studentname varchar(50) NOT NULL,
  studentcontact varchar(20) NOT NULL,
  issueddate timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  PRIMARY KEY (id)
);

INSERT INTO issuebooks (id,bookcallno,studentid,studentname,studentcontact,issueddate) VALUES
(4, 'A@4', 23, 'kk', '932992932', '2016-07-19 18:43:16'),
(6, 'A@4', 335, 'Sumedh', '95676565756', '2016-07-19 18:44:34'),
(7, 'A@4', 87, 'abhishek', '9329882382', '2016-07-19 18:46:12');


CREATE TABLE books(
  id int(10) NOT NULL AUTO_INCREMENT,
  callno varchar(100) NOT NULL,
  name varchar(100) NOT NULL,
  author varchar(100) NOT NULL,
  publisher varchar(100) NOT NULL,
  quantity int(10) NOT NULL,
  issued int(10) NOT NULL,
  added_date timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  PRIMARY KEY (id),
  UNIQUE KEY callno (callno),
  UNIQUE KEY callno_2 (callno)
) 

INSERT INTO books(id,callno,name,author,publisher,quantity,issued,added_date) VALUES
(1, 'A@4', 'C In Depth', 'Shrivastav', 'BPB', 2, 2, '2016-07-19 19:37:56'),
(2, 'B@1', 'DBMS', 'Korth', 'Pearson', 3, 0, '2016-07-18 18:39:52'),
(3, 'G@12', 'Let''s see', 'Yashwant Kanetkar', 'BPB', 10, 0, '2016-07-18 23:02:14');
