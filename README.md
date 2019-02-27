# sql-citybase

SQL dumps for all US states and cities (around 30,000 in total) with county and long / lat coordinates.

### Table Schemas

#### us_states

	  id INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	  state_code CHAR(2) NOT NULL,
	  state_title VARCHAR(50) NOT NULL,
	  PRIMARY KEY (id)

#### us_cities

	  id INT(10) UNSIGNED NOT NULL AUTO_INCREMENT,
	  id_state INT(10) UNSIGNED NOT NULL,
	  city_title VARCHAR(100) NOT NULL,
	  city_county VARCHAR(100) DEFAULT NULL,
	  city_latitude VARCHAR(100) DEFAULT NULL,
	  city_longitude VARCHAR(100) DEFAULT NULL,
	  PRIMARY KEY (id)
