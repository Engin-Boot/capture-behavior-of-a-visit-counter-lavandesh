# Visit-counter for a Facilities Manager

## Scenario: Report visitor trends during a week of operation

(Assumption - The Facilities manager has interest
in the predictions of the visits not the past trends)

- Given : The 'visit-counter' UI has a tab
'Prediction generator' with option to select
the 'Duration' of prediction like 'next week',
'next 30 days' and 'next 90 days'
and a 'Get Report' button.

- When : Select 'next week' option
in 'Duration' and Press 'Get Report' button.

- Then : Generate a pdf report having
shift-wise predictions, in the form of
line graph with error bars, for the duration.

## Scenario: Alert when seating capacity is full

- Given : The sensor of 'visit-counter' is working
fine and connects to the database and syncs
regularly. There is a in-built method in the
software 'visit-counter' to determine the number
of seats occupied at any given time.

- When : Number of people according to footfall counter is
more than 1.1 times the seating capacity.
(considering 10 percent of people in
hospital are their staff)

- Then : Send an alert 'Seating Capacity is full'
in form of Push notification, SMS and email
to Facilities manager.
