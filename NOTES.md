\# Patch Exercise Notes



\## Summary of Changes



1\. Fixed the task search SQL in TaskRepository.java by grouping the title/description conditions. This ensures the archived and status filters apply correctly to both searchable fields.

2\. Removed the artificial query delay and unnecessary complexity calculation from TaskController.java.

3\. Updated App.jsx so changing the search query or status filter resets pagination to page 1.

4\. Updated useTasks.js to clear the previous error when a new task request starts.



\## What I Chose Not to Change



I did not make broad refactors or change unrelated configuration warnings because they were outside the highest-value bugs for this focused exercise. I also avoided dependency upgrades and npm audit fix --force to prevent unnecessary changes.



\## Biggest Remaining Risk



The backend uses an in-memory H2 database, so task data is reset when the application restarts. There are also no automated backend tests covering the search, status filtering, and pagination behavior.



\## Tools / AI Used



I used ChatGPT to help review the code, identify the SQL operator-precedence issue, reason about the frontend pagination/error-state behavior, and review the focused changes. I then applied the changes locally, ran the Spring Boot backend and Vite frontend, and manually tested search, status filtering, and pagination.

