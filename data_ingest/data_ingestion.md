1.  CREATE TABLE collision(crashDate STRING, crashTime STRING, borough STRING, zipcode INT, latitude DOUBLE, longitude DOUBLE, location STRING, onStreet STRING, crossStreet STRING, offStreet STRING, personInjured INT, personKilled INT, pedestrianInjured INT, pedestrianKilled INT, cyclistInjured INT, cyclistKilled INT, motoristInjured INT, motoristKilled INT, factor1 STRING, factor2 STRING, factor3 STRING, factor4 STRING, factor5 STRING, collisionId INT, code1 STRING, code2 STRING, code3 STRING, code4 STRING, code5 STRING) COMMENT 'collisions' ROW FORMAT DELIMITED FIELDS TERMINATED BY ',' STORED AS TEXTFILE;

create table mta(time STRING, subway INTEGER, subway_percent DOUBLE, ride INTEGER, ride_percent DOUBLE, LIRR INTEGER, LIRR_percent DOUBLE, Metro_North INTEGER, Metro_percent DOUBLE, Access INTEGER, Access_percent Float, traffic INTEGER, traffic_percent Double ) ROW FORMAT DELIMITED FIELDS TERMINATED BY ',' STORED AS TEXTFILE;

2. Copy input data manually to HDFS location '/user/<net_id>/messages2' as given below.

load data inpath '/user/th2160/project/collision.csv' into table collision;

load data inpath '/user/th2160/project/daily.csv' into table mta;


3. Query the table 'collision' on hive.
