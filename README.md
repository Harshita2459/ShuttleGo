# ShuttleGo

ShuttleGo is a website created using the MERN and is focused to provide the University students, the direct access to the University’s shuttle service without any middlemen (teachers, Hostel Wardens) whenever in emergency. It also provides the facilities to the teachers and the hostel authorities to book shuttle through it. 

## Login:-

![Picture2](https://github.com/Harshita2459/ShuttleGo/assets/145472484/a3c6867e-ca36-459d-bab7-8fd9e5d1d6b8)

Login page is the landing page of the website which allows the user to enter the website by providing their user credentials. It uses a form (/login/Form.js). The form helps in taking input of the user credentials store it in the database for further verification of the user data.

![Picture3](https://github.com/Harshita2459/ShuttleGo/assets/145472484/127c2f6c-0277-42a2-838e-87f5d09d1bb6)

##Signup(Signup.js):-

Signup page user a signup form that helps user register himself in order to use the website.

![Picture4](https://github.com/Harshita2459/ShuttleGo/assets/145472484/2e534951-983e-493a-a66f-2cbd07d69441)

### Purpose: This component represents the main sign-up page.

###Structure:

It imports React, the sign-up form component, the Navbar component, and the CSS file for styling.

Renders a div with className "signUpPage" containing the sign-up form wrapped inside a div with className "signUpDivs".

Includes the Navbar component and the sign-up form component within this structure.

## Form Component (Form.js):

### Purpose: This component renders the sign-up form.

### State:

userData: Stores user input data such as name, email, password, phone, date of birth, and role.

rePass: Stores the re-entered password for validation.

error: Indicates if there's any validation error.

errorName: Stores the specific validation error message.

### Functions:

signup(): Performs form validation and sends a POST request to the server upon successful validation.

Structure:

Renders a sign-up form with input fields for name, email, password, re-entered password, phone number, date of birth, and role selection.

Includes error handling for validation errors and displays error messages accordingly.

Provides a "Sign up" button to trigger the signup function.

Offers a link to the sign-in page for users who already have an account.

## Overall Functionality:

The sign-up form ensures all fields are filled and validates inputs such as email format, password length, phone number length, and password matching.
Upon successful validation, it sends a POST request with user data to the specified endpoint.
Users are directed to the sign-in page if they already have an account.

# NAVBAR(Navbar.js):-

![Picture5](https://github.com/Harshita2459/ShuttleGo/assets/145472484/6d83d346-6d43-4133-8182-0e0280b5a366)

## Purpose:
The Navbar component renders a navigation bar at the top of the page.

## Props: None

## Local State:

clicked (Boolean): Indicates whether the menu icon has been clicked to toggle the visibility of the menu items.

## Methods:

handleClick: Toggles the value of clicked in the state when the menu icon is clicked.

## Rendering:

Renders a logo, a menu icon (which toggles the visibility of menu items when clicked), and a list of menu items.

Menu items are rendered dynamically using data from the MenuItems array.

# MenuItems Data (MenuItems.js):

## Purpose:

The MenuItems array contains data for each menu item rendered in the Navbar.

## Structure:

Each item in the array is an object with the following properties:

title (String): Title or label for the menu item.

url (String): URL or path for the menu item.

cName (String): CSS class name for styling the menu item.

icon (String): CSS class name for an icon associated with the menu item.

# Additional Notes:

The Navbar component utilizes React Router's Link component for navigation.

The menu items are mapped dynamically from the MenuItems array, making it easy to add or modify menu items.

# HOME(Home.js):

![Picture6](https://github.com/Harshita2459/ShuttleGo/assets/145472484/7661463d-4ccc-4960-805d-d4b96c53e2f1)

# CODE:-

![Picture7](https://github.com/Harshita2459/ShuttleGo/assets/145472484/2a5a97f0-f8a9-496b-9ecb-efd856b9564f)

## Purpose:

The Home component serves as the main page of the application.

It renders a Navbar, a Hero section, Roles (if the user is logged in), or a message prompting the user to log in, and a Footer.

## Props: None

## Local State:

isLoggedIn: Boolean value retrieved from localStorage indicating whether the user is logged in or not.

# Hero Component (Hero.js):

## Purpose:

The Hero component is responsible for rendering a hero section with an image, title, and text.

## Props:

cName (String): CSS class name for the hero section.

heroImg (String): URL of the hero image.

title (String): Title for the hero section.

text (String): Text content for the hero section.

## Local State: None

# ROLES(Roles.js):-

## Purpose:

The Roles component displays different options based on the user's role.

It fetches bookings associated with the user and displays them if available.

## Props: None

## Local State:

showPopup (Boolean): State to manage the visibility of a popup.

bookings (Array): State to store bookings associated with the user.

![Picture8](https://github.com/Harshita2459/ShuttleGo/assets/145472484/16cd7649-a9e9-4b01-bfae-2148f46e0fe0)

# FOOTER(Footer.js):-

![Picture9](https://github.com/Harshita2459/ShuttleGo/assets/145472484/0b97b8ed-0b59-497d-a60a-60501b0b9f3c)

## Purpose:

The Footer component renders a footer section with useful links and contact information.

## Props: None

## Local State: None

# ABOUT(About.js):-

![Picture10](https://github.com/Harshita2459/ShuttleGo/assets/145472484/83d64568-2fe5-4d45-b596-05e913c9b102)

# STUDENT(student.js):-

## Purpose:

The Student component represents the portal for students in the application.

It displays information related to shuttle bookings for students.

It provides a form for booking a shuttle if the user is logged in as a student.

## Props: None

## Local State:

shuttles (Array): State to store the list of shuttle bookings for the logged-in student.

## Dependencies:

React Router for navigation (Link component).

Navbar component for navigation consistency.

## Lifecycle and Side Effects:

Utilizes useEffect hook to fetch shuttle bookings from the backend API when the component mounts.

The useEffect hook runs when isLoggedIn or role changes, ensuring that the data is fetched only when the user is logged in as a student.

## Rendering:

Renders different content based on the user's authentication status and role.

If the user is not logged in, it displays a message prompting the user to log in.

If the user is logged in but not a student, it displays a message informing them to log in with a student account.

If the user is logged in as a student, it displays the student portal with a heading and a button to book a shuttle.

It also displays a list of shuttle bookings for the logged-in student, showing details such as email, campus, phone number, image, and booking status.

## Additional Notes:

The component fetches shuttle bookings only when the user is logged in as a student, ensuring data security and access control.

Conditional rendering is used to display different content based on the user's authentication status and role.

The component provides a simple form for booking a shuttle, facilitating interaction with the application's functionality.

![Picture11](https://github.com/Harshita2459/ShuttleGo/assets/145472484/443e2082-892c-4530-8fae-71604e80a8fa)

# TEACHER(Teacher.js):-

![Picture12](https://github.com/Harshita2459/ShuttleGo/assets/145472484/6cc74127-aea9-48aa-81c4-b6ec271d3e53)

![Picture13](https://github.com/Harshita2459/ShuttleGo/assets/145472484/94e778e1-5670-480d-a257-b2d6cb39bda6)

# HOSTEL AUTHORITY:-

![Picture14](https://github.com/Harshita2459/ShuttleGo/assets/145472484/2f471015-e21f-41d3-b4b8-8deb6b194774)

![Picture15](https://github.com/Harshita2459/ShuttleGo/assets/145472484/0b4928d9-1ab6-4dbb-be80-e846e08e39a2)

# TRANSPORT AUTHORITY:-

![Picture16](https://github.com/Harshita2459/ShuttleGo/assets/145472484/dd921951-5674-460b-9c63-c6866783173e)

![Picture17](https://github.com/Harshita2459/ShuttleGo/assets/145472484/9fb8fee3-10d8-48fd-879c-786756a74b33)

![Picture18](https://github.com/Harshita2459/ShuttleGo/assets/145472484/9a36b92f-99b2-41bd-b751-15a7e6e26d2e)

## Purpose:

Represents the portal for transport authorities.

Has access to the overall website and adding new shuttle details.

Allows viewing and management of shuttle bookings.

## Dependencies:

React Router for navigation (Link component).

## Rendering:

Displays transport authority portal with a button to add a new shuttle.

Shows login prompt if the user is not authenticated.

## Interaction:

Allows accepting or declining shuttle bookings.

## Additional Notes:

Fetches shuttle booking data from the backend API.

Provides a simple interface for transport authorities to manage bookings.

This website solves the problem of the University students of not able to access the shuttle services directly. It will help them to access the shuttle by directly contacting the transport authority and request for the shuttle whenever in emergency by providing valid proof.
