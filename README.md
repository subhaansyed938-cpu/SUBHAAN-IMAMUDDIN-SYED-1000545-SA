# ParentConnect AI — School Communication Assistant

## 1. Project Overview

**ParentConnect AI** is an AI-powered school communication chatbot developed using **Google Dialogflow ES**. It is designed to help parents access common school-related information quickly and conveniently through natural-language conversations.

The project was developed for the *Artificial Intelligence: Real-World Applications and Implications* summative assessment, under **Scenario 2: ParentConnect AI — School Communication Assistant**.

The chatbot aims to improve communication between parents and schools by reducing the need for repeated manual enquiries and making frequently requested information easier to access.

## 2. Problem Statement

Parents frequently need information about student attendance, examination schedules, fee payments, school announcements, homework, and school procedures. Obtaining this information manually can require repeated calls, messages, or visits to school.

ParentConnect AI addresses this problem by providing a conversational interface where parents can ask questions in everyday language and receive relevant responses.

## 3. Project Objectives

- Provide quick access to common school-related information.
- Help parents check attendance information and examination schedules.
- Answer questions about school fees and payment deadlines.
- Share school announcements and event updates.
- Provide information about school timings, homework, leave applications, and teacher contacts.
- Use Dialogflow intents and entities to understand different user queries.
- Improve usability through welcome messages, help responses, and fallback handling.
- Demonstrate the practical application of conversational AI in education.

## 4. Technology Stack

| Technology | Purpose |

 Google Dialogflow ES : Natural-language understanding and chatbot conversation management.
 Dialogflow Intents : Identify the purpose of a parent's message.
 Dialogflow Entities : Identify relevant information and categories within user messages.
 GitHub : Version control, source files, and project documentation.
 Google Drive : Hosting the sample examination timetable.

**Integration approach:** The supplied agent is configured as a Dialogflow ES chatbot without a custom webhook. Its configured intent responses handle the supported queries.

## 5. Main Features

### Student Attendance
Provides a sample attendance summary without requiring the parent to enter a student's name.

### Examination Schedule
Responds to examination timetable enquiries and provides a link to the sample timetable.

[Open the Sample Examination Timetable](https://drive.google.com/file/d/1_OZPH4WyZrJ70TGsp3C1UIMGxzqQEFX6/view?usp=sharing)

### Fee Details and Payment Deadlines
Provides configured sample information about tuition fees, transport fees, extracurricular charges, and payment deadlines.

### School Announcements and Events
Provides configured school updates, including sample parent-teacher meeting and school-event announcements.

### School Timings and General Help
Answers common questions about school hours and how to obtain assistance with school procedures.

### Homework and Leave Applications
Supports common homework-related enquiries and questions about student absence or leave procedures.

### Teacher Contact and Student Information
Handles relevant enquiries about teacher contacts and general student information.

### Welcome and Fallback Responses
Welcomes users, provides general assistance, and offers a fallback response when a query is not recognised.

> **Important:** Attendance figures, fee amounts, school timings, and announcement dates in this project are configured sample data. They must not be treated as verified information from a real school.

## 6. Dialogflow Intents

The supplied Dialogflow ES agent contains the following intent files:



Copy and paste this Markdown table directly into your GitHub `README.md` file. GitHub will automatically format it into a readable table.

## Dialogflow ES – Intent Overview

| No. | Intent Name             | Description                                              |
| --- | ----------------------- | -------------------------------------------------------- |
| 1   | Welcome the Parent      | Greets users and introduces the chatbot.                 |
| 2   | General Help            | Explains the chatbot's supported functions.              |
| 3   | School Timings          | Provides configured school-hour information.             |
| 4   | Attendance              | Returns the sample attendance summary.                   |
| 5   | Absence Reason          | Handles enquiries about student absence.                 |
| 6   | Leave Application       | Provides guidance about leave applications.              |
| 7   | Exam Schedule           | Shares the examination timetable link.                   |
| 8   | Exam Results            | Handles examination-result enquiries.                    |
| 9   | Homework                | Responds to homework-related questions.                  |
| 10  | Fee Details             | Provides configured fee information.                     |
| 11  | Fee Payment             | Handles fee-payment enquiries.                           |
| 12  | Fee Deadlines           | Provides information about payment deadlines.            |
| 13  | School Announcement     | Shares configured school announcements.                  |
| 14  | Teacher Contact         | Handles teacher-contact enquiries.                       |
| 15  | Student Information     | Handles general student-information enquiries.           |
| 16  | Default Fallback Intent | Responds when the chatbot cannot match a user's message. |
| 17  | Goodbye                 | Ends the conversation.                                   |



These intents cover the major communication needs identified in the ParentConnect AI scenario.

## 7. Custom Entities

The supplied agent includes the following custom entities:


 ## Dialogflow ES – Entity Overview

| No. | Entity Name         | Description                                 |
| --- | ------------------- | ------------------------------------------- |
| 1   | Subject           | Represents academic subjects.               |
| 2   | Announcement_type | Categorizes school announcements.           |
| 3   | Absence_reason    | Represents reasons for student absence.     |
| 4   | Day_type          | Represents categories of days.              |
| 5   | Period            | Represents school periods or time slots.    |
| 6   | Section           | Represents student sections.                |
| 7   | Fee type          | Categorizes types of school fees.           |
| 8   | Payment method    | Represents payment methods.                 |
| 9   | Exam type         | Categorizes examinations.                   |
| 10  | Grades            | Represents grades or academic levels.       |
| 11  | Contact_role      | Identifies contact roles, such as teachers. |



Entities help Dialogflow identify relevant categories in user messages and support the organisation of school-related queries.

## 8. Sample Chatbot Interactions

The following examples illustrate the intended use of the chatbot. Actual responses depend on the configured Dialogflow agent.

**Example 1: Attendance**

Parent: "What is my child's attendance?"

ParentConnect AI: Returns the configured sample attendance summary of 92% attendance, based on 92 days present out of 100 working days.

**Example 2: Examination Schedule**

Parent: "When are the exams?"

ParentConnect AI: Provides the examination timetable link.

**Example 3: Fee Details**

Parent: "What are the school fees?"

ParentConnect AI: Returns the configured sample fee breakdown.

**Example 4: School Events**

Parent: "Any upcoming school events?"

ParentConnect AI: Provides a configured school announcement or event update.

**Example 5: General Help**

Parent: "What can you help me with?"

ParentConnect AI: Explains the supported school-information categories.

## 9. Repository Structure

The GitHub repository is organised to keep the agent export, documentation, and testing materials together.

```
ParentConnect-AI/
│
├── README.md
│
├── dialogflow-agent/
│   └── Parent_Connect_AI_Dialogflow_ES.zip
│
├── docs/
│   └── intents-and-entities.md
│
├── tests/
│   └── test-plan.md
│
└── PUBLISHING-CHECKLIST.md
```

## 10. Installation and Setup

To import the chatbot into Google Dialogflow ES:

1. Download the Dialogflow agent ZIP file from this repository.
2. Open the [Dialogflow Console](https://dialogflow.cloud.google.com/).
3. Select or create a Dialogflow ES agent.
4. Open the agent settings and locate the import/export options.
5. Choose **Restore from ZIP** or the equivalent restore option.
6. Select the downloaded agent ZIP file.
7. Confirm the restore operation and allow the import to finish.
8. Open the Dialogflow ES test console and try the sample queries listed in this README.

**Note:** Import the Dialogflow agent ZIP itself, not the entire GitHub repository ZIP.

## 11. Testing and Optimization

The chatbot should be tested using different natural-language queries to verify intent matching and response accuracy.

| Test | Example query | Expected behaviour |

 1  - "Hello" : Displays the welcome response.
 2  - "What are the school timings?" : Returns configured school timings.
 3  - "Show attendance" : Returns the sample attendance summary.
 4  - "When are the exams?" : Provides the examination timetable link.
 5  - "Tell me about school fees" : Returns configured fee information.
 6  - "Any event updates?" : Returns a configured school announcement.
 7  - "I need to apply for leave" : Provides leave-application guidance.
 8  - "What homework is there?" : Matches the homework-related intent.
 9  - "How can I contact a teacher?" : Matches the teacher-contact intent.
 10 - An unrelated or unclear message : Displays a fallback response.

**Testing status:** These are planned test cases. Mark each case as passed or failed only after testing it in the Dialogflow console. Record any errors and update training phrases or responses where necessary.

## 12. Deployment and Live Chatbot

The chatbot is configured in Google Dialogflow ES. A public-facing demonstration link must be added after the chatbot has been deployed or connected to an accessible interface.

Live chatbot link: https://www.gstatic.com/dialogflow-console/fast/messenger/bootstrap.js?v=1

The Dialogflow console test panel is useful for development and testing, but it should not automatically be treated as a public live-chatbot URL.

## 13. Limitations and Future Improvements

### Current limitations

- The supplied responses contain sample school information rather than verified live school records.
- The agent does not have a custom webhook connected to a school database.
- Attendance and fee responses should not be interpreted as personalised, live student records.
- The chatbot's accuracy depends on its training phrases, intent configuration, entities, and responses.
- A public deployment link must be configured separately if a public demonstration is required.

### Future improvements

- Integrate an authorised school information system through a secure backend.
- Provide verified, student-specific information after appropriate authentication.
- Add richer interactive responses and clearer navigation between topics.
- Expand training phrases using feedback from testing.
- Improve accessibility and support for additional languages.
- Add privacy and data-protection safeguards before handling real student information.

## 14. Ethical Considerations

ParentConnect AI is intended to improve communication and accessibility, not replace official school staff or systems.

A production implementation should protect student and parent information, restrict access to authorised users, and avoid presenting sample or outdated information as official records. Sensitive student information should only be accessed through secure, authorised integrations.

## 15. Assignment Alignment

This project addresses **Scenario 2: ParentConnect AI — School Communication Assistant** in the CRS Artificial Intelligence summative assessment.

The assignment calls for at least 15 intents and 10 entities, contextual responses, suggestion prompts, testing with at least five realistic scenarios, deployment, and a detailed GitHub README containing integration details and a live chatbot link.

The supplied agent export lists 16 intent files, including the fallback intent, and 11 custom entities. Testing results and the live deployment link should be completed and verified before final submission.

## 16. Project Information

- Project name: ParentConnect AI
- Scenario: Scenario 2 — School Communication Assistant
- Course: Artificial Intelligence: Real-World Applications and Implications
- Platform: Google Dialogflow ES
- Student name: Subhaan Imamuddin Syed
- Candidate registration number: 1000545
- School name: Aspee Nutan Academy

## 17. References

- [Google Dialogflow documentation](https://cloud.google.com/dialogflow/docs)
- [Dialogflow ES documentation](https://cloud.google.com/dialogflow/es/docs)
- [Dialogflow conversation design tips](https://developers.google.com/assistant/df-asdk/dialogflow/tips)

---

*ParentConnect AI demonstrates how conversational AI can support school communication by making common information easier to request and access. The project can be extended into a production-ready assistant through verified school integrations, secure data handling, testing, and deployment.*

