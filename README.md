# CECS 478 Course Project: Privacy Review of a Campus Data Release

All records are synthetic. They describe fictional students at a fictional university.

## Files

Each scenario folder contains the same three files.

| File | Contents |
| --- | --- |
| `release_request.csv` | The requested rows and fields, with names and email addresses removed and student IDs hashed |
| `public_auxiliary.csv` | Public information on 1,500 people from club rosters, a people-search site, and social-media profiles |
| `leaked_roster.csv` | 250 names, student IDs, and majors from a scholarship spreadsheet posted by mistake on a public club drive |

Student IDs are nine digits and begin with `029`. The data office computes `student_hash` as the SHA-256 hash of the student ID written as a nine-digit string.

## Fields

| Field | Scenarios | Meaning |
| --- | --- | --- |
| `student_hash` | A, B, C | SHA-256 of the student ID |
| `birth_date` | A, B, C | Date of birth, YYYY-MM-DD |
| `gender` | all files | Woman, Man, or Nonbinary |
| `home_zip` | all files | Five-digit home ZIP code |
| `major` | all files | Declared major |
| `class_level` | all files | Freshman, Sophomore, Junior, Senior, or Graduate |
| `residence` | A, C, auxiliary | Residence hall, campus apartments, or Off campus |
| `international` | A, C | Yes or No |
| `insurance` | A | Insurance on file at the Health Center |
| `visits_this_term` | A | Number of Health Center visits this term |
| `last_visit_month` | A | Month of the most recent visit |
| `primary_reason` | A | Primary reason for the student's visits |
| `transfer` | B, C | Transfer student, Yes or No |
| `first_generation` | B, C | First-generation college student, Yes or No |
| `pell_eligible` | B | Pell Grant eligibility, Yes or No |
| `course` | B | Gateway course |
| `weekly_logins` | B | Average learning-platform logins per week |
| `submission_rate` | B | Share of assignments submitted, 0 to 1 |
| `accommodation` | B | Registered disability accommodation, Yes or No |
| `final_grade` | B | A, B, C, D, F, or W |
| `dependents` | C | Has dependents, Yes or No |
| `work_hours` | C | Paid work hours per week |
| `food_insecure` | C | Food insecure by the survey's screening questions, Yes or No |
| `housing_insecure` | C | Housing insecure in the past year, Yes or No |
| `phq2_score` | C | PHQ-2 depression-screening score, 0 to 6 |
| `name` | auxiliary, roster | Full name |
| `birth_year` | auxiliary | Birth year, blank when unknown |
| `source` | auxiliary | Where the outsider found the entry |
| `student_id` | roster | Nine-digit student ID |

## Getting started

Open `CECS478_Project_Starter.ipynb` in Google Colab or Jupyter. Set `SCENARIO` in the first code cell and run the cell. In Colab, upload the scenario folder to the Files panel first. Read ZIP codes and student IDs as text so leading zeros are kept.

The starter notebook only loads the files. Your team writes the analysis. Before you submit, restart the runtime and run every cell.
