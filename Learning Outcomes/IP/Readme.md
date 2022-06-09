# IP

## 1. Web application
In the Web application department i have to learn how to make a good program. What that means is that it should be structured naturaly and is somewhat easy to read. 
Atleast easy enough that you dont have to look at documentation everytime you want to change things.
That also means that nothing should be open to interpetation. you cant think that other people should know what you thought about just becasue its logical for you. 
But the opiside is also true. As you dont have to explain everything all the time. you dont have to explain that 1+1 is 2.

At the moment i am starting to get this proces. As i am to delete generic names and use conventional naming and using more spelling conventions in my code by programming language bases.

[Link to where i talk about my code](https://github.com/ThomasPouw/Portofolio-S3/tree/main/Project)



## 2. Software quality
In the Software quality department i have to learn how to efficiantly montitor and secure my code and program. At the moment i havent done any testing.
I am still planning to do that but thing keep popping up that are a bit more important.
But for the security part. I just made the login. It isnt linked yet to anything but atleast there is a start. I am gonna put the responce that Auth0 gives me into a JSON webtoken and use that instead of just leaving the responce as it is. 
in the database will just be the unique id of the Auth0 logged in user.

## 4. CI/CD
With CI/CD we mean **continuous integration** and **continuous deployment** for that we use things like github action for CI and things like Docker for the CD part.
CI/CD now works for both the frontend and the backend. Although the frontend part does not have any testing yet. As there is a problem with karma and looking for the tests.

when it sees a new commit on the master branch it will run the CI/CD. It wont upload the commit to for example heroku if it has an error. As that means that the product is not up to level. And so it would not be smart to upload it to the CD. As for CD your CI needs to be correct. 
In the Backend Test will be happening in the build phase as that is how *mvn clean install* works. And for the static code analysis, it is handeled by sonarcloud directly. As you will be asked which repositories has to be looked at. And because of that you will not find the command to activate the static code review in node.js.yml 

## 8. Professional 
With professionalism we dont just mean acting professional but also doing things like this. Writing this down and doing paperwork. 
As this could help in the future when you or probarbly someone else picks up the project. The have to know what you were thinking on this moment. Thats why doing the paper work is nessesary.
