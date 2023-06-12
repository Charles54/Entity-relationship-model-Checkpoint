# Entity-relationship-model-Checkpoint

           +-----------------+
           |    Gymnasium    |
           +-----------------+
           | gym_id (PK)     |
           | name            |
           | address         |
           | phone_number    |
           +-----------------+
                  |
                  |
             +----+------+
             |           |
     +-------+-------+   |   +------------------+
     |  Coach        |   |   |    Session       |
     +---------------+   |   +------------------+
     | coach_id (PK) |   |   | session_id (PK)  |
     | last_name     |   |   | sport_type       |
     | first_name    |   |   | schedule         |
     | age           |   |   | max_capacity     |
     | specialty     |   |   +------------------+
     +---------------+   |
                         |
         +---------------+-----------------+
         |               |                 |
+--------+--------+ +----+-----+   +-------+-------+
|   Member        | |   Attendance  | |    Enrollment  |
+-----------------+ +---------------+ +---------------+
| member_id (PK)  | | attendance_id  | | enrollment_id |
| last_name       | | member_id (FK) | | member_id (FK)|
| first_name      | | session_id (FK)| | session_id (FK)|
| address         | +---------------+ +---------------+
| date_of_birth   |
| gender          |
+-----------------+
