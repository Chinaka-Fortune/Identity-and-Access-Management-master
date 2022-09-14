# Coffee Shop

Coffee Shop new digitally enabled cafe for students to order drinks, socialize, and study hard. But they need help setting up their menu experience.

The app shows my knowledge of building APIs with Flask. I implemented Authentication, Authorization and Permissions with Auth0. There are three main users of this web application which are the public, the Barista and Manager. 

The application will:

1. Display graphics representing the ratios of ingredients in each drink.
2. Allow public users to view drink names and graphics.
3. Allow the shop baristas to see the recipe information.
4. Allow the shop managers to create new drinks and edit existing drinks.

The authentication system used for this project is AUTH0. There is a logic to direct a user to the Auth0 login page, managing the JWT token upon successful callback, and handle setting and retrieving the token from the local store. This token is then consumed by the DrinkService and passed as an Authorization header when making requests to our backend. The Auth0 JWT includes claims for permissions based on the user's role within the Auth0 system. This project makes use of these claims using the auth.can(permission) method which checks if particular permissions exist within the JWT permissions claim of the currently logged in user. This determines whether a button will be enabled or disabled on the frontend.

1. [`./backend/`](./backend/README.md)
2. [`./frontend/`](./frontend/README.md)

### Backend

The `./backend` directory contains a Flask server with an SQLAlchemy module. You will need to configure, and integrate Auth0 for authentication.

[View the README.md within ./backend for more details.](./backend/README.md)

### Frontend

The `./frontend` directory contains a complete Ionic frontend to consume the data from the Flask server. You will only need to update the environment variables found within (./frontend/src/environment/environment.ts) to reflect the Auth0 configuration details set up for the backend app.

[View the README.md within ./frontend for more details.](./frontend/README.md)
