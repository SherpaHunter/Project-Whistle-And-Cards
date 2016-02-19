# Whistle and cards data schema draft
This is a draft for the project 'Whistle and cards' APP development.  
We need to review this document and finalize the first offical version by the end of 10/03/2016.

## League Licenced Referee Information Table

**Table name:** 
 
```
Licenced_Referees
```
**Descriptoin:**  
This table contains authorized referee in the league. It can be used to authentication of registered referee within the league.

**Attributes:**

```
LicenceID: String,
Name: String,
Overdue: Date
```

## Referee Information Table

**Table name:** 
 
```
Referee_Info
```
**Descriptoin:**  
This table contains detailed information of each referee. It takes referee's individual input as the input and save them into database.

**Attributes:**

```
ID: Integer,
Name: String,
Gender: String,
DOB: Date,
Address: String,
Mobile: String,
Home_phone:String,
LicenceID: String
```
## Game Information Table

**Table name:**
  
```
Game_Info
```
**Descriptoin:**  
This table contains detailed information of each game.

**Attributes:**

```
ID: Integer,
AssignedDate: Date,
StartTime: Date,
EndTime: Date,
Place: String,
HostTeamID: Integer,
VisitTeamID: Integer,
RefereeID1: Integer,
RefereeID2: Integer,
RefereeID3: Integer,
RefereeID4: Integer,
Description: String
```

## Team Information Table

**Table name:**
  
```
Team_Info
```
**Descriptoin:**  
This table contains detailed information of each team within the league. Each time will have a unique id as a key.

**Attributes:**

```
ID: Integer,
Name: String,
ContactName: String,
ContactNumber: String,
Address: String,
Level: String,
Description: String
```
## Referee Proposal Avaliable Table

**Table name:**
  
```
Referee_proposal
```
**Descriptoin:**  
This table will take each referee's input as a row and save it into the database, which include avaliable date and interval, as well as prefered location.

**Attributes:**

```
RefereeID: Integer,
AvailableDate: Date,
AvailableStart: Date,
AvailableEnd: Date,
AreaSelectingRule: String,
Comments: String
```

## Administrator Proposal Game Date Proposal Table

**Table name:**
  
```
Admin_gameDate_proposal
```
**Descriptoin:**  
This table contains admin's proposal game date for the game season. And each referee can send his/her confirmation on different game days and it'll update this information back into this table.

**Attributes:**

```
GameDate: Date,
ConfirmDeadline: Date,
ConfirmedReferees: Object,
Comments: String
```