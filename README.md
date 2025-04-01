Maintenance Log Analysis
Overview
This project provides a solution for analyzing equipment maintenance costs over time. It allows users to efficiently query the total maintenance costs for specific date ranges based on a log of maintenance records. The implementation utilizes a Fenwick Tree (Binary Indexed Tree) to ensure efficient updates and queries.

Features
Efficient Querying: Quickly retrieve total maintenance costs for specified date ranges.
Dynamic Updates: Easily add new maintenance records and update costs.
Date Handling: Automatically maps dates to indices for efficient processing.

Requirements
Python 3.x

Installation
Clone the repository:
git clone https://github.com/yourusername/maintenance-log-analysis.git
cd maintenance-log-analysis

Ensure you have Python installed on your machine.

Usage
Input Format
Maintenance Logs: A list of tuples, where each tuple contains:

equipment_id: An identifier for the equipment.
date: A string representing the date of maintenance in the format "YYYY-MM-DD".
cost: An integer representing the cost of maintenance.
Queries: A list of tuples, where each tuple contains:

start_date: A string representing the start date of the query range.
end_date: A string representing the end date of the query range.

Example:
maintenance_logs = [
    (101, "2024-01-01", 500),
    (102, "2024-01-10", 300),
    (101, "2024-01-15", 700)
]

queries = [
    ("2024-01-01", "2024-01-10"),
    ("2024-01-01", "2024-01-15")
]

result = maintenance_cost_analysis(maintenance_logs, queries)
print(result)  # Output: [800, 1500]

Function Description
maintenance_cost_analysis(maintenance_logs, queries):
Parameters:
maintenance_logs: List of maintenance records.
queries: List of date range queries.
Returns: A list of total maintenance costs for each query.

Implementation Details
The solution uses a Fenwick Tree (Binary Indexed Tree) to efficiently manage cumulative sums of maintenance costs.
Dates are mapped to indices to facilitate quick access and updates.
The implementation is designed to handle a large number of records and queries efficiently.
