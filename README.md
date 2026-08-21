# DOSW Laboratory 3

## Requirements

**Course:** DOSW — Software Development and Operations  
**Institution:** Escuela Colombiana de Ingeniería Julio Garavito  
**Activity:** Express Hackathon 2026-2 
**Work mode:** Teams of three students  
**Estimated in-class time:** 3 hours

---

## 1. Laboratory Objective

The objective of this laboratory is to apply requirements definition and analysis techniques through a practical case study, enabling students to develop proficiency in these first two phases of the software development life cycle.

---

## 2. Prerequisites

Before getting started, please consider the following recommendations:

* Select a diagramming tool of your choice that supports UML and C4 Model standards. Suggestions: _Miro, Draw.io or Lucidchart_.
* Select a mockup and user flow design tool of your choice. Suggestions: _Miro or Figma_.
* Before the laboratory session, create an account for each team member on the selected tool(s).
* Create a GitHub repository named: `DOSW_Lab3_InitialFirstNameOfEachMember`. **Important**: Create the repository with the options to include the README and `.gitignore` files.
* Create the *develop* branch from *main*.
* Do not forget to add the professor as a collaborator to the repository and send its URL via Teams.
* Make sure to distribute the commits appropriately so that the work completed by each team member is clearly visible.

---

## 3. Case Study

**TechCup** is a digital platform for managing the semester-long soccer tournament organized for the Systems Engineering, Artificial Intelligence Engineering, Cybersecurity Engineering, and Statistical Engineering programs at Escuela Colombiana de Ingeniería Julio Garavito. The system will be used by students, team captains, and tournament organizers.

The TechCup logo is available at the following [link](https://github.com/DOSW-2026-2/Requirements/blob/9e0d4cd367cad363ac73cac08c0a52b802e1b3ef/docs/TechCup_Logo.png).

In this first version of the system, TechCup must provide the basic functionality required to create tournaments and register teams for each tournament.

### Problem Description

Currently, the School does not have a centralized system that allows users to:

* Create a tournament by specifying its basic rules and information (dates, fees, etc.).
* Easily register teams for tournaments.
* Process the registration payment for each team.
* Validate payments made by teams.
* View the teams registered for each tournament.
* Generate reports on registrations for each tournament.
* Send registration payment reports in JSON format to the Dean's Office.

The goal of the system is to ensure that tournaments and registrations comply with specific rules while allowing users to interact with the platform in a simple and secure manner.

### General Business Rules

During interviews with the Dean's Office of the Systems Engineering program, the following basic business rules were identified:

* Tournaments must not last longer than one day.
* Each tournament must be identified by a unique ID consisting of exactly **five digits**, based on the year and academic semester. For example, **20262** represents the second semester of 2026.
* The possible statuses for a tournament are: **Pending, Active, In Progress, Closed, and Cancelled**.
* Only one tournament can be active at a time.
* Each team may register only for the tournament that is currently active.
* Teams must be able to pay the registration fee through **PSE**.
* Tournaments cannot be deleted.

### General Functionalities

The main functionalities of **TechCup** are:

* User authentication using username and password for TechCup organizers and students.
* **Tournament Management Module:** Authorized users (organizers) should be able to create tournaments, change their status, and update tournament information.
* **Team Management Module:** users should be able to create teams, update team information, make registration payments, and register teams for a tournament. These actions may be performed according to the user's role: **captains** can create teams, make payments, and update team information, while **organizers** can perform all actions, including reviewing payments and approving registrations.
* **View the payment made by a team:** Tournament organizers should be able to consult and verify the payment associated with a team's registration.
* **Generate a report of registered teams:** Tournament organizers should be able to generate a report containing the teams registered for a tournament.
* **Generate a report of registration revenue:** Tournament organizers should be able to generate a report of the revenue obtained from registration fees.
* **Delete a tournament and its registered teams.**

---

## 4. PART 1 – Project Structure (20%)

With the goal of gaining a better understanding of the different uses of Maven, you will create a project using _Maven archetypes_.

1. Create the `feature/proj-structure` branch based on the `develop` branch.
2. Answer the following questions in the README:

   1. What is a Maven *Archetype*?
   2. What is the purpose of the `maven-archetype-quickstart` archetype?
   3. What command can be used to create a project based on a Maven archetype?
   4. What is a `pull request` in GitHub?
   5. How do you create a `pull request` in GitHub?
   6. How do you approve a `pull request` in GitHub?
   7. Include the bibliography, using **APA format**, for the sources consulted to answer the questions above.

3. Create the basic project structure using the `maven-archetype-quickstart` archetype ([reference](https://maven.apache.org/archetypes/maven-archetype-quickstart/index.html)).

   1. When running the command to create the project using the archetype, make sure to define:
       * `groupId`: `edu.eci.dosw.lab`
       * `artifactId`: `DOSW-Laboratorio4`
   2. Add the command used to create the project structure to the README.

**Important:** The command should generate a project structure similar to the following:

```text
DOSW-Lab3/
├── pom.xml
├── README.md
└── src/
    ├── main/
    │   └── java/
    │       └── edu/
    │           └── eci/
    │               └── dosw/
    │                   └── lab/
    │                       ├── Application.java
    └── test/
        └── java/
            └── edu/
                └── eci/
                    └── dosw/
                        └── lab/
                            ├── ApplicationTest.java
```

4. Manually add the *docs* package (including its subfolders) to obtain the following structure:

```text
DOSW-Lab3/
├── pom.xml
├── .gitignore
├── README.md
└── src/
|    ├── main/
|    │   └── java/
|    │       └── edu/
|    │           └── eci/
|    │               └── dosw/
|    │                   └── lab/
|    │                       ├── Application.java
|    └── test/
|        └── java/
|            └── edu/
|                └── eci/
|                    └── dosw/
|                        └── lab/
|                           ├── ApplicationTest.java
└── docs/
    ├── uml/
    ├── images/
    ├── requirements/
```

5. Create a pull request to merge the changes from the `feature/proj-structure` branch into `develop`. The pull request must be approved by at least one team member.

**Important:** The pull request cannot be approved by the same person who created it.

---

## 5. PART 2 – Context Diagram (20%)

Prepare the **context diagram** for the **TechCup** system.

1. In the selected tool for C4 diagrams, build the Context Diagram for TechCup.
2. Create the `feature/proj-scope` branch based on the `develop` branch.
3. Export the context diagram you created as an image and save it in the `uml` folder.
4. Create the [*scope.md*](https://github.com/lauherrerac/dosw-lab4-example/blob/aa911e5c9ae703ac531f34d208815a595b40ea1d/docs/requirements/scope-template.md) file in the `requirements` folder (path: `DOSW-Laboratorio4/docs/requirements`). **Note:** Use the document in the link as a template.
5. Complete each section of the file. **Important:** You can fill it in Spanish:

   1. System.
   2. Problem to be solved.
   3. Context Diagram: (Include the image and link to the diagram created in step 1).
   4. System Scope.
      
6. Create a pull request to merge the changes from the `feature/proj-scope` branch into `develop`. The pull request must be approved by at least one team member.

**Important:** The pull request cannot be approved by the same person who created it.

---

## 6. PART 3 – Requirements Definition and Analysis (30%)

Based on the case study and the context diagram developed, complete the following tasks:

1. Create the `feature/proj-requirements` branch based on the `develop` branch.
2. Create the [*requirements.md*](https://github.com/lauherrerac/dosw-lab4-example/blob/00d784d9631da6971bcc472d4f004fd4eec71970/docs/requirements/requirement-template.md) file in the `requirements` folder (path: `DOSW-Lab3/docs/requirements`). **Note:** Use the document in the link as a template.
3. List the main functional and non-functional requirements of the TechChup system (**at least 5 of each type of requirement**). It is not necessary to provide detailed descriptions; mention each requirement in a single sentence.
4. From the list, select **3 functional requirements** of the TechCup system and create a **use case diagram** for each one. The diagrams must follow the **UML standard**.
5. Export the use case diagrams as images and save them in the `uml` folder.
6. Provide a detailed description of each of the 3 functional requirements selected in step 4. Use the template provided in the [*requirements.md*](https://github.com/lauherrerac/dosw-lab4-example/blob/00d784d9631da6971bcc472d4f004fd4eec71970/docs/requirements/requirement-template.md) file.
7. Answer the following questions:

   1. Do you identify any requirement that needs to be further detailed? Which one(s)?
   2. Are there any requirements that contradict each other? Which one(s)?
   3. If you had to prioritize the requirements, which **2 requirements** should be considered the most important and implemented in the first iteration of the project?
   4. Is there any requirement that should not be implemented?
      
8. Create a pull request to merge the changes from the `feature/proj-requirements` branch into `develop`. The pull request must be approved by at least one team member.

**Important:** The pull request cannot be approved by the same person who created it.

---

## 7. PART 4 – Mockups and Navigation Flows (25%)


Based on the case study, the identification and analysis of requirements, complete the following tasks:

1. Create the `feature/proj-design` branch based on the `develop` branch.

2. Select one of the functional requirements described in Part 3. Consider the following suggestions:

   1. Select the requirement for which you have the most detailed information and the least uncertainty.
   2. Select the requirement that includes enough visual elements to allow you to apply different design resources. If none of the requirements meet this criterion, select one and propose the visual elements yourself.
   3. Select a requirement that has at least **3 steps in the main flow**. If none of the requirements meet this criterion, select one and define the 3 steps yourself.

3. Design the **mockups** for the screens involved in the selected functional requirement and its **navigation flow**. Design a **minimum of 3 and a maximum of 5 screens**. Make sure to use the [TechCup logo](https://github.com/DOSW-2026-2/Requirements/blob/9e0d4cd367cad363ac73cac08c0a52b802e1b3ef/docs/TechCup_Logo.png).

4. Export the mockups as images and save them in the `images` folder.

5. Update the `requirements.md` file in your repository by including a link to the mockup associated with the selected requirement.

6. Create a pull request to merge the changes from the `feature/proj-design` branch into `develop`. The pull request must be approved by at least one team member.

**Important:** The pull request cannot be approved by the same person who created it.

---

## 8. PART 5 – Submission (5%)

Create a pull request to merge the changes from the `develop` branch into `main`. The pull request must be approved by at least one team member.

**Important:** The pull request cannot be approved by the same person who created it.

--- 

## 9. Summary

| Item | Percentage |
|---|---|
| PART 1 – Project Structure | 20% |
| PART 2 – Context Diagram | 20% |
| PART 3 – Requirements Definition and Analysis | 30% |
| PART 4 – Mockups and Navigation Flows | 25% |
| PART 5 – Submission | 5% |

--- 

## 10. Submission Checklist

### Project Structure

* [ ] Maven project created using `maven-archetype-quickstart`.
* [ ] Required `groupId` and `artifactId` configured.
* [ ] Required project structure created.
* [ ] Maven command and Archetype questions documented in the README.
* [ ] APA bibliography included.

### Context Diagram

* [ ] Context diagram created using the C4 standard.
* [ ] Diagram exported and saved in `docs/uml`.
* [ ] `scope.md` completed using the provided template.
* [ ] Diagram and system scope included in `scope.md`.

### Requirements

* [ ] At least 5 functional requirements identified.
* [ ] At least 5 non-functional requirements identified.
* [ ] Three functional requirements selected and detailed.
* [ ] UML use case diagram created for each selected requirement.
* [ ] Use case diagrams exported and saved in `docs/uml`.
* [ ] Requirements analysis questions answered.

### Mockups and Navigation Flow

* [ ] One functional requirement selected.
* [ ] Between 3 and 5 screens designed.
* [ ] Navigation flow defined.
* [ ] TechCup logo included.
* [ ] Mockups exported and saved in `docs/images`.
* [ ] `requirements.md` updated with the mockup link.

### Git Workflow and Submission

* [ ] All required feature branches were created from `develop`.
* [ ] All required pull requests were created and approved by a different team member.
* [ ] Changes from all feature branches were merged into `develop`.
* [ ] Final pull request from `develop` to `main` was created, approved, and merged.
* [ ] Repository contains all required files and working links.
* [ ] All team members' contributions are reflected in the Git history.

--- 

## 11. Academic Integrity

All team members must understand and be able to explain the submitted solution. External references, generated code, and AI-assisted content must be reviewed, adapted, tested, and documented according to the instructor's rules.

The repository history must reflect the real participation of all team members.
