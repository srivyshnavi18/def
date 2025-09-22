# def
•  You made changes to one file in the above project but haven't staged them yet. You realize they were a mistake. What Git command will you use to discard the local changes?
•	Command: git checkout -- <file-name> or git restore <file-name>
•  You made a commit but typed the wrong commit message. You haven't pushed it yet. How do you fix it?
•	Command: git commit --amend -m "your new message"
•  You want to view the commit history of the current branch in a readable format. What Git command should you use?
•	Command: git log --oneline or git log --oneline --graph
•  You're on the main branch. Create the branch Featuer/patient and switch to that branch. What commands do you use?
•	Command: git checkout -b Featuer/patient
•  You've made some commits locally and now want to upload them to the remote repository. What do you run?
•	Command: git push
•  You want to see all the branches that exist both locally and on the remote. How?
•	Command: git branch -a
•  Create a branch Suggestions and merge with patient branch, how can it be?
•	Commands:
1.	git checkout patient (to move to the patient branch)
2.	git merge Suggestions (to merge the Suggestions branch into patient)
•  How do you pull the latest changes from the remote repository and merge them into your local branch?
•	Command: git pull or git pull origin <branch-name>
•  Specify the git command when pushing for the first time and want to set the remote branch.
•	Command: git push -u origin <branch-name> or git push --set-upstream origin <branch-name>
•  You cloned a remote repository, but later you find that you need to push your changes to a different remote repository. How do you configure your local repository to push to this new remote?
•	Command: git remote set-url origin <new-remote-url>
•  After running git pull, you notice that your local branch is behind the remote branch. How would you proceed to bring your local branch up to date without losing your local changes?
•	Command: git pull (This is the correct command; Git is designed to merge changes automatically without losing your local work.)
•  You've pushed a patient branch to a remote repository, but now you need to delete the branch from the remote. How would you do that?
•	Command: git push origin --delete patient
•  How do you apply a .patch file provided by your teammate and include it in your commit history?
•	Commands:
1.	git apply <patch-file-name.patch>
2.	git add .
3.	git commit -m "Applied patch from teammate"




























1. Abstract: System Overview
This project designs an online platform for grocery delivery, similar to BigBasket. The system lets customers shop, pay, and track orders. It also provides tools for store managers to handle inventory and for delivery agents to fulfill orders.

2. Functional Requirements
These are the core actions the system must perform:

User Management: Customers, managers, and agents can securely sign up and log in.

Shopping: Customers can browse items, add them to a cart, and place an order.

Payments: The system will process payments securely.

Order Tracking: Customers can follow their order's journey from store to delivery.

Inventory & Order Handling: Managers can update stock and assign orders to delivery agents.

Delivery Management: Agents can view their assigned orders and update their delivery status.

3. Non-Functional Requirements
These requirements define how well the system performs:

Performance & Reliability: The system must be fast, reliable, and available 24/7.

Security: All user and payment data must be protected.

Usability: The platform must be easy to use for all three types of users.

Scalability: The system should be able to handle growth in users and orders.

4. Users of the System
The system has three primary users:

Customers: People who buy groceries online.

Store Managers: Staff who manage products and prepare orders.

Delivery Agents: People who deliver the orders to the customer's location.
