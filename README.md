# MIST 4610 Project 1 (Group 6)

## Team Member Names: 


Hannah Ganeriwal [@hannahganeriwal](https://github.com/hannahganeriwal)

Luke Liu [@lukel04](https://github.com/lukel04)

Robert Black [@robertblack11](https://github.com/robertblack11)

Sarah Kirk [@sarahkirk03](https://github.com/sarahkirk03)

Wyatt Bewley [@wsb38150](https://github.com/wsb38150)

Zachary Bowles [@zeb19037](https://github.com/zeb19037)



## Prompt Used: 


Pretend you are the owner/operator of a college football team needing to build a relational database. You hired some students from the MIST 4610 class at the University of Georgia to create the database for you. They need to know more about your organization to identify which entities, attributes, and relationships are important for you. Start by describing your business as a real client



## Scenario from ChatGPT: 


You are the owner/operator of a college football team, the Bulldogs, at a prestigious university. With a rich history of success on the field and a commitment to academic excellence, your football program is integral to the university's identity. As the owner, you understand the importance of building a comprehensive relational database to streamline operations and support the development of your student-athletes.

You've hired a team of students from the MIST 4610 class at the University of Georgia to create the database for you. To help them understand your organization, you provide insights into key aspects of your football program:




### Entities:


1. Players

2. Coaches

3. Injury Type

4. Injury

5. Academic Advisors

6. Facility

7. Training Session

8. Equipment

9. Player Schedule

10. Position

11. NIL

12. NIL Contract


As the owner/operator of the Bulldogs football team, you're spearheading the implementation of a comprehensive relational database system to optimize team performance and support the development of your student-athletes. This database will efficiently manage essential aspects of the football program, including player management with detailed player information such as name, position, eligibility status, and academic standing, as well as coach details encompassing names, positions, and experience. Additionally, training schedules, workout routines, and medical records will be meticulously organized to optimize player performance and minimize injury risk during training sessions. Game planning and analysis will benefit from data on upcoming matchups and opponent details. Efficient team operations and logistics will be ensured through the management of practice facilities, equipment inventory, and usage. Academic support services for student-athletes will be facilitated by tracking academic advisor information, while injury prevention and management will be supported through the tracking of player injuries, treatments, and severity levels. By centralizing critical data and streamlining operations, this relational database will contribute to the continued success and excellence of the Bulldogs' football program.

Efficient team operations and logistics will be ensured through the management of practice facilities, equipment inventory, and usage. Academic support services for student-athletes will be facilitated by tracking academic advisor information, while injury prevention and management will be supported through the tracking of player injuries, treatments, and severity levels. By centralizing critical data and streamlining operations, this relational database will contribute to the continued success and excellence of the Bulldogs' football program.

## Data Model and Description:

  Our data model represents the structure of player management on a hypothetical college football team.  The Players entity represents a player on the team and includes descriptive information about each player.  Since players are the core of a football team, they have the most relationships with other entities.  Each player is also in college, so they have an academic advisor.  The AcademicAdvisory entity contains the name and contact information for each advisor.  Since an advisor can advise many students, there is a one to many relationship between AcademicAdvisor and Players.
  Training is important for the players to perform better and individual players train more than once, therefore there is a one to many relationship between Players and TrainingSession.  TrainingSession includes how long each training session is and also acts as an associative entity between the Players and EquipmentType as well as between Players and Facility.  This relationship is necessary because many players use many facilities and many players use many facilities.  The EquipmentType and Facility entities include descriptive information the user can query.  The Coach entity includes descriptive information about each coach in addition to experience and contact information.  Each coach coaches many training sessions and many players, so there is a one to many relationship between Coach and Players as well as between Coach and TrainingSession.
  The main goal of football is to win matches, and since many matches are played by many players, we created an associative entity between Players and Matches called PlayerSchedule.  The Matches entity contains information about individual matches, such as opponent, date and score.  In addition to being an associative entity, PlayerSchedule includes player information across many matches, including their performance, playtime and status.
  College football players do not make money directly from the school, so they form contracts with NIL companies.  Many players can have many contracts with many NIL companies so there is an associative entity between Players and NILCompany called contracts.  The NILCompany entity includes the name of the company and the Contracts entity includes the date and amount of each contract.
  Lastly, players often get injured within games or practice, so it is important to know which players have been injured and what it was.  Since many players can have many injuries, there is an associative entity between Players and InjuryType called Injury.  InjuryType includes data for what the medical description of the injury was and the Injury entity includes the date and time for when the injury happened.  This is very helpful to know if the player should modify training or sit out from games depending on their condition and how long ago it was.


![Data Model GitHub](https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/dc75944e-2c2f-468d-bb13-e8ce038f659a)

## Data Dictionary: 
<img width="723" alt="Matches Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/543fc2e7-426e-490a-aa47-5ccc69864929">

<img width="723" alt="PlayerSchedule Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/29ca0b97-14c0-4e79-be55-ce4386b06e36">

<img width="595" alt="Players Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/74acca18-e74b-4573-80de-9ee05ed860f0">

<img width="731" alt="Contracts Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/3ef031cf-b32e-45e3-a39a-56a223557a57">

<img width="719" alt="NILCompany Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/d956131a-fb8c-463d-a05d-06289ac7a8b3">

<img width="703" alt="Injury Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/b1a308de-4bae-44e6-b079-31ca30efc0b1">

<img width="687" alt="InjuryType Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/ea5a5a16-9ec0-45c3-b870-81fdc9de0d0f">

<img width="687" alt="EquipmentType Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/2579e2e5-2e55-474f-8e92-8b64687c040c">

<img width="589" alt="TrainingSession Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/0f465c9e-6492-4b0a-a4b1-abb10a0295f4">

<img width="691" alt="Facility Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/384500be-485d-469a-8f37-76f2915a2c24">

<img width="691" alt="Coach Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/9dbe1562-f69d-4dec-bfb6-8c6b60d5c81a">

<img width="726" alt="AcademicAdvisor Table" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/7630e5c4-1958-4f84-bffb-87f896327bc4">


## Query Matrix: 

<img width="778" alt="Query Matrix" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/21d4442b-2c80-4d10-8ac7-afb98bda1151">


## Queries 

### Query 1

<img width="827" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/d2edec00-0f40-4e9f-900c-7da044c762c3">

### Query 2

<img width="770" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/0f91a90b-d028-4129-a085-d4126bee222a">

### Query 3 

<img width="632" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/531d3aab-a7fd-4813-b759-4de440b5f897">

### Query 4

<img width="593" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/42e4ee78-ea62-4b58-a84c-017fef8f0654">

### Query 5 

<img width="632" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/5e8cab3c-ec2d-42b6-a3ef-1e6adcf3a858">

### Query 6 

<img width="721" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/d7420a0e-76f1-40f2-9b5a-1cfa32bc9e44">

### Query 7 

<img width="889" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/4eb6558e-5263-4832-b17d-1e142cb0d7cb">

### Query 8 

<img width="934" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/2d0053b2-36cf-4dc7-ab46-669d133b9c0e">

### Query 9 

<img width="961" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/247064ee-a671-4d9c-ade0-90c0a05f84c7">

### Query 10 

<img width="832" alt="image" src="https://github.com/hannahganeriwal/MIST4610-Project-1--Group-6/assets/152109984/6f192551-80b7-4750-b87a-9d68383b7efb">


## Database Information: 

Name of the Database: ns_Sp24_61608_Group6



