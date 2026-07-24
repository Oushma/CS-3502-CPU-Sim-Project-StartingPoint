# CPU Scheduling Simulator

A Windows Forms application that demonstrates CPU scheduling algorithms through an interactive graphical interface. Each algorithm displays detailed execution results and performance metrics including Average Waiting Time (AWT), Average Turnaround Time (ATT), CPU Utilization, and Throughput.

Original creator: Francis (used with permission)

## Project Status

The simulator is fully functional with **six scheduling algorithms** implemented:

| Algorithm | Method | Notes |
|-----------|--------|-------|
| First Come First Serve | `RunFCFSAlgorithm` | Processes executed in order of arrival |
| Shortest Job First | `RunSJFAlgorithm` | Processes sorted by burst time |
| Priority Scheduling | `RunPriorityAlgorithm` | User-supplied priority values (higher = higher priority) |
| Round Robin | `RunRoundRobinAlgorithm` | Time quantum parameter required |
| SRTF (Shortest Remaining Time First) | `RunSRTFAlgorithm` | Preemptive SJF, executes shortest remaining burst time |
| HRRN (Highest Response Ratio Next) | `RunHRRNAlgorithm` | Non-preemptive with aging to prevent starvation |

## Performance Metrics

The simulator calculates and displays the following metrics for each algorithm:

- **Average Waiting Time (AWT)** - Sum of waiting times / number of processes
- **Average Turnaround Time (ATT)** - Sum of turnaround times / number of processes
- **CPU Utilization (%)** - (Total burst time / Total time) × 100
- **Throughput** - Number of processes / Total time

## Requirements

- Windows operating system
- .NET 8.0 SDK or newer
- Visual Studio 2022 or VS Code with C# extensions

## How to Run

### Using Visual Studio

1. Clone the repository:
   ```bash
   git clone https://github.com/Oushma/CS-3502-CPU-Sim-Project-StartingPoint.git
   ```
2. Open CpuScheduler.sln in Visual Studio 2022

3. Press F5 to build and run the application

### Using VS Code

1. Clone the repository:
git clone https://github.com/yourusername/CS-3502-CPU-Sim-Project-StartingPoint.git

2. Install the C# Dev Kit extension in VS Code

3. Open the project folder in VS Code

4. Press F5 or go to Run & Debug panel

### Using .NET CLI
From the project root directory:
```bash
dotnet build
dotnet run --project CpuScheduler/CpuScheduler.csproj
```

## Usage
Usage
1. Enter the desired number of processes 
2. Choose a scheduling algorithm from the interface
3. The app will prompt for additional values as needed (burst time, priority, quantum time, etc.)
4. View the results in the display table showing waiting times and turnaround times

### New Algorithms Added
## SRTF (Shortest Remaining Time First)
- Preemptive version of SJF

- Always executes the process with the shortest remaining burst time

- New arrivals with shorter burst times preempt the current process

- Optimal for minimizing average waiting time

- Calculates response time for accurate performance analysis

## HRRN (Highest Response Ratio Next)
- Non-preemptive algorithm

- Calculates response ratio: (Waiting Time + Burst Time) / Burst Time

- Process with highest ratio executes next

- Prevents starvation through aging (waiting time increases ratio)

- Balances fairness and efficiency

### License

This project is licensed under the terms of the [MIT license](LICENSE.txt)
