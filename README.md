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


----------------------------------------------------------------------
I have following tables

routes

id | route_name

stops

id | stop_name

stop_orders

id | route_id | stop_id | stop_order

here i will store all stops name

buses

id | bus_name

1 | R.S

here i will store all bus names

3.route_connect

id | bus_id | stop_id

1 | 1 | 1

2 | 1 | 2

bus_timing

id | route_id | stop_id | bus_id | bus_timing | trip | trip_direction

bus_name|stop_name

R.S |Sydney
R.S | Melbourne

----------------------------------------------------------------------

1) My aim is to get all bus names when user will search between two stops.

2) For example if user search for source to destination (Sydney to Melborne) then it should return all bus names which is traveling between these two city. If there is no direct buses then i need to show connected buses between two city

I am trying write a query where i need to retrieve all buses between two stop and between two timings

i tried lots of combination of query but it failed to retrive the expected result

1) I need to retrieve all buses which travel between two city along with between two times.

2) Also if buses are not directly travel between two city then i need to show inter connected buses.

1)routes will contain different routes like sydney,melborne.

2)stops will contain same as routes

3)stop_order table contain each route as multiple stops with the order so we can know which is then next stop based on order

4)each bus has timing which will be mentioned in bus timing table with route and stop 5)one bus will travel multiple times between two city so i added trip and direction will identify which way bus is traveling i mean sydney to melborne or melborne to sydney



![city_route](https://github.com/codeforfungit/bustiming/blob/master/city_route.jpg)
Image explanation

1)In image city refers to routes table

2)green color shows multiple stops in city

3)city 1 and city 2 will connect in city 3 so if a person wants to go city-1 to city-2 then he need to use interconnected buses between city-1 to city-3 and city-3 to city-2
