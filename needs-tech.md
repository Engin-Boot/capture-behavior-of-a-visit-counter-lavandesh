# Visit-counter technical needs

Scenario: Recover across restarts of the
server that runs the visit-counter

- Given : Sensors are running and
connects to the server of 'Visit-counter'
and syncs at the intervals of 5 sec

- When : 'Visit-counter' server restarts
and re-establishes
connection to the sensor.

- Then : Sensor checks the time-stamp
of the last synchronization to the database
and if it is different than what it is in local
memory then updates the latest count of visitors
to server Database.

Scenario: Reconcile counts if the sensor
is offline for a while

- Given : Server of 'Visit-counter' is up and running.

- When : Sensor goes offline
and comes back online
and send 'setup' request to the server.

- Then : Server updates the 'Count'
and 'time-stamp' variable of the sensor system
by retrieving last count and time-stamp
on the server database.
