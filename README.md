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

