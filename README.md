# Santa_Project
Code of an exercise to develop an algorithm which aims to optimise the delivery of 100,000 gifts across the globe by Santa. The generated algorithm is required to produce an itinerary for delivery which reduces reindeer weariness. 

Terminology
1. Gift - An individual gift which has a gift ID, delivery location and weight
2. Gift Trip - A trip consists of one set of deliveries of gifts, starting at the north pole and ending at the north pole. A trip can have a weight limit up to 1000
3. Journey - A journey is the process of delivering all gifts and can consist of x number of trips. The algorithms are required to produce an itinerary for a journey
4. WRW score - Weighted Reindeer Weirdness (WRW) is calculated using the objective function provided in Appendix A.4. It is the WRW which the developed algorithm is required to optimise
5. Evaluation -The number of iterations that an algorithm performs on a given journey or trip to develop an optimal itinerary. After x number of evaluations, 1 WRW score will be output as the best found score
6. Repeat - A repeat is the number of times that an algorithm is run. x repeats will produce x WRW scores
7. Distance - The haversine distance between two locations on the globe

The code combines Simulated Annealing with two neighbourhood moves. To combine the two, multiple methods were explored:
1. a 50% chance of either running
2. a bias towards one of the NMs
3. an evaluation bias where an NM would only be considered for a certain number of evaluations
4. a temperature moving bias where the chance of implementing NM6 became lower as tempterature dropped


Neighbourhood Move 2 (NM2) = moves a randomly chosen gift within a randomly selected trip to another random position within the same trip
Neighbourhood Move 6 (NM6) = selects three random trips, splits them at a random point, and merges them again to create three new trips
