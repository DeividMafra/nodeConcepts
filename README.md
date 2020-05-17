# nodeConcepts
In this repository, I'm showing some basic concepts of node.js using express as HTTP Methods and Parameters, Middlewares, and Automated Tests with Jest.

## Credits: Rocketseat 🚀

# What it should do?

It's five routes simulating a portal where the end-user can create, update, delete a repository as list all created repositories as well and give a "like"/ a "star" for it.

## Routes:

POST /repositories: This router should receive title, url, and techs from the body request. The complete object create is like shown below.

``{ 
    id: "uuid",
    title: 'my repository',
    url: 'http://github.com/...', 
    techs: ["Node.js", "..."], 
    likes: 0 
};``

Ps. using uuid to auto generate universal unique id.

GET /repositories: List repositories.

PUT /repositories/:id : To update the specific repository by id. Only title, url, and techs are enabled to be updated.

DELETE /repositories/:id : To delete the specific repository by id.

POST /repositories/:id/like: To increase the likes quantity.

# Automated tests

### likes.spec.js
- should be able to give a like to the repository;
- should not be able to like a repository that does not exist.

### repositories.spec.js
- should be able to create a new repository;
- should be able to list the repositories;
- should be able to update repository;
- should not be able to update a repository that does not exist;
- should not be able to update repository likes manually;
- should be able to delete the repository;
- should not be able to delete a repository that does not exist;

## All credits and thanks to https://rocketseat.com.br/
