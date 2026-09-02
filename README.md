# cs3113fa21-project1

**Author:** Nima Shadaram

## How I Ran the Project

1. Use the command `make all` in the terminal. This compiles the program and gets it ready to run.
2. To run the program, use the name of the executable file (`project1`), followed by the name of the input text file (e.g. `input.txt`).
3. I created a condition where if no file was passed in from the terminal, the program would read from `stdin` instead, so input could still be provided.
4. Lastly, use the command `make clean` to remove any executable files created during the build process.

## Bugs I Expected

Some of the bugs I expected involved figuring out how to get the proper location of the integers I needed in the array. Another was getting the correct math for each calculation — on some timings, I struggled to understand the underlying math and how to calculate them properly.

Several of these expected issues did come up while working on the program. The main one was getting the proper inputs into the array and storing the burst integers into their own array, since this determined the rest of the calculations. I also had trouble reading the file in correctly, and my non-voluntary context switches were sometimes off.

A bigger problem I hadn't anticipated was that many of my variables held garbage values because they were never initialized to 0. A lot of my assumptions about this project involved understanding how to store my variables, but due to my limited experience in C, implementing that correctly took a lot of trial and error.

## People Who Helped Me Understand the Timings

- Jonathan Leslie
- Anthony Immensuch

## Function Descriptions

**`main`**
Determines whether input will be read from an open file or from `stdin`. Two structs are created to store the variables and are initialized to avoid garbage values. These variables are then stored in an `arraystore` array, which is used to calculate their necessary positions. After assigning the base values, they are placed into their positions, and the main calculation function is called.

**`getinfotimes`**
Uses a series of while loops and process counters to determine which positions get updated and where increments occur. This is also where variables like response time are calculated, keeping all calculations in one place rather than spread across the program. These totals are then divided by `numPIDs` to get the average times.

**Context switch calculation**
A separate method calculates the number of context switches using a for loop over the process IDs.

## Sources

- [FCFS Scheduling — Guru99](https://www.guru99.com/fcfs-scheduling.html)
- [Throughput vs Turnaround Time vs Waiting Time vs Response Time — 8bitavenue](https://www.8bitavenue.com/throughput-vs-turnaround-time-vs-waiting-time-vs-response-time/)
- [First Come First Serve — StudyTonight](https://www.studytonight.com/operating-system/first-come-first-serve)
