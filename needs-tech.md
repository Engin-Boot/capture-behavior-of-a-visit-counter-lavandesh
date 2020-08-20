# Visit-counter technical needs

Scenario: Recover across restarts of the server
that runs the visit-counter

  Given : 'visit-counter' and sensor are running and connected to the server
  and syncs at the intervals of 5 ms
  
  When : Initiate and complete the restart of 'visit-counter'
  
  Then : 

Scenario: Reconcile counts if the sensor is offline for a while

  Given
  When
  Then
