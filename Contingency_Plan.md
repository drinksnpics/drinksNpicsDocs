# DrinksNPics Platform Contingency Plan
[Draft]


## Acknowledgements

This Platform Recovery Plan is created by the ThreeAmigos Developer Group for the capacitation and use of the System Administrator at DrinksNPics Cinemas, at their only location at Aguascalientes, Aguascalientes, México.

## Risk Evaluation

The following risks have been identified.

* Database gets corrupted.
* TheMovieDatabase API stops receiving support.

## Prevention Plan

### Backup
A daily backup of the firebase database must be performed for all nodes every day at 10:PM, and stored as a JSON file in the establishment facilities.

Every node (table) must be exported to JSON Separately, in case a single node becomes corrupted, son that it can be easily and modularly restored.

### System Checks
Once every two months, service should be paused, and the servers where the application is mounted over will have to perform a maintenance routine.
Such process must include but it is not limited to.

* Physical dust cleanup.
* Cache deleting.
* Disk revisions.
* Log deletion and exploration.

### Own DB
It is a latent risk that one day TheMovieDatabase support will end. Rendering every single movie information site useless.

A recommended countermeasure would be to copy the retrieved data from such sites to a DrinksNPics owned server that could be used as a relay for the lost information.

## Recovery Plan

### Data Loss
In case a data base goes corrupt, do the following

1.- The corrupted data must be backed up
2.- The latest backup must be restored in the firebase server
3.- Use a script to find the different records in within the two and recover the uncorrupted records manually.

### Service is Down
1.- Perform integrity checks in the following platforms.  
  * DrinksNPics Admin Server
  * Firebase
2.- Fix any error with the help of logs.
3.- Restart the applications if no error was encountered.

## Contact
support@threeamigos.org
