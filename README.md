# GitHub for Embedded Application Development

## 1. Version Control of Embedded Applications Using GitHub

### Aim
To understand how GitHub is used to maintain different versions of an embedded application and manage source code during Raspberry Pi project development.

### Introduction
GitHub is a cloud-based platform used to store, manage and share source code. It uses Git, a version control system that tracks changes made to project files.

In Raspberry Pi embedded application development, GitHub helps developers maintain different versions of C++ programs, correct errors and collaborate with other developers.

### Importance of GitHub Features

**1. Commit History**

- Commit history records all changes made to the project.
- Each commit contains a description of the changes.
- Developers can check previous versions of the program.
- It helps identify and correct errors.

Example:
```bash
git add main.cpp
git commit -m "Added LED control program"
```

**2. Branches**

- A branch is a separate working copy of the project.
- Developers can test new features without affecting the main program.
- It helps develop multiple features independently.

Example:
```bash
git branch sensor-control
git checkout sensor-control
```

**3. Merging**

- Merging combines changes from one branch into another.
- After testing a new feature, it can be merged into the main branch.
- It helps combine the work of multiple developers.

Example:
```bash
git checkout main
git merge sensor-control
```

### Example: Raspberry Pi Project

Consider a Raspberry Pi-based automatic temperature monitoring system.

- Version 1: Read temperature using a sensor.
- Version 2: Display temperature on an LCD.
- Version 3: Add an alarm when temperature exceeds the limit.

Each version can be saved using Git commits. New features can be developed using branches and merged into the main project after testing.

### Advantages

1. Maintains different versions of source code.
2. Tracks changes made by developers.
3. Allows easy error correction.
4. Supports teamwork and collaboration.
5. Prevents accidental loss of previous code.

### Result
Thus, GitHub helps maintain different versions of embedded applications using commit history, branches and merging during Raspberry Pi project development.

---

## 2. Complete Workflow for Managing a Raspberry Pi Embedded C++ Project Using GitHub

### Aim
To understand the complete workflow of managing a Raspberry Pi embedded C++ project using GitHub.

### Introduction
GitHub provides a platform to store and manage embedded C++ source code. Developers can download an existing repository, modify source files, save changes and synchronize them with the remote repository.

### Steps Involved

**Step 1: Create a GitHub Repository**

1. Open https://github.com.
2. Log in to your GitHub account.
3. Click the New Repository option.
4. Enter the repository name.
5. Select Public or Private.
6. Click Create Repository.

Example repository name: `raspberry-pi-project`

**Step 2: Clone the Repository**

Cloning means downloading a copy of the remote repository to the local computer or Raspberry Pi.

Command:
```bash
git clone https://github.com/username/raspberry-pi-project.git
```

Move into the project folder:

```bash
cd raspberry-pi-project
```

**Step 3: Create and Modify Source Files**

Create a C++ file named `main.cpp`.

Example program:

```cpp
#include <iostream>
using namespace std;

int main()
{
    cout << "Raspberry Pi Embedded Project" << endl;
    cout << "GitHub Version Control" << endl;

    return 0;
}
```

Save the file after making the required modifications.

**Step 4: Check File Changes**

Use the following command to check modified files:

```bash
git status
```

This command displays the current status of the repository.

**Step 5: Add Source Files**

Add the modified files to the staging area.

```bash
git add main.cpp
```

To add all modified files:

```bash
git add .
```

**Step 6: Commit Changes**

Commit saves the changes in the local Git repository with a meaningful message.

```bash
git commit -m "Added Raspberry Pi C++ program"
```

**Step 7: Synchronize with Remote Repository**

Push uploads the committed changes to GitHub.

```bash
git push origin main
```

To download the latest changes from GitHub:

```bash
git pull origin main
```

### Complete Workflow

```text
Create GitHub Repository
          |
          v
    Clone Repository
          |
          v
    Modify C++ Files
          |
          v
     Check Status
          |
          v
       Add Files
          |
          v
      Commit Changes
          |
          v
      Push to GitHub
          |
          v
   Remote Repository Updated
```

### Important Git Commands

| Command | Purpose |
|---|---|
| `git clone` | Download repository |
| `git status` | Check file changes |
| `git add .` | Add modified files |
| `git commit` | Save changes locally |
| `git push` | Upload changes to GitHub |
| `git pull` | Download latest changes |
| `git log` | View commit history |

### Advantages

1. Easy source-code management.
2. Maintains project history.
3. Allows developers to work from different systems.
4. Supports backup of source code in a remote repository.
5. Simplifies project updates and collaboration.

### Result
Thus, the complete workflow for managing a Raspberry Pi embedded C++ project using GitHub is understood through cloning, modifying, adding, committing, pushing and pulling source-code files.

---

## 3. Role of GitHub in Embedded Application Development

### Aim
To analyse the role of GitHub in embedded application development through repository creation, source-code uploading, version tracking and collaboration.

### Introduction
GitHub plays an important role in embedded application development by providing a centralized platform for storing, managing and sharing source code.

It is useful for projects developed using Raspberry Pi, Arduino, ESP32 and other embedded platforms.

### 1. Repository Creation

A repository is a storage location for project files and source code.

Steps:
1. Open GitHub.
2. Click New Repository.
3. Enter the project name.
4. Add a project description.
5. Select Public or Private.
6. Click Create Repository.

Example: `raspberry-pi-temperature-monitor`

### 2. Source-Code Uploading

Developers can upload source-code files to GitHub.

Example project files:

```text
raspberry-pi-temperature-monitor/
│
├── main.cpp
├── sensor.cpp
├── sensor.h
├── README.md
└── .gitignore
```

The `main.cpp` file contains the main program, while `sensor.cpp` and `sensor.h` contain sensor-related functions.

Files can be uploaded through the GitHub website or using Git commands.

```bash
git add .
git commit -m "Uploaded embedded source code"
git push origin main
```

### 3. Version Tracking

Version tracking records changes made to the project over time.

For example:

- Version 1: Basic sensor reading.
- Version 2: Added LCD display.
- Version 3: Added temperature alarm.
- Version 4: Improved program performance.

GitHub maintains the commit history, allowing developers to view previous changes and restore earlier versions when required.

### 4. Collaboration Among Developers

GitHub allows multiple developers to work on the same embedded project.

Important collaboration features:

- **Branches:** Developers can work on different features independently.
- **Pull Requests:** Developers can propose changes for review.
- **Code Review:** Other developers can check the source code.
- **Issues:** Developers can report bugs and track project problems.
- **Merging:** Approved changes can be combined into the main project.

### Example: Raspberry Pi Smart Home Automation

Consider a smart home automation project using Raspberry Pi.

| Developer | Responsibility |
|---|---|
| Developer 1 | Sensor programming |
| Developer 2 | Relay control |
| Developer 3 | LCD display |
| Developer 4 | Main program integration |

Each developer can create a separate branch and upload their work. After testing and reviewing, all changes can be merged into the main branch.

### Advantages of GitHub in Embedded Development

1. Provides centralized source-code storage.
2. Maintains different project versions.
3. Supports teamwork among developers.
4. Helps identify and fix software errors.
5. Provides project documentation through README files.
6. Allows developers to access projects from different locations.
7. Improves project development and maintenance.

### Result
Thus, GitHub plays an important role in embedded application development by providing repository management, source-code uploading, version tracking and collaboration facilities. It makes Raspberry Pi and other embedded projects easier to develop, maintain and share.

---

## Conclusion

GitHub is an important tool for embedded application development. It helps developers store source code, maintain different versions, track changes and collaborate with team members. By using Git commands such as clone, add, commit, push and pull, developers can efficiently manage Raspberry Pi embedded C++ projects.
