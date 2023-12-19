#JavaFrameworks 
!!! ZIE OOK: js_angular_guard_login.html
![[js_angular_guard_login (1) 1.html]]

Auth: Token?
- No? => Login page
- Yes? => Route: logged in => /users\[auth]
token wordt opgeslagen in de localstorage
=> De check wordt uitgevoerd met de server voor overenkomst enzo

Guards => Class die de "CanActivate" interface implementeren
1. **AuthGuard:**
    - The `AuthGuard` is a common type of guard used to protect routes that require authentication. It checks whether the user is logged in or not.
    - If the user is authenticated, the guard allows access to the requested route. If not, it may redirect the user to a login page or prevent access.
      
2. **Route Protection:**
    - Guards are typically applied to specific routes in the Angular application’s routing configuration. You specify which guards should be executed for each route, determining if the user can access it.
      
3. **Login Component:**
    - This is the component where users enter their credentials to log in. After successful login, the authentication service updates the user’s status, indicating that they are logged in.
      
4. **Authentication Service:**
    - The authentication service is responsible for managing the user’s authentication status. It typically provides methods like `login()`, `logout()`, and `isLoggedIn()` that the login component and guards use.
      
5. **Router Events:**
    - Angular’s router emits events during navigation. Guards can subscribe to these events, allowing dynamic decision-making based on the navigation state.
      
6. **Redirects:**
    - When a user tries to access a protected route without being authenticated, guards can redirect them to a login page or another appropriate location.
      
7. **User Authentication State:**
    - Guards often rely on the authentication state stored in the authentication service. This state could be a simple boolean flag indicating whether the user is authenticated or more detailed information about the user.
    
8. **Lazy Loading and Feature Modules:**
    - In larger applications, guards are crucial when working with lazy-loaded modules. They ensure that the necessary conditions are met before loading a module, protecting sensitive sections of the application.

[[Hashing]]
