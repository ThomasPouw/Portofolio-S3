# IP

## 1. Web application
In the Web application department, I have to learn how to make a good program. What that means is that it should be structured naturally and is somewhat easy to read. 
At least easy enough that you do not have to look at documentation every time you want to change things.
That also means that nothing should be open to interpretation. you can’t think that other people should know what you thought about just because its logical for you. 
But the opposite is also true. As you do not have to explain everything all the time. you do not have to explain that 1+1 is 2.

[Link to where I talk about my code](https://github.com/ThomasPouw/Portofolio-S3/tree/main/Project)

For design I had some made... of course it changed over time but here is the design as I had it in my head when I first started.
![image](https://user-images.githubusercontent.com/90248008/174053551-8bdbad64-f6e7-4bbe-8b81-c1e2cfea3a7b.png) 

![image](https://user-images.githubusercontent.com/90248008/174053616-9e5d4615-2248-477b-bcc2-f3a3149b4995.png)



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

There was also some research done. I researched both "Colour Psychology" and "Roles and Permissions". Sadly, the Roles and Permissions one is a bit wasted because of the whole Single page application vs Machine to Machine Auth0 situation. But even still, if I have to redo anything at least I got a personal reference point now, in my own words that I can understand.

But on the topic off things I could not do, I think that the main idea that I had is done. But sadly, the details are missing. As the pieces are not completely aligned. As for example the 4-block piece is a bit longer than 4 blocks making it so that no other piece can get past it if it is a 5 wide/height space. Also, the idea of the level editor sadly had to be scrapped. They are for the sprite editor also got onto the chopping block. What I mean by this is that although I am proud of what I did, it is sadly not everything I wanted to do.



## 2. Software quality
In the Software quality department, I have to learn how to efficiently monitor and secure my code and program. 
But for the security part, there is the auth0 login page and that is about it. I wanted to have a whole auth0 system, but sadly because I am using Auth0 single page application I cannot use the management API key and so it is almost impossible to do anything with roles as to unlock them you need that key. I know you can get that key with a machine-to-machine application and if I had more time, I would off asked somebody to help me setting it up. But sadly because of time restrains it is put on the same pile as worlds and fixing that weird bug where the level will not load correctly. But I do know how Roles and Permissions work as I did a whole research paper about it. 

For testing I did unit testing as it the base version of testing. It is what happens before tests like integration testing and system testing. Unit testing are very easy to do as you just test certain parts. And even though some things like components look like integration tests as they involve parts of the program you already unit tested, but it does not have any hierarchy type testing. So, nothing goes before the other. Every test can do their own thing at their own time. But some parts still involve other units of the program. At the table alone you need to ask three parts of the store. the User part, the Nationality part, and the level part. And to make those part you need multiple methods. That work together to get the information from the backend to the frontend. Of course, that is how it usually works, but while testing I block the sending of the URLs and just put the information it needs into the state.  But you can still not call it an integration tests, because of the flat nature of my testing. But I did do a lot of unit testing. Over 100-unit tests have been written and successful. from that 72 are from the frontend and 28 are from the backend. The reason for that big different is because there was just more to tests in the frontend as the backend is technically just a highway to the database. And, because the store of the frontend needs to be tested and just like I said it involves a lot of different kinds of methods just like I just said. for the nationality part of the store alone there are 12 tests. And you can see that part as one of the smaller parts of the store. As it only interacts with itself and user. Or at least within the borders the files. to access the tests, download the frontend files and then type "npm test" in the terminal. It will start testing. 


## 4. CI/CD
With CI/CD we mean **continuous integration** and **continuous deployment** for that we use things like GitHub action for CI and things like Docker for the CD part.
CI/CD now works for both the frontend and the backend. Although the frontend part does not have any testing yet. As there is a problem with karma and looking for the tests.

when it sees a new commit on the master branch it will run the CI/CD. It will not upload the commit to for example Heroku if it has an error. As that means that the product is not up to level. And so, it would not be smart to upload it to the CD. As for CD your CI needs to be correct. 
In the Backend Test will be happening in the build phase as that is how *mvn clean install* works. And for the static code analysis, it is handled by SonarCloud directly. As you will be asked which repositories has to be looked at. And because of that you will not find the command to activate the static code review in node.js.yml. The reason why I chose SonarCloud is quite simple. By recommendation. As I heard that SonarCloud was easy to set up, free and reliable. Even then I was a bit careful and looked around at other choices. But in the end, I just chosen SonarCloud. The reason why it is automated is actually pretty funny as I did not know it did that. But in retrospect it does make sense as I did give it permission to look into the two repositories. 
The Docker for the backend is split into 3. That is because if you put it together 2 will not open without a special script. And to show how these 3 Services can work without knowing of each other’s existence I made it so that it just put in 3 docker repositories. It also fixes the problem of ports nicely as it just reads what port to expose. 

Sadly, there will be no frontend CD as there is a bug in either TypeScript/Angular or its just web development. Where it makes it so that the interface called *offscreencanvas* will not be seen by anything. And that interface is important as Pixijs uses it and Pixijs is the library that controls the board. The error only happens when you build as you must change the file in typescript/lib called lib.dom.d.ts and put in this just under the definition of HTML Element. https://stackoverflow.com/questions/50831981/how-to-use-offscreencanvas-in-typescript-project ![MicrosoftTeams-image (4)](https://user-images.githubusercontent.com/90248008/174430026-87e64cdf-4f64-4228-a2bb-0c0494cd16a4.png)

Of course I talked with the teacher about it and after talking to him in the evening he said that I could stop trying to fix it as it will not change anything anymore as it is just broken. 
![image](https://user-images.githubusercontent.com/90248008/174430074-fab41700-aed1-4d14-ba90-d801607bb1af.png)
![image](https://user-images.githubusercontent.com/90248008/174430113-6422f866-137d-469e-b223-fc9a7612f9c2.png)


## 8. Professional 
With professionalism we do not just mean acting professional but also doing things like this. Writing this down and doing paperwork. 
As this could help in the future when you or probably someone else picks up the project. They have to know what you were thinking on this moment. That’s why doing the paperwork is necessary.

When it comes to talking to teachers/project owners/people that are higher on the hierarchy. I know that I must respect them and listen to them. 
That does not mean that I should not talk back as sometimes their ideas can be that their idea is not the best in the current situation. 
As in the end I know how much I can do in a certain amount of time. As it is not the best idea to disappoint the project owner just because you said yes to all the demands of them. So sometimes you have to keep the project owner and you on the same level. Sometimes you have to go higher/lower and sometimes the project owner has to go higher/lower. As a healthy relation between project owner and you, is a relation with the least amount of fear and the most amount of trust.

Sadly, I still have a self-confidence problem so talking can be a bit problematic at times. As I am a bit scared of what the other person thinks off me. Even if I already know that everything is fine. But I already knew that "solving" that was not really going to happen in one semester. As my confidence problems are rooted in my inability to understand what others are thinking sometimes, or so I think.
