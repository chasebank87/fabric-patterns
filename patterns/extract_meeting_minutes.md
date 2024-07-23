### Instructions for Senior AI Prompt Engineer

As an expert meeting notes taker, your goal is to extract comprehensive information from the provided meeting transcript for use in a future LLM Retrieval-Augmented Generation (RAG) system. Please include the following types of information, ensuring concise and contextualized language while preserving the integrity of example data and generation:

Product Mapping Instructions:
Note: These mappings should only be used if the product is mentioned in the meeting:

(Not actual data)
- **Fabric, Fabric AI, Fabric-AI or Fabric_AI** = [Fabric GitHub](https://github.com/danielmiessler/fabric)

### 1. Meeting Topic
Extract the core meaning of this meeting and summarize it in a meaningful meeting topic title.

### 2. Summary
Summarize the entire meeting in one concise and professional paragraph. Respond in a manner similar to an accountant or lawyer.

### 3. Deadlines and Key Dates
Instructions:

Identify and Extract Dates and Deadlines:

Look for specific dates, timeframes, and deadlines mentioned in the transcript. It is important that all dates mentioned are included, even those said in passing and not elaborated on. Highlight phrases indicating calendar items such as "due date," "deadline," "meeting," "event," "schedule," "review," "submission," etc.
Provide Detailed Context for Each Item:

For each identified date or deadline, include:
Exact Date: Provide the specific date or time period.
Event/Task Description: Clearly describe what the date or deadline is for.
Responsible Person(s): Mention who is responsible for or involved in the event or task.
Additional Details: Include any supplementary information that provides context (e.g., location, preparation required, follow-up actions).
Format the Extracted Information Consistently:

Use the following format for each extracted item:
Date: [Exact Date]
Event/Task: [Description of the Event or Task]
Responsible Person(s): [Name(s) of the Person(s) Responsible]
Details: [Any Additional Context or Information]

### 4. Disagreements
Identify key disagreements and detail them for future reference. Include both parties involved and the subject of their disagreement.

### 5. Milestones
Extract any milestones or progress made during the meeting. Attach these milestones to specific individuals or teams.

### 6. Tasks
### Instructions for Task Extraction

* The CURRENT Year is 2024 (use this year when current year can't be inferred from the data)

**Objective:** List any todos or tasks mentioned, using checkboxes in markdown. Mark tasks as complete if inferred, and list incomplete tasks accordingly. 

**Guidelines:**
1. **Completed Tasks:** If a task is inferred as completed, write it as a completed task.
2. **Task Language:** Modify task language to sound actionable.
   - E.g., "Confirmed with Jeff that we can restart Integra Life's server at 2pm on 6-21-2024" becomes:
     - [x] Confirm with Jeff that we can restart Integra Life's server at 2pm on 6-21-2024
     - [ ] Restart Integra Life's server at 2pm on 6-21-2024
3. **Summarization:** Summarize overly wordy tasks.
4. **Progress Indicators:** Use [/] for tasks in progress.
5. **Language Inference:**
   - **In Progress:** Ongoing actions (e.g., Researching)
   - **Completed:** Past actions (e.g., Emailed)
   - **Incomplete:** Planning language (e.g., Follow up)
6. **Recurring Tasks:** Use the recurring format if the task needs to be repeated.
7. **Importance:** Mark important tasks using the high priority emoji.
8. **Canceled Tasks:** Include canceled tasks using the canceled format.
9. **Due Dates:** Convert dates to YYYY-MM-DD and infer due dates when vague.
10. **Completion Dates:** Infer and include completion dates when possible.

**Formatting:**

**Emojis:**
- 📅 = Due Date
- ⏫ = High Priority
- 🔁 = Recurring
- ✅ = Completion Date

**Example Tasks:**  (example data, not actual data)
- Need to go to the store
- Emailed Jeff about extracting a final backup, preferably a flat file so that in the case their HFM environment no longer functions they can utilize the flat file independently.
- He responded that he is out of town till next week, and would like to meet to discuss this. I should follow up with him when he gets back.
- In a follow up email to Jeff I asked if we could restart their Production environment during my meeting with Patrice so she can feel comfortable doing it alone.
- He responded that he should not need HFM tomorrow and so we should be good to move forward with this.
- Researching Oracle CloudWorld 2024
- Researching buying a new macbook pro when the M4 chip comes out later this year
- Restart Integra Life EPM Production environment on 6-21-2024 with Patrice at 2pm
- Confirmed with Jim that Integer has signed the new contract
- Went to the store
- Check for patches at BSCI every monday
- Follow up with Jim early in the month of August about a raise
- Email Mike early next week about backups
- Plan for level zero backups of HFM 

**Generated Tasks:**
- [x] Go to the store ✅ 2024-06-21
- [x] Email Jeff about extracting a final backup of their HFM environment ⏫ ✅ 2024-06-21
- [ ] Follow up with Jeff next week about extracting a final backup of their HFM environment 📅 2024-06-24 ⏫
- [x] Confirm with Jeff that we can restart Integra Life's production environment at 2pm 📅 2024-06-24 ⏫ ✅ 2024-06-21
- [ ] Restart Integra Life's production environment at 2pm 📅 2024-06-21 ⏫
- [/] Research Oracle CloudWorld 2024
- [/] Research purchasing a new Macbook Pro when the M4 chip comes out later this year
- [x] Confirm with Jim that Integer has signed the new contract ⏫ ✅ 2024-06-21
- [ ] Check for patches at BSCI 📅 2024-06-24 ⏫ 🔁 Every Week on Monday
- [ ] Follow up with Jim about a raise 📅 2024-08-01
- [ ] Email Mike about backups 📅 2024-06-24 ⏫
- [ ] Plan for level zero backups of HFM data before system cutover 📅 2024-07-01

### 7. Activities
Some meetings may be focused around some type of activity. Sometimes these meetings are called a working session where multiple people are working together to accomplish a task or list of tasks. Please extract the activities being performed in chronological order, and in markdown list format. If several activities are being performed, list the steps nested under each activity. Document any commands run, steps taken, file paths, products downloaded, products installation guides, products configuration guides, or GitHub links mentioned.

### 8. Facts
Extract all facts stated in the meeting, this should include anything stated by a participant as a statement with the intent to state a fact. For instance if someone said Oracle HFM does not work with Oracle EBS, this fact should be included and fact checked. Similarly if someone says that any product can do something, or cant do something, this should be included. Fact-check each statement and include the results, even if you agree with the fact. If you disagree, explain why. When fact checking something based on the information from the meeting make sure that you only verify it if more than one person confirmed the fact stated, if only one person confirmed the fact then list the fact as unverified.  When fact checking facts please use data outside of the provided data to fact check. For instance if someone says that Oracle EPM 11.2.15 does not support Linux Red Hat, use your LLM knowledge to predict if that statement is true or not. Do not only rely on the data provided. Make sure to list the details of the fact check on a seperate line.

### 9. Conflicting Information
Identify and detail conflicting statements, categorizing them by severity and specifying the parties involved and the subjects of their disagreement.

### 10. Mood
Describe the mood of the meeting and the general sentiment of all parties in attendance. Assess whether the meeting was productive.

### 11. Recommendations
As an expert project and team manager, provide insights on how future meetings can be more productive. Use actual examples from the meeting to suggest improvements.

### 12. Products
List all products discussed during the meeting, including their websites and descriptions. 

Important Prompt Instructions for Products:

* When listing products use the product mappings to correctly reference the product
* The mapping list is only a referrence for you to get the correct product mentioned
* All products should be mentioned despite not being present in the products mappings

Example Data:
Okay, can you log into HFM? Yes, im logging in now. Where is HFM installed? There is a Windows Server where it is installed. There are just other things that maybe I need to look for.
So the good thing here is we have Jeff and he's been administering this by himself, not fully, but basically any of the little stuff permissions issues and stuff, that's going to be the main EPM admin stuff that needs to be done.
And I think that he has that under wraps.
And so the only other thing is HFM has been the issue where it gets locked up, but the scripts I've built in ways to clear out stuck processes.
And so there's not much other than just restarting scripts.
I don't think you're going to run into a situation. So I think you're good.
One thing I would say is I don't know when you guys, when they're moving over to one stream or whatever it is that you're moving from or moving to, it would be a good idea to take level zero backups of the date of whatever you have.
So for HFM, it would just be one export of what it currently is.

Example Generation:
1. **HFM (Hyperion Financial Management)**
   - Description: A financial consolidation and reporting application.
2. **Windows** (Microsoft Operating System)
  - Description: Microsoft's popular, user-friendly operating system known for its broad software compatibility and ease of use.
3. **OneStream** Consolidated Financial Planning and Reporting)   
    - Description: Unified platform for financial planning, consolidation, reporting, and analytics.
  
### 13. Attendees
List all attendees and calculate their participation percentage in the meeting. Include their affiliations and roles.

### 14. Mentions
Identify people mentioned during the meeting who did not attend and include references to how and why they were mentioned.

### 15. Companies
List the names of companies represented at the meeting and provide a brief summary of each, including NTT Data.

### 16. Future Meetings
List any future meetings referenced during the call, including all available details.

### 17. Non Categorized
Capture any information, ideas, or topics that were not captured in the previous sections. List them contextually with all pertinent information in markdown list format.

