•相關網站:
https://flask-wtf.readthedocs.io/en/stable/



•Database Table 

CREATE TABLE countries (
	id serial PRIMARY KEY,
	name VARCHAR ( 60 ) NOT NULL
);

INSERT INTO
    countries(id,name)
VALUES
(1, 'Afghanistan'),
(2, 'Aringland Islands'),
(3, 'Albania'),
(4, 'Algeria'),
(5, 'American Samoa'),
(6, 'Andorra');

CREATE TABLE state (
	id serial PRIMARY KEY,
	name VARCHAR ( 60 ) NOT NULL,
	country_id INT NOT NULL
);

INSERT INTO state (id, name, country_id) VALUES (1, 'ARMM', 171);
INSERT INTO state (id, name, country_id) VALUES (2, 'Bicol', 171);
INSERT INTO state (id, name, country_id) VALUES (3, 'Central Luzon', 171);
INSERT INTO state (id, name, country_id) VALUES (4, 'Central Mindanao', 171);
INSERT INTO state (id, name, country_id) VALUES (5, 'Alabama', 227);
INSERT INTO state (id, name, country_id) VALUES (6, 'Alaska', 227);
INSERT INTO state (id, name, country_id) VALUES (7, 'Arizona', 227);
INSERT INTO state (id, name, country_id) VALUES (8, 'California', 227);
INSERT INTO state (id, name, country_id) VALUES (9, 'Florida', 227);

CREATE TABLE city (
	id serial PRIMARY KEY,
	state VARCHAR ( 60 ) NOT NULL,
	name VARCHAR ( 60 ) NOT NULL,
	stateid INT NOT NULL
);

INSERT INTO city (id, state, name, stateid) VALUES (1, 'CA', 'Anaheim', 8);
INSERT INTO city (id, state, name, stateid) VALUES (2, 'NV', 'Arden-Arcade', 8);
INSERT INTO city (id, state, name, stateid) VALUES (3, 'CA', 'Bakersfield', 8);
INSERT INTO city (id, state, name, stateid) VALUES (4, 'CA', 'Carson', 8);
INSERT INTO city (id, state, name, stateid) VALUES (5, 'NV', 'Daly City', 8);
INSERT INTO city (id, state, name, stateid) VALUES (6, 'AC', 'Angeles City', 3);
INSERT INTO city (id, state, name, stateid) VALUES (7, 'OC', 'Olongapo', 3);
INSERT INTO city (id, state, name, stateid) VALUES (8, 'SF', 'San Fernando', 3);
INSERT INTO city (id, state, name, stateid) VALUES (9, 'TA', 'Tarlac', 3);