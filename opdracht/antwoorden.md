# Antwoorden Eindopdracht

1. Copy paste je gemaakte SQL query hieronder

SELECT r.name race, c.name circuit 
FROM circuits c 
JOIN races r 
ON c.circuitId = r.circuitId 
WHERE year = 
(SELECT MAX(year) FROM races)
   
2. Copy paste je gemaakte SQL query hieronder
   
SELECT name, surname, points 
FROM driver_standing ds 
JOIN races r 
ON ds.raceId = r.raceId
JOIN drivers d
ON d.driverId = ds.driverId
WHERE year = 2017
AND points = 10

3. Copy paste je gemaakte SQL query hieronder

SELECT forename, surname, duration
FROM drivers d
JOIN pitstops p
ON d.driverId = p.driverId
WHERE duration < 25
   
4. Copy paste je gemaakte SQL query hieronder

SELECT c.name constructor, r.name grandprix
FROM constructor_standing cs
JOIN races r
ON r.raceId = cs.raceId
JOIN constructors c
ON c.constructorId = cs.constructorId
WHERE year = 2010
AND c.name = 'mclaren'
   
5. Copy paste je gemaakte SQL query hieronder

SELECT c.name circuit, country, r.name grandprix, surname
FROM driver_standing ds
JOIN races r
ON r.raceId = ds.raceId
JOIN drivers d
ON d.driverId = ds.driverId
JOIN circuits c
ON r.circuitId = c.circuitId
WHERE year = 1950
AND surname LIKE 'f%'
   
