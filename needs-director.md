# Visit-counter for a Director

Scenario: Show patient visits during working days and holidays

  Given : The sensor database is working
  
  When : the predictions of patient visits are requested
  for particular time period 
  (Example - next week, next month)
  
  Then : Generate a report with estimated number of patients
  visiting hospital on working days and holidays
  for requested time period

Scenario: Compute parking slots to reserve for visiting specialists

  Given : The hospital is open

  When : Schedule of visiting specialists for the day is
  pushed or new visit of consultant is added

  Then : Generate a report with number of slots to reserve along with time of when to reserve slot
