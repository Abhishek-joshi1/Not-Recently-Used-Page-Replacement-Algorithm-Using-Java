This repository contains a Java implementation of the Not Recently Used (NRU) page replacement algorithm. The code simulates the NRU algorithm to manage page requests within a given number of frames, tracking page faults and hits. Below is a detailed explanation of the code structure and its functionality.

Code Structure and Functionality
Class: NRUPageReplacement
Fields
numFrames: The number of frames available in memory.
frameList: A list that stores the pages currently loaded into the frames.
usageList: A list that tracks the usage status of the pages in the frames (used for determining the replacement strategy).
Constructor
NRUPageReplacement(int numFrames): Initializes the numFrames, frameList, and usageList.
Methods
findPageToReplace(int NumPages, int[] pageRequests)

Purpose: Simulates the NRU page replacement process.
Parameters:
NumPages: Total number of page requests.
pageRequests: An array of page requests.
Functionality:
Iterates through each page request.
Checks if the page is already in the frames (page hit) and updates its usage status.
If the page is not in the frames (page fault), it adds the page to the frames or replaces the least recently used page if the frames are full.
Tracks and prints the memory state at each step.
Calculates and prints the page faults, page hits, and their respective ratios at the end of the simulation.
getLowestUsagePageIndex()

Purpose: Finds the index of the page with the lowest usage status (for replacement purposes).
Returns: The index of the page to be replaced.
getMemoryState()

Purpose: Generates a string representation of the current state of the memory (frames).
Returns: A string showing the pages in the frames along with their usage status.
Main Method
main(String[] args)
Purpose: Entry point for the program execution.
Functionality:
Prompts the user to input the number of pages and page requests.
Prompts the user to input the number of frames.
Initializes an instance of NRUPageReplacement with the specified number of frames.
Executes the NRU page replacement simulation and displays the results.
