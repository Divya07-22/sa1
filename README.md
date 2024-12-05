API Endpoints
1. Add a Habit
POST /habits
Body:

json
Copy code
{
  "name": "Exercise",
  "dailyGoal": 1
}
Response:

json
Copy code
{
  "message": "Habit added successfully",
  "habit": { "id": 1, "name": "Exercise", "dailyGoal": 1, "completion": {} }
}
2. Mark Habit as Complete
PUT /habits/:id
Path Parameter: id (ID of the habit)
Response:

json
Copy code
{
  "message": "Habit marked as complete for today",
  "habit": { "id": 1, "name": "Exercise", "dailyGoal": 1, "completion": { "2024-12-05": true } }
}
3. Get All Habits
GET /habits
Response:

json
Copy code
[
  { "id": 1, "name": "Exercise", "dailyGoal": 1, "completion": { "2024-12-05": true } }
]
4. Weekly Report
GET /habits/report
Response:

json
Copy code
[
  { "id": 1, "name": "Exercise", "weeklyCompletion": 5 }
]
