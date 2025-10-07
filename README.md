Batch Payroll Application
📝 Overview
This document describes the use cases for the Batch Payroll Application. This system automates the process of calculating, generating, and distributing payroll for employees, incorporating necessary inputs like timecards and sales receipts, and handling deductions like union dues.

👥 Actors
The primary users (actors) interacting with the system are:

Payroll Admin: The administrative user responsible for initiating payroll runs and submitting initial data.

Employee: The system user whose payroll is being processed. They submit time-related documents.

Union: An external entity that interacts with the system to manage related service charges.

🛠️ Key Use Cases (Functionality)
This section lists the main functions the system performs, categorized by the initiating actor.

Payroll Admin Functions
Use Case	Description
Run Payroll	Initiates the entire payroll calculation and generation process.
Submit Sales Receipt	Enters supplementary sales data needed for commission or specific earnings calculation.
Choose Payment Method	Configures whether employees are paid via check, direct deposit, etc.

Employee Functions
Use Case	Description
Submit Timecard	Enters the hours worked data, which is crucial for gross pay calculation.


Union Functions
Use Case	Description
Add Service Charges	Registers specific charges or fees related to union membership into the payroll system.

⚙️ Process Flow: Payroll Calculation
The central sequence of operations for generating a paycheck is as follows. These use cases are typically executed automatically upon a Run Payroll request.

Calculate Payroll: Determines the gross pay based on submitted timecards and sales receipts.

Deduct Union Dues: Subtracts mandatory union fees from the gross pay. This step must follow Calculate Payroll.

Generate Paycheck: Produces the final payment (check or deposit record) with net pay after all calculations and deductions are complete. This step must follow Deduct Union Dues.
