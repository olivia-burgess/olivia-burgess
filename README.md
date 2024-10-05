```md
 .+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+. 
(       __        __   _                          _           )
 )      \ \      / /__| | ___ ___  _ __ ___   ___| |         ( 
(        \ \ /\ / / _ \ |/ __/ _ \| '_ ` _ \ / _ \ |          )
 )        \ V  V /  __/ | (_| (_) | | | | | |  __/_|         ( 
(        __\_/\_/ \___|_|\___\___/|_| |_| |_|\___(_)          )
 )      |_   _|__    _ __ ___  _   _                         ( 
(         | |/ _ \  | '_ ` _ \| | | |                         )
 )        | | (_) | | | | | | | |_| |                        ( 
(         |_|\___/  |_| |_| |_|\__, |          _              )
 )       _ __   ___ _ __ ___  _|___/ __   __ _| |            ( 
(       | '_ \ / _ \ '__/ __|/ _ \| '_ \ / _` | |             )
 )      | |_) |  __/ |  \__ \ (_) | | | | (_| | |            ( 
(       | .__/ \___|_|  |___/\___/|_| |_|\__,_|_|             )
 )      |_|__   ___  _ __| |_ / _| ___ | (_) ___             ( 
(       | '_ \ / _ \| '__| __| |_ / _ \| | |/ _ \             )
 )      | |_) | (_) | |  | |_|  _| (_) | | | (_) | _ _       ( 
(       | .__/ \___/|_|   \__|_|  \___/|_|_|\___(_|_|_)       )
 )      |_|                                                  ( 
(                                                             )
 "+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+"+.+" 
```
# Todos App
This app began as an assessment project for React forms, but I found it so enjoyable that I continued working on it. I’ve incorporated Shadcn and Tailwind for styling, which allowed me to create a visually appealing interface while letting me focus more on front-end logic, which was one of my main goals.

### My Learnings:
* **Component Libraries:** I’ve learnt a lot using Shadcn in this project, and the customisation of it. Some components I utilised are data table, button, form, dropdown menu, and more.

* **Working with Dates:** This is my first time working with dates. The database stores dates in ISO 8061 format, but on the front end, I convert them to a locale string for display. When submitting or updating dates, they’re converted back to ISO 8061 before being sent to the API. I encountered an interesting issue regarding the `typeof` due date. Since a todo can be created with or without a due date, the date can be a string or undefined on the front end. However, Knex ignores undefined values, which caused the date update request to be skipped. The Shadcn component only accepts undefined for no input, so I solved this by converting undefined to null when sending the date to the backend. In my interface, `dueDate` can now be a string, undefined, or null.

* **Data Sorting:** Sorting data presented a interesting learning experience. Although I could sort the data by due date on the initial database query, it wasn't ideal for client-side re-sorting. For instance, if the data was already sorted by `dueDate` asc, the first click on that column would to sort it the same way, only on the second click it would be desc. For all other columns the first click would sort asc. To solve this, I removed sorting from the db query and utilised sorting on the front end, with props from the Shadcn data table component to manage it.

* **Component Structure:** I’ve worked on splitting my components more efficiently and passing props to ensure modularity and reusability.

# Pet Bet
This app was part of a teacher-led project at Dev Academy, where I was part of a team of six. I paired with another student to work on the project, while our facilitator acted as the product owner and agile facilitator. We received tickets with brief descriptions of the requirements and a wireframe, leaving us to figure out the solutions. It was an incredible project to work on, and I had a great experience collaborating and problem-solving with the team.

### My Learnings:
* **SQL Querys:** I gained a valuable insight into what can be achieved through database queries versus front-end calculations. For example, one of our tasks was to display a win/loss ratio on the leaderboard, and we were using Knex for our backend. Knex doesn't provide a method to calculate the ratio in the query. After researching, I found two possible solutions: 1) use SQL within the Knex query or 2) calculate the ratio on the front end. I consulted with our facilitator, who encouraged me to give the first option a try. This experience was a great learning opportunity, it showed me how much more is possible on the backend when you go beyond Knex.

* **Implementing Auth0:** We had just learned about Auth0 the week before starting this project, and I wasn’t completely confident with it yet. My pair was assigned the task of implementing Auth0, and this experience really helped solidify my understanding. I learned more about the various objects and methods available, such as user.name, loginWithRedirect, and logout, as well as how to conditionally render components based on authentication status and protecting routes on the backend.

* **React Forms:** For this ticket, I worked on it solo, coding in the morning before the presentation. While the styling isn't finished, the functionality is fully working. This experience really helped me solidify my understanding of React forms and made them feel less overwhelming. My facilitator navigated with me to complete the final parts of the form and taught me valuable lessons about using the spread operator and `useNavigate` from `react-router-dom`. Although it isn’t styled, I’m proud of getting it to work and delivering a functional result under pressure.
