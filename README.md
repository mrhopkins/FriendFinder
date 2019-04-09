# Friend Finder - Node and Express Servers

### https://afternoon-brushlands-45704.herokuapp.com/

## Overview:

FriendFinder is a compatibility-based application -- basically a dating app. This full-stack site takes in results from users surveys, then compare their answers with those from other users. The app will then display the name and picture of the user with the best overall match.

Express is used to handle routing.

## REPLACE GIF WITH NEW RUN THROUGH OF WEB APP
> ![gif](https://j.gifs.com/qjDJE3.gif)

### Instructions

1. Your survey should have 10 questions of your choosing. Each answer should be on a scale of 1 to 5 based on how much the user agrees or disagrees with a question.

2. Your `server.js` file should require the basic npm packages we've used in class: `express` and `path`.

3. Your `htmlRoutes.js` file should include two routes:

   * A GET Route to `/survey` which should display the survey page.
   * A default, catch-all route that leads to `home.html` which displays the home page.

4. Your `apiRoutes.js` file should contain two routes:

   * A GET route with the url `/api/friends`. This will be used to display a JSON of all possible friends.
   * A POST routes `/api/friends`. This will be used to handle incoming survey results. This route will also be used to handle the compatibility logic.

5. You should save your application's data inside of `app/data/friends.js` as an array of objects. Each of these objects should roughly follow the format below.

```json
{
  "name":"Ahmed",
  "photo":"https://media.licdn.com/mpr/mpr/shrinknp_400_400/p/6/005/064/1bd/3435aa3.jpg",
  "scores":[
      5,
      1,
      4,
      4,
      5,
      1,
      2,
      5,
      4,
      1
    ]
}
```

6. Determine the user's most compatible friend using the following as a guide:

   * Convert each user's results into a simple array of numbers (ex: `[5, 1, 4, 4, 5, 1, 2, 5, 4, 1]`).
   * With that done, compare the difference between current user's scores against those from other users, question by question. Add up the differences to calculate the `totalDifference`.
     * Example:
       * User 1: `[5, 1, 4, 4, 5, 1, 2, 5, 4, 1]`
       * User 2: `[3, 2, 6, 4, 5, 1, 2, 5, 4, 1]`
       * Total Difference: **2 + 1 + 2 =** **_5_**
   * Remember to use the absolute value of the differences. Put another way: no negative solutions! Your app should calculate both `5-3` and `3-5` as `2`, and so on.
   * The closest match will be the user with the least amount of difference.

7. Once you've found the current user's most compatible friend, display the result as a modal pop-up.
   * The modal should display both the name and picture of the closest match.

---

## Built with:

- [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) - High-level programming language
- [Node.js](https://nodejs.org/en/) - Open-source run-time environment that executes JS code outside of a browser
- [JSON](http://www.json.org) - Data format
- [MySQL](https://www.mysql.com) - Database
- [MAMP](https://www.mamp.info/en/) - Access to local PHP server and MYSQL server
- [Visual Studio Code](https://code.visualstudio.com/) - source code editor developed by Microsoft

#### npm packages used:

- [express](https://www.npmjs.com/package/express) - A collection of common interactive command line user interfaces
- [mysql](https://www.npmjs.com/package/dotenv) - Node.js driver for MySQL
- [path](https://www.npmjs.com/package/path) - Utilities for working with file and directory paths
- [morgan](https://www.npmjs.com/package/morgan) - HTTP request logger middleware for node.js
- [body-parser](https://www.npmjs.com/package/body-parser) - Node.js body parsing middleware

---

#### Check me out on LinkedIn!

https://linkedin.com/in/matthewrhopkins/
