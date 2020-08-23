# Visit-counter for a Director

## Scenario: Show patient visits during working days and holidays

(Assumption - The director has interest in the
past trends of the visits not the predictions)

- Given : The 'visit-counter' UI has a tab 'Total
  visits' with option to select the 'Duration' like
  'last week', 'last 30 days' and 'last 90 days'
  and a 'Get Report' button.
  
  - When : Select one of the options in 'Duration'
  and Press 'Get Report' button.
  
  - Then : Generate a pdf report having shift-wise
  data of total number of visits, in the form of
  line graph with error bars, for the select
  duration and color-code the day, that is, green
  for working days and red for holidays.

## Scenario: Compute parking slots to reserve for visiting specialists

(Assumption - I am writing this feature in the
context of 'visit-counter' software, this software
does not take care of schedules and usual calender stuff)

- Given : 'Visit-counter' can import the
  schedule of visits from external software.
  There is a in-built method in the software
  'visit-counter' to determine the number of
  parking slots occupied at any given time.

  - When : Occupied parking slots reach 80 percent
  of total available parking slots(Total parking
  slots - number of reserve parking slots for
  next 1 hour) OR when external software notify
  new reservation OR one hour before each visit
  of specialists.

  - Then : Generate a push notification and SMS alert,
  containing the number of slots to reserve
  and the time of visit of consultants.
