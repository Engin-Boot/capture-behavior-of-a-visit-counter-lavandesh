# Visit-counter for a Facilities Manager

Scenario: Report visitor trends during a week of operation

 Given : The sensor database is working
 and sensor worked for last 7 days
  
  When : Request report of visitors trend
  for last week
  
  Then : Generate a report with number of
  visitors
  visited hospital in last 7 seven days

Scenario: Alert when seating capacity is full

  Given : When the 'visit-counter' is ON and working

  When : Number of people on footfall counter is
  more than 1.2 time the seating capacity

  Then : Generate an alert for more seating capacity.
