# Secure Console-Based Voting System in C

A simple yet secure voting system developed in C for academic or small-scale election purposes. This console application ensures authorized voting using unique student IDs and restricts duplicate votes. Handlers can manage candidates and monitor poll results through password-protected access.

## Features

- **Voter Authentication**  
  Each voter must enter a valid and unused student ID from the `voters.txt` file.

- **Handler Access**  
  Handlers authenticate via a password to manage candidate information or view polls.

- **Candidate Management**  
  Handlers can add or modify candidates. Each modification resets the vote counts.

- **Poll Results Viewing**  
  Handlers can view current standings from the `polls.txt` file.

- **File-Based Data Management**  
  Utilizes plain text files for easy portability:
  - `voters.txt` – list of authorized voters
  - `candidate.txt` – list of candidates
  - `polls.txt` – vote count for each candidate

## File Structure

├── main.c ├── voters.txt ├── candidate.txt ├── polls.txt


## How It Works

1. **Program Start**:  
   Choose between `Handler` or `Voter` access.

2. **Voter Flow**:
   - Enter student ID.
   - If valid and not previously used, proceed to vote.
   - Vote is recorded and voter marked as "voted".

3. **Handler Flow**:
   - Enter password (`xyz123` by default).
   - Choose to:
     - Change candidate info (resets polls)
     - View current poll results
     - Return to home

## Setup & Run

### Compile the program

```bash
gcc main.c -o voting_system
