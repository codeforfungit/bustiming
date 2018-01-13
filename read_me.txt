MY entire Project Description

we have multiple city (in table i refered as route) 
and each city as bus stops 
and each city has many buses 
and every bus will travel many times in day between source to destination
(To identify every bus trip i have added column in bus_timing tables as trip and direction 
,Here direction will be 1 and 2 , 1 will be source to destination and 2 will be destination to source)
----------------------------------------------------------------------

My Project Aim

1)When user search between source to destination with between two time then it should return all buses travel between two city

2)Gordon Linoff already answered but that will return only one record .his answer will fail if we select long time i mean 1 clock to 12 clock
then there might be chances of same will have multiple trips then it should return all trips 
----------------------------------------------------------------------

when user search between stop_8 and stop_18  and between 1 clock to 12 clock then it should return all buses with time 