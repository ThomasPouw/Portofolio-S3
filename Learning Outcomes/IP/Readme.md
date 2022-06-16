# IP

## 1. Web application
In the Web application department i have to learn how to make a good program. What that means is that it should be structured naturaly and is somewhat easy to read. 
Atleast easy enough that you dont have to look at documentation everytime you want to change things.
That also means that nothing should be open to interpetation. you cant think that other people should know what you thought about just becasue its logical for you. 
But the opiside is also true. As you dont have to explain everything all the time. you dont have to explain that 1+1 is 2.

At the moment i am starting to get this proces. As i am to delete generic names and use conventional naming and using more spelling conventions in my code by programming language bases.

[Link to where i talk about my code](https://github.com/ThomasPouw/Portofolio-S3/tree/main/Project)

For design i had some made... ofcourse it changed over time but here is the design as i had it in my head when i first started.
![image](https://user-images.githubusercontent.com/90248008/174053551-8bdbad64-f6e7-4bbe-8b81-c1e2cfea3a7b.png) 

![image](https://user-images.githubusercontent.com/90248008/174053616-9e5d4615-2248-477b-bcc2-f3a3149b4995.png)



![image](https://user-images.githubusercontent.com/90248008/174054166-1f2d2788-07a8-4a65-8b25-78abb7f7cda8.png)

(Unused because of lack of idea how it should work + time)

![image](https://user-images.githubusercontent.com/90248008/174053695-b21d3b1b-7041-46b2-aff4-c257a4b2c5c9.png)

(Unused because of lack of idea of editor + other method of making sprites.) 

![image](https://user-images.githubusercontent.com/90248008/174054244-3c304c07-e8a8-4c3c-a633-cd062ed6f736.png)

(Unused because of SPA does not have access of Roles and Permissions)

![image](https://user-images.githubusercontent.com/90248008/174053899-55395702-ba25-4e56-980a-4cf9fe091711.png)

(Unused because of SPA does not have access of Roles and Permissions)

![image](https://user-images.githubusercontent.com/90248008/174053932-a10999fc-f04d-4a52-b41d-37bd3ebb0823.png)

![image](https://user-images.githubusercontent.com/90248008/174054394-7b43c31b-ca2f-4324-8900-0c2b815cd509.png)



![image](https://user-images.githubusercontent.com/90248008/174054440-2be36650-9de3-4cb3-8856-96573b5eb4b6.png)

Just combined with User

![image](https://user-images.githubusercontent.com/90248008/174054502-50a6ce85-958e-4a6f-b706-c0ef3ed5f723.png)





## 2. Software quality
In the Software quality department i have to learn how to efficiantly montitor and secure my code and program. At the moment i havent done any testing.
I am still planning to do that but thing keep popping up that are a bit more important.
iBut for the security part. I just made the login. It isnt linked yet to anything but atleast there is a start. I wanted to have a whole auth0 system, but sadly because i am using Auth0 single page application i can not use the managment API key and so its almost impossible to do anything with roles as to unlock them you need that key. I know you can get that key with a machine-to-machine application and if i had more time i would off asked somebody to help me setting it up. But sadly because of time restrains it is put on the same pile as worlds and fixing that weird bug where the level will not load correctly. But i do know how Roles and Permissins work as i did a whole research paper about it. 

## 4. CI/CD
With CI/CD we mean **continuous integration** and **continuous deployment** for that we use things like github action for CI and things like Docker for the CD part.
CI/CD now works for both the frontend and the backend. Although the frontend part does not have any testing yet. As there is a problem with karma and looking for the tests.

when it sees a new commit on the master branch it will run the CI/CD. It wont upload the commit to for example heroku if it has an error. As that means that the product is not up to level. And so it would not be smart to upload it to the CD. As for CD your CI needs to be correct. 
In the Backend Test will be happening in the build phase as that is how *mvn clean install* works. And for the static code analysis, it is handeled by sonarcloud directly. As you will be asked which repositories has to be looked at. And because of that you will not find the command to activate the static code review in node.js.yml 

## 8. Professional 
With professionalism we dont just mean acting professional but also doing things like this. Writing this down and doing paperwork. 
As this could help in the future when you or probarbly someone else picks up the project. The have to know what you were thinking on this moment. Thats why doing the paper work is nessesary.

When it comes to talking to teachers/project owners/people that are higher on the hierarcy. I know that i have to respect them and listen to them. 
That does not mean that I should not talk back as sometimes their ideas can be that their idea is not the best in the current situation. 
As in the end I know how much I can do in a certain amount of time. As it is not the best idea to disappoint the project owner just because you said yes to all of the demands of them. So sometimes you have to keep the project owner and you on the same level. Sometimes you have to go higher/lower and sometimes the project owner has to go higher/lower. As a healty relation between project owner and you is a relation with the least amount of fear and the most amount of trust.
