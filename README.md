# Talkify

## Contributors

- **[tassan](https://github.com/tassan)**

## License

This project is licensed under the **MIT License**.

## Background Context

**Talkify** is a TDD Sandbox Project designed to explore and showcase Test-Driven Development (TDD) principles in a real-world application. The goal is to build a robust and scalable real-time chat system while adhering to clean code and agile practices.

This project is inspired by the work shared in the [Optivem Journal](https://journal.optivem.com/) and the insights of [Valentina Jemuović](https://substack.com/@valentinajemuovic), encouraging developers to adopt and refine their TDD skills. Check out the links for more details and inspiration.

## Use Cases

### Use Case 1: Real-Time Messaging

#### Actors:

- **Primary Actor**: Registered User
- **Secondary Actor**: System (Talkify Backend)

#### Preconditions:

1. The user must be registered and logged into the system.
2. The user must have an active internet connection.

#### Basic Flow:

1. The user navigates to a chat window.
2. The user types a message into the input box.
3. The user clicks the "Send" button or presses Enter.
4. The system sends the message to the recipient(s) in real-time.
5. The system confirms message delivery by updating the chat UI.

#### Alternative Flows:

- **Unregistered User**: If the user is not registered, the system redirects them to the login or signup page.
- **Offline Recipient**: If the recipient is offline, the system stores the message and delivers it when they reconnect.

#### Exceptional Flows:

- **Message Delivery Failure**: If the message fails to send due to a server error, the system displays an error message and allows the user to retry.

#### Postconditions:

1. The message appears in the recipient's chat window in real-time.
2. The message is stored in the database for future retrieval.

---

### Use Case 2: User Authentication

#### Actors:

- **Primary Actor**: User
- **Secondary Actor**: Authentication Service

#### Preconditions:

1. The user must have an account (for login).
2. The system must have access to the authentication service.

#### Basic Flow:

1. The user enters their email and password into the login form.
2. The user clicks the "Login" button.
3. The system validates the credentials against the authentication service.
4. If valid, the user is granted access to the application.

#### Alternative Flows:

- **Password Reset**: If the user forgets their password, they can initiate a password reset via a "Forgot Password" link.
- **OAuth Login**: The user can log in using an external provider (e.g., Google, GitHub).

#### Exceptional Flows:

- **Invalid Credentials**: If the credentials are invalid, the system displays an error message.
- **Account Locked**: If the account is locked, the system informs the user and provides support contact details.

#### Postconditions:

1. The user gains access to the application.
2. A session is initiated and maintained until logout or timeout.
