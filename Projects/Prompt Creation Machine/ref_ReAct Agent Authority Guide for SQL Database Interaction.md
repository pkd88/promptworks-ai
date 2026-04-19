ReAct Agent Authority Guide for SQL Database Interaction
1. The ReAct Architecture
The ReAct (Reason-Act) pattern turns a static language model into an active agent. Instead of jumping to an answer, the agent follows a rigid "Thought-Action-Observation" loop.
Why Use ReAct for SQL?
Standard AI models often guess database schemas. ReAct agents are "grounded." Grounded agents never assume a table exists; they check the database metadata first. This prevents "No such column" errors that plague simpler systems.


2. The Universal Prompt Template
To make an agent follow this guide, you must provide a System Prompt. This prompt defines the boundaries of the agent's "brain."

System Instructions: "You are a SQL Expert Agent. You have access to a database. You must answer questions by following this format:

Question: The user's input. Thought: Describe your reasoning and which tool you need next. Action: The name of the tool (list_tables, get_schema, execute_query). Action Input: The specific input for that tool. Observation: The raw data returned by the tool. ... (Repeat Thought/Action/Observation if needed) Final Answer: The human-readable result based on the data."


3. The Toolset (The Agent's Hands)
A ReAct agent is only as good as its tools. Below are the four essential tools for any SQL Agent.

Tool Name
Purpose
Example Input
sql_db_list_tables
Shows all tables in the DB.
"" (Empty String)
sql_db_schema
Shows columns for a table.
"Sales_2025"
sql_db_query_checker
Checks SQL for common errors.
"SELECT * FROM Users"
sql_db_execute
Runs the query and gets data.
"SELECT count(*) FROM Orders"


4. Full ReAct Trace: 2025 Sales Analysis
This is a full execution example. In this scenario, Phil asks: "What was the total revenue from the 'Outdoor' category in Q1 of 2025?"

Question: What was the total revenue from the 'Outdoor' category in Q1 of 2025?

Thought: I need to find which tables contain sales and category information. I will start by listing all tables. Action: sql_db_list_tables Action Input: "" Observation: Customers, Products, Orders, Order_Details, Categories

Thought: The 'Orders', 'Order_Details', and 'Categories' tables seem relevant. I need to see the schema for these tables to find the revenue and date columns. Action: sql_db_schema Action Input: "Orders, Order_Details, Categories" Observation: - Table 'Orders': columns [OrderID, CustomerID, OrderDate, TotalAmount]

Table 'Order_Details': columns [DetailID, OrderID, ProductID, Quantity, UnitPrice]
Table 'Categories': columns [CategoryID, CategoryName]

Thought: I can calculate revenue using the 'TotalAmount' from the 'Orders' table. I need to join 'Orders' with 'Order_Details' and 'Categories' to filter by 'Outdoor'. I will write a query to sum the TotalAmount for 2025-01-01 through 2025-03-31 where CategoryName is 'Outdoor'. Action: sql_db_query_checker Action Input: "SELECT SUM(o.TotalAmount) FROM Orders o JOIN Categories c ON o.CategoryID = c.CategoryID WHERE c.CategoryName = 'Outdoor' AND o.OrderDate BETWEEN '2025-01-01' AND '2025-03-31'" Observation: The query is syntactically correct and safe.

Thought: The query is verified. I will now execute it to get the final total. Action: sql_db_execute Action Input: "SELECT SUM(o.TotalAmount) FROM Orders o JOIN Categories c ON o.CategoryID = c.CategoryID WHERE c.CategoryName = 'Outdoor' AND o.OrderDate BETWEEN '2025-01-01' AND '2025-03-31'" Observation: [(45200.50,)]

Thought: I have the data. The total revenue for the Outdoor category in Q1 2025 was 45,200.50. Final Answer: The total revenue for the Outdoor category during the first quarter of 2025 was $45,200.50.


5. Advanced Logic: Error Recovery
If the 'Observation' returns an error (e.g., "Column 'TotalAmount' does not exist"), a ReAct agent does not stop.

New Thought: "The database says TotalAmount is missing. I must have looked at the wrong table."
New Action: sql_db_schema
New Action Input: "Order_Details"
New Observation: columns [Quantity, UnitPrice]
Revised Logic: The agent now realizes it must multiply Quantity by UnitPrice instead of using a single TotalAmount column.


6. Safety and Security Constraints
To prevent accidental data loss or security breaches, ReAct agents must follow these rules:

Read-Only Access: Use a database user that only has SELECT permissions.
Limit Rows: Always append "LIMIT 10" or "TOP 10" to exploratory queries to prevent memory crashes.
No DML: Explicitly forbid the agent from using INSERT, UPDATE, DELETE, or DROP commands.
Human-in-the-Loop: For high-stakes databases, the agent should output the "Thought" and "Action" and wait for a human to type "Approve" before the Action is executed.
