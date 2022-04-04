# History

This project tests deploying an express react app to Heroku

# Instructions to create this project

create react-express folder
cd react-express
mkdir server
mkdir client

npm i -g create-react-app express-server

//create react app
cd react-express/client
npx create-react-app app1
npm run build

//create server app
cd ..
cd server
express

//cut build from client/app1 and paste into server

react-express/server> npm install to get node_modules

in server/app.js add these 2 lines after var app = express();

app.use(express.static(path.join(\_\_dirname, 'build')));

app.get('/\*', (req, res) => {
res.sendFile(path.join(\_\_dirname, 'build', 'index.html'));
});

react-express/server> npm start
head over to localhost:3000 to see react app1

deploy to github. I created a README.md (this file) and did not check create README.md when creating github repo/

Follow tutorial to deploy to Heroku:
tutorial to follow: https://www.freecodecamp.org/news/deploy-a-react-node-app-to/

Link to Heroku website

https://react-express-sl.herokuapp.com/
