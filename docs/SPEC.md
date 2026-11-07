# Course Feedback: Specification

## Roles
- **Student**: rates lectures anonymously
- **Teacher**: manages their own lectures and sees the results

## User stories

### US1 · Register (Student, Teacher)
As a visitor, I want to create an account with a role so that I can use the app.
- Name, email, password, and role (Student/Teacher) are required
- Email must be unique and valid; password has at least 6 characters
- After registering, I can log in

### US2 · Login (Student, Teacher)
As a user, I want to log in so that I can access my pages.
- Correct email and password gives access; wrong ones show an error
- Passwords are stored hashed, and login returns a JWT
- Pages that need login redirect to the login page if I am not logged in

### US3 · Browse lectures (Student)
As a student, I want to see all lectures so that I can choose one to rate.
- Each lecture shows its title and teacher name
- I can search by title
- The list is paginated
- A lecture I already rated shows a "Rated" badge

### US4 · Rate a lecture (Student)
As a student, I want to give 1-5 stars and a comment so that the teacher gets my feedback.
- Rating is required (1-5); comment is optional
- I can rate each lecture only once
- The page says my feedback is anonymous

### US5 · Create a lecture (Teacher)
As a teacher, I want to add a lecture so that students can rate it.
- Title is required
- The new lecture appears in "My Lectures"

### US6 · Edit and delete my lecture (Teacher)
As a teacher, I want to change or delete my lectures so that the list stays correct.
- I can edit only my own lectures
- Deleting asks for confirmation
- A student cannot access these actions

### US7 · See results (Teacher)
As a teacher, I want to see the results of my lecture so that I can improve.
- Shows the average rating, total feedbacks, and the count of each star (5 to 1)
- Shows the list of comments with stars and date
- No student name or id is ever shown

### US8 · Role protection (Student, Teacher)
As the system, I want to limit pages by role so that users only do what they are allowed to.
- Students cannot open teacher pages, and teachers cannot rate
- The backend returns 403 for the wrong role

## Data
- User: id, name, email, password, role
- Lecture: id, title, teacherId (one teacher has many lectures)
- Feedback: id, lectureId, studentId, rating, comment, createdAt (one lecture has many feedbacks; unique per lectureId + studentId)