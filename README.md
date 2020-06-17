# remo-coding-challenge-1
- Fork this repo to your account
- Run `npm install`
- If you are planning to use firebase, create a firebase project and add your config in `src/services/firebase`
- Sample express server is added within this repo. Run `npm run start-server` to start the server in port `8000`. 
- This server contains sample get and post requests and will be called in Login page from browser (Component: Auth.tsx)
- You are free to use either server and/or firebase for state management
- Run `npm run start` to start the server. This will open the landing page with login option

## Requirements
- Use google login/email login to authenticate user
- This app has 2 routes (`/` and `/theater`)
- Convert the route `/theater` as authenticated i.e. user can go into this page only if he/she is logged in
- Theater page
  - This page will have a conference map with tables as below
  - Once user is authenticated, users will be redirected into this theater page
  - Create table DOM elements by accessing `tables` from the `TableConfig`. `first-table` is added as example. `19` tables are present in the configuration
  - Users can go into any table and their avatars will be shown as below.
  - Assign a table to the user when they land on this page
    - Assignment logic
      - Loom video: https://www.loom.com/share/1b07226e01fe44ca9b9b52899ce8ebb8
      - First user will go into first table, second user will be paired with first user in first table
      - third user will go into second table and fourth will be paired with third user in second table
      - once all the tables have 2 people, next incoming user will go into first table and then second and so on
      - Once all the tables have 3 users, next incoming user will go in first table and then second and so on
      - Users can switch table at any point of time
  - User should be able to switch tables by double clicking on the table
  - If user refreshes the browser at any point of time, they should land on same table
  - At any point of time, one user can be in only one room
  - Max allowed in a table should be configurable ranging from 3 - 6
  - When a table is full and new user tries to enter, show error

- Functionality testing (Bonus)
  - How to test this feature in mass scale?
  - This conference map can have 100 people max. How as a developer can you test this with max capacity?