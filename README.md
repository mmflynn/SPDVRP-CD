# SPDVRP-CD
Test instances for the Split Pick-up and Delivery Vehicle Routing Problem with Cross-Docks

This repro contains the data for the instances considered in our Thesis paper.

Each the filenames shows the structure of the instance with  the following encoding
S=a_D=b_X=c(d)_e.csv,

Where,
a is the number of supplier vertices
b is the number of delivery vertices
c is the number of cross-dock vertices
d is the number of cross-dock vertices that can receive a delivery (these are additional to those in c)
e is the number of orders.

Each file is stuctured in 5 blocks with the first 3 being location definitions all having a common format
Site (i.e. Cross-dock), Suppler, and Destination
Identifier, X coordinate, Y coordinate, vertex number

The fourth group defines the orders in the format
Source, destination, volume, earliest collection time, latest delivery time, count

The final block defines a basic set of routes that allows a feasible solution.  The format of these routes is
Route Id, python list of vertices visited.

A support file in the format S=a_D=b_X=c(d)_e.0150%.1w.csv, has a modified version of the orders in S=a_D=b_X=c(d)_e.csv with tighter time windows.
