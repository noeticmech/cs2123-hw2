

# Instructions

Write a program that solves the following problems. The solution to each will be based on one of the algorithms we've covered in class. Your program should take a single command line argument that specifies an input file, and produce a text file containing the solutions to each problem separated by lines containing `"---"` and named `solutions_<input_file_name>.txt`. The input file will consist of five lines corresponding to these five problems in order. Each line will contain the name of a file containing a graph to work on, optionally followed by a comma and any additional parameters for that problem. A basic test is included in the `./tests/` directory. You can verify your output by running a "diff" on your `solutions_test_0.txt` and `./tests/solutions_0.txt`.


## Example

Given a file `tests/test_0.txt` with the following contents:

    turtle_0.csv, 2
    maze_0.csv
    construction_0.csv
    adventure_0.csv, quest_8
    hybras_0.csv

&#x2026;your program should produce a file `solutions_test_0.txt` with the following contents:

    ---
    living room, office
    kitchen, laundry room, mudroom
    ---
    Start, 1, 4, 6, 9, Exit
    ---
    Store, Coffee, Friend
    ---
    quest_1, quest_2, quest_3, quest_6
    quest_1, quest_2, quest_4, quest_5, quest_6
    quest_1, quest_2, quest_4, quest_5, quest_7
    quest_1, quest_2, quest_4, quest_7
    ---
    6, Poëlitetz, Vervold, Twitten's Cross, Bulmer Skeme, Arquensio, Domreis
    ---


# Not All Who Wander Are Lost&#x2026;

During a moment of inattentiveness, your pet turtle has wandered off. He couldn't have gotten too far. Given an elapsed time *T*, and a graph that represents the environment with spaces as nodes and the connections between these spaces as edges, compute an ordering for searching the surroundings that are reachable within the elapsed time. Assume that your turtle can move from one space to another in 1 time-unit and that you can easily search the surroundings before he has a chance to move again. The node that represents the space you last saw your turtle has been labeled "Last Seen".

Your output should consist of *T* lines, with each line *t* containing the (comma separated) locations your turtle could reach in *t* time-units. Turtles get distracted too, sometimes.

    living room, office
    kitchen, laundry room, mudroom


# &#x2026;But You Are.

You are lost in a maze and have a dreadful feeling you need to get out of here as fast as possible. Given a graph that represents each intersection in the maze as a node and the passages in-between them as edges, compute a list of intersections through which you will pass on your way to the exit *without exploring more of the maze than necessary*. Assume that the intersection you begin at is labeled "Start" and the intersection that leads out of the maze is labeled "Exit".

Your output should be a single line containing the labels of the nodes on your path, including "Start" and "Exit"

    Start, 1, 4, 6, 9, Exit


# Under Construction

The City of Tulsa is currently pursuing construction along several of the city's key thoroughfares. While no part of the city is *technically* disconnected from other parts of the city, for a few hours each day, travel times along some routes in certain directions has become "practically infinite". Given a graph that represents the city with nodes as locations and edges as routes between them, determine which of the following locations are reachable from the "Work" location during these times: "Home", "Store", "Library", "Coffee", and "Friend".

    Store, Coffee, Friend


# Choose Your Own Adventure

You are organizing the writing for a story-driven adventure game. One of your writers wants to be able to know which story beats the player character may have reached before any given story beat. Given the label *S* of a story beat and a graph in which story beats are represented by nodes and the actions leading to the next story beat are represented by edges, list all sets of story beats that can precede the given story beat.

Your output should consist of a number of lines, each line containing the sorted labels of a particular set of potentially experienced story beats (that is, not in story order, but alphabetical order). Do not include the target story beat in these lists.

*Note: Doing this properly is a little involved. Make sure you have something that works for straightforward cases before worrying about the less straightforward ones.*

    quest_1, quest_2, quest_3, quest_6
    quest_1, quest_2, quest_4, quest_5, quest_6
    quest_1, quest_2, quest_4, quest_5, quest_7
    quest_1, quest_2, quest_4, quest_7


# Conditional Inheritance

You have escaped bondage to the Ska along with Aillas, prince of Troicinet, who has promised you lands and knighthood if your company can make it from the Ska stronghold of Poëlitetz in North Ulfland to the palace in Domreis on the other side of Hybras before his cousin is crowned king in his stead. He reckons you have about two weeks. As an island nation, there are many paths to Troicinet both by land and sea. Given a graph that represents these paths as edges weighted with the estimated travel time in days (assuming that your party is not substantially delayed by Skalings, pirates, malicious fae halflings, or agents of King Casmir of Lyonesse), find the shortest path from the node labeled "Poëlitetz" to the node labeled "Domreis". Your output should be the number of days followed by the locations (node labels) along your path.

    6, Poëlitetz, Vervold, Twitten's Cross, Bulmer Skeme, Arquensio, Domreis

