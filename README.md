### Road-trip!
### A* Search


initial state:- Initial start city
state space:- all the cities and junctions are part of state space 
Successor function:- all the connected cities for the current state
goal state:- current nodes as end city

Heuristic:
    distance:
        Haversine distance between the nodes. edge cost as distance between nodes given in road-segment.txt
    Time:
        Haversne distance/max speed limit .Max speed limt of all states because it make the heuristic admissible. it never over estimates the heuristic value of time. edge cost as the length of the connecting road/speed limit of the connecting route.
    Safe:
        edge cost id the length of the connecting road multipled by the accident probability of the road. heuristic is 0 as it never overestimates
    segment:
        Heuristic is the haversine distance/max segement length of  all roads so heuristic never over estimates. edge weight is is 1.

Procedure:
    keep the initial state into the fringe. 
        check for goal state. if goal display
        take min from fringe calculates cost by edge weight+heuristic values and append them to fringe
        we are not visiting the already visited states if their cost is greater than exixting cost of that state. (optimised the code to great level)
    

heuristic for the junction nodes is taken as 0
