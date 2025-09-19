## Data Schema Reference

### Exercise 1

**Schema** 

id — Unique record identifier for this delivery/appointment cycle
facility_name — Health facility where the patient is registered/served
ccc — Pseudonymized patient code (CCC-like identifier)
age — Patient age in years
sex — Patient sex (e.g., Male/Female)
client_type — Patient/program category (e.g., New, Returning, PMTCT, Adolescent, Adult, Key Population)
sub_county — Administrative sub-county of the facility/patient
last_vl_date — Date of last viral load sample/record (if available)
drug_refill_date — Date medications were dispensed/refilled for this cycle
prefered_delivery_date — Patient’s requested date for delivery or pickup
delivery_type — Mode of delivery (Home Delivery, Pick-up Station, Facility Pickup)
delivery_package — Regimen and days shorthand (e.g., TLD 60, TLD 90, TLE 30)
prefered_delivery_location — Requested delivery location label (e.g., Home, Market, Facility)
actual_delivery_date — Date the delivery actually occurred (blank if not delivered)
actual_delivery_location — Location where delivery was completed (blank if not delivered)
delivery_geocoordinates — Latitude,Longitude string for the delivery location (approximate)
delivery_outcome — Result of delivery attempt (e.g., Delivered, Not Delivered – Unreachable/Moved/etc.)
delivery_time — Local time of the delivery event or attempt (HH:MM)
medication_returned — Whether the medication package was returned to stock (Yes/No)
name_of_rider — Rider identifier/name for operational tracing
comments — Short operational note (e.g., unreachable, moved, rescheduled)
county — Administrative county of the facility/patient
created_at — Timestamp when the record was created
created_by — User/system that created the record
updated_at — Timestamp of last update to the record
updated_by — User/system that last updated the record
dob — Patient date of birth (pseudonymized/approximate)
county_of_residence — Patient’s county of residence
group_identifier — Cohort label (e.g., AGYW, KeyPop, Adolescents, General)
mmd_days — Days of medication dispensed at last refill (e.g., 30/60/90/180)
next_appointment_date — Scheduled next clinic visit date provided at last encounter
appointment_attended_date — Date the appointment was actually attended (blank if missed/transferred/deceased)
appointment_status — Appointment outcome (attended, missed, rescheduled, transferred, deceased)

### Exercise 2 

**Schema**

anon_id — Anonymized patient identifier (use for grouped train/test splits)
encounter_date — Date of the current clinical encounter/record
Diagnosis_Date — Date of initial HIV diagnosis
age_at_encounter — Age (years) at the encounter date
weight — Patient weight (kg) at/near encounter
height — Patient height (cm) at/near encounter
Age at Reporting — Age (years) at reporting/reference time
CD4_Count — CD4 cell count (cells/µL)
Current_WHO_HIV_Stage — WHO HIV clinical stage (I–IV) at/near encounter
Viral_Load — HIV viral load (copies/mL)
days_late — Days late relative to the scheduled appointment (positive = late)
iit_flag — Appointment non-adherence label (1 if days_late > 28, else 0)
early_arrival — Indicator: arrived before scheduled date (0/1)
on_time — Indicator: attended on/near scheduled date (0/1)
late_arrival — Indicator: arrived after scheduled date (0/1)
past_encounters — Count of prior recorded encounters for the patient
pct_late_arrivals — % of past encounters that were late (0–100 or 0–1 scale)
prev_iit_status — IIT flag for the immediately previous encounter (0/1)
second_last_iit_status — IIT flag for the second previous encounter (0/1)
num_past_iits — Total count of past IIT events up to this record
success_flag — Binary success outcome for this cycle as defined in preprocessing (0/1)
overall_appointment_success — Derived appointment adherence status for this record (0/1)
time_since_diagnosis_at_scheduled_appointment — Days between diagnosis date and the scheduled appointment date
Is_ART — Indicator: currently on ART (0/1)
gender — Patient gender (e.g., M/F)
Current Regimen Line — Treatment line at encounter (e.g., First Line, Second Line)
TPT Outcome — Tuberculosis Preventive Therapy outcome (e.g., Completed / Not Completed)
Establishment — Facility/clinic name for the encounter
Next_clinical_appointment — Date of the next scheduled clinical appointment
NCDs — Recorded non-communicable conditions (e.g., Hypertension, None)
age_group — Age bucket (e.g., 26–35, 36–45, 46–60)
adherence_predicted — Model predicted class for adherence/LTFU (0/1) from baseline (see starter code for class meaning)

## Exercise 4

**Sheet: Product Backlog — Schema**

Product Backlog ID — Unique identifier of the business request (e.g., PB0001)
Request Description — Detailed description of the business ask/request
Business Priority — Priority set by the business (e.g., High/Medium/Low)
Business Cluster — Business area/category (e.g., Retail, Finance, Analytics, Infrastructure, Data Strategy)
Acceptance Criteria — Conditions that must be met for the request to be accepted as done
Requested By — Name/role of the requester or sponsoring stakeholder
Requested When — Date/time the request was raised
Business Value — Relative value score used for prioritization
Sprint Backlog ID — Link to the corresponding sprint user story (e.g., SB0001)
User Story Description — Decomposition of the request into a user story/implementation note
User Story Type — Category of work (Feature, Defect, Enabler)
Value Stream — Impacted value stream (e.g., Customer Experience, Payment Reliability, Data Infrastructure, IT Operations, Business Analytics)

**Sheet: Sprint Backlog — Schema**

User Story No — Unique identifier for the sprint story (e.g., SB0001)
User Story Name — Short title of the sprint story
User Story Description incl. Expected Outcome — Detailed story description including expected business/technical outcome
Business Priority — Priority of the story within the sprint (e.g., High/Medium/Low)
User Story Type — Category of work (Feature, Defect, Enabler)
User Acceptance Criteria (UAT) — Acceptance criteria to verify completion and quality
Estimates — Effort estimate for the story 
Mandays — Effort expressed in person-days 
Owner — Primary assignee or responsible team member
Sponsor — Business sponsor or stakeholder for the story
Value Stream — Value stream associated with the story 