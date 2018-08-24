create TABLE pk10_pk_data(
	number_id int PRIMARY KEY auto_increment,
	number_of_periods int COMMENT '期数',
	pk_first int COMMENT '第一名',
	pk_two int COMMENT '第二名',
	pk_third int COMMENT '第三名',
	pk_fourth int COMMENT '第四名',
	pk_fifth int COMMENT '第五名',
	pk_sixth int COMMENT '第六名',
	pk_seventh int COMMENT '第七名',
	pk_eighth int COMMENT '第八名',
	pk_ninth int COMMENT '第九名',
	pk_tenth int COMMENT '第十名', 
	create_time timestamp NULL DEFAULT CURRENT_TIMESTAMP COMMENT '创建时间'
)auto_increment=1 engine=innodb

create table pk10_odds(
	odds_id int primary key auto_increment,
	pk_number int COMMENT '号码',
	number_odds float(10,2) DEFAULT 1 COMMENT '赔率'
)



create table beijing_pk_user(
  user_id int PRIMARY KEY auto_increment,
	username char NOT NULL COMMENT '用户名',
	`password` char NOT NULL COMMENT '密码'
)auto_increment=1 engine=innodb

-- 投注 投注的是名次(名次的基础下投注)
create table pk10_betting(
	betting_id int PRIMARY KEY auto_increment,
	betting_place_of_name char not null COMMENT '投注名次', -- 名次id
	
	betting_size char not null COMMENT '投注大小', -- 大小id
	betting_single_pair char not null '投注单双', -- 单双id
  -- 龙虎id
	user_id int COMMENT '投注用户'
)auto_increment=1 engine=innodb

select * from pk10_pk_data


create table beijing_pk_user_betting_state(
	
)auto_increment=1 engine=innodb
