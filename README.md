# Talk Proposal Generator

The Talk Proposal Generator is a web application that helps you generate engaging and effective talk proposals for your next conference. Our tool uses AI to help you create professional proposals based on your inputs.

## Features
- Three types of talks: Choose between a 30-minute talk, a 60-minute workshop, or a 10-minute lightning talk.
- Custom proposal based on your ideas: The application takes in your ideas and generates a proposal tailored to your needs.
- Conference selection: Tailor your proposal to the conference you're planning to attend. The current options include PyCon US, PyCon AU, and SciPy.
- Feedback system: After generating a proposal, you can provide feedback to help improve the system.
- User login functionality: This application implements user authentication.

## Installation and Setup
1. Clone this repository.
2. Install the dependencies using pip install -r requirements.txt.
3. Set the GOOGLE_CLIENT_ID and GOOGLE_CLIENT_SECRET environment variables for Google OAuth. Set the OpenAI API key environment variable as well.
4. Run the application using the command python app.py.

## Database
The application uses SQLite for its database. The database consists of a user table with fields for id, name, email, and profile_pic. The database is initialized with the init-db command that clears the existing data and creates new tables.

## User Authentication
The application handles user authentication via Google OAuth. It sets up a user session and manages it with Flask-Login. It also retrieves a user from the database. Users can log in at the /login endpoint, which redirects them to Google for authentication. Upon successful authentication, Google sends back an authorization code to the /login/callback endpoint, which then retrieves the user's profile information from Google, verifies their email, and logs them in​4​.


## License
This project is licensed under the MIT License. See the LICENSE file for details.
