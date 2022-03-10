# Santa_Project
Code of an exercise to develop an algorithm which aims to optimise the delivery of 100,000 gifts across the globe by Santa. The generated algorithm is required to produce an itinerary for delivery which reduces reindeer weariness. 

Terminology
Gift - An individual gift which has a gift ID, delivery location and weight
Gift Trip - A trip consists of one set of deliveries of gifts, starting at the north pole and ending at the north pole. A trip can have a weight limit up to 1000
Journey - A journey is the process of delivering all gifts and can consist of x number of trips. The algorithms are required to produce an itinerary for a journey
WRW score - Weighted Reindeer Weirdness (WRW) is calculated using the objective function provided in Appendix A.4. It is the WRW which the developed algorithm is required to optimise
Evaluation -The number of iterations that an algorithm performs on a given journey or trip to develop an optimal itinerary. After x number of evaluations, 1 WRW score will be output as the best found score
Repeat - A repeat is the number of times that an algorithm is run. x repeats will produce x WRW scores
Distance - The haversine distance between two locations on the globe

The code combines Simulated Annealing with two neighbourhood moves.

Neighbourhood Move 2 (NM2) = moves a randomly chosen gift within a randomly selected trip to another random position within the same trip
Neighbourhood Move 6 (NM6) = selects three random trips, splits them at a random point, and merges them again to create three new trips
