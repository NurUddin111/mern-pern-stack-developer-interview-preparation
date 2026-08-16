# Docker — Core Interview Questions

## Q01. What is Docker, and what problem does it solve?

## Q02. Why would you use Docker in a web application project?

## Q03. What is the difference between Docker and a Virtual Machine?

## Q04. What is a Docker Image?

## Q05. What is a Docker Container?

## Q06. What is the relationship between a Docker Image and a Docker Container?

## Q07. Why is Docker useful for solving the "it works on my machine" problem?

## Q08. What does containerization mean?

## Q09. What are the main benefits of using Docker?

## Q10. Can you run multiple containers on the same machine? If yes, how can they be different from each other?

## Q11. Suppose you have a Node.js application that works perfectly on your computer. Why might it fail when another developer runs it on their computer, and how can Docker help?

## Q12. If you delete a Docker container, does the Docker Image also get deleted? Why or why not?

## Q13. Can you create multiple containers from the same Docker Image? Why would you want to do that?

## Q14. Does a Docker container contain a complete operating system like a Virtual Machine? Explain.

## Q15. Imagine you have a Node.js backend, PostgreSQL database, and Redis server. Why might Docker be useful for running this application locally?

# Docker — Image & Container Interview Questions

## Level 1 — Fundamentals

## Q16. What is a Docker Image?

## Q17. What is a Docker Container?

## Q18. What is the difference between a Docker Image and a Docker Container?

## Q19. How do you create a Docker Container from an Image?

## Q20. Can multiple Containers be created from the same Image? Why would you do that?

## Level 2 — Understanding

## Q21. Is a Docker Image writable or read-only? What happens when a Container modifies files2?

## Q22. What happens to a Container when you stop it?

## Q23. What happens to a Container when you remove/delete it?

## Q24. If you delete a Container, does the Image also get deleted? Why?

## Q25. Can you modify a running Container? If yes, what happens to those changes?

## Level 3 — Dockerfile & Images

## Q26. What is a Dockerfile, and how is it related to a Docker Image?

## Q27. What is a base Image? Give an example.

## Q28. Why would you use FROM node:22 in a Dockerfile?

## Q29. What happens when you run docker build?

## Q30. What happens when you run docker run?

## Level 4 — Practical / Scenario Questions

## Q31. You have a Node.js + Express application. How would you create a Docker Image for it?

## Q32. You have one Docker Image for your Node.js application. Can you run three instances of your backend from that same Image? How?

## Q33. Your application works on your machine but doesn't work on another developer's machine. How can Docker help solve this problem?

## Q34. Your Container crashes. Does the Docker Image become unusable? Explain.

## Q35.Suppose you have Finvia with a Next.js frontend and Node.js backend. Would you put both applications inside one Docker Image or use separate Images? Why?
