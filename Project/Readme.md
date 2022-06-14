# Project

## Frontend

For my front end I am using Typescript Angular, the reason behind that is simple. Because I saw the positive representation and decided to look deeper into it. 
When I did that, I saw all the opportunities it would bring. Like Type casting and actual error messages. 
It is also just more fun to use then normal JavaScript as it asks you to really think of how you structure things. Because if things are not clear what type it is it will complain.
And that is what I was looking for. Something that complains but helps me improve my coding abilities. 
That is why I use Typescript. Its JavaScript but more in line with other languages.

The reason why I use Angular is partly because of Typescript. I was planning on using the Typescript version of React. 
But just as a joke I looked at the documentation of Angular. And I just kind of fell in love with it. As it addresses my big problem with React. 
How the folders are structured. A component in Angular has the CSS/SCSS, the html, and the typescript file in one folder, while in other frameworks that would be bad practice and they would be in at least 3 other folders.
I just like the structure more of Angular then other frameworks.

Sadly i can not do everything i planned. As things like Worlds, a levelcreator and 'Roles and permissions' were put on the pile of things that i would not do. As worlds would be useless without a levelcreator and for roles and permissions i would of needed to have a machine-to-machine application. And because of time restrains i just could not do that. 


[Link to my frontend Code](https://github.com/ThomasPouw/TrickingEnigma-Frontend)

## Backend 

For the Backend I am using Java SpringBoot. The reason for it is because I failed my last semester 3 and so I decided to use Java SpringBoot again as I did not do justice to it last time. 
The project is a microservice based ***One***, what that means is that the backend project is actually 3 smaller projects in one. The idea behind microservices is that you can reuse parts of your services for other applications. And in my application you can resonable do that with 2 and maybe with the last one as well. But that is more because Record was made as with the idea that it would need help from the two sides. But for both Level and User they can be used for other applications. As level also includes Sprite and LevelSprite. And User has Nationality.

What i meant with Level, LevelSprite and Sprite is that a level has ofcourse sprites. But you do not want just sprites in your level. As it will just be all on 0,0. As they do not know where they should stand. So LevelSprite is there as a way for sprite to hold a bit more information without touching sprite directly. So now a sprite has a general coords of where it is placed. But also what kind of sprite they are. As you do not want to confuse a Cargo sprite with a End point sprite or even a Wall sprite. But as they are just recolours of each other it just makes sense to put the information of what am i and where am i? in a diffent section from where the sprite is located.

For User its just natural to put in Nationality with it. The reason for nationality existing is actually just to make my game a bit competitive as some countries see each other as there rival, even in the smallest of things. So nationality is just there to make it easier to look up users with a certain nationalities, but sadly because of time restraines that idea got shelved for now. 

[Link to my backend Code](https://github.com/ThomasPouw/TricklingEnigma-Backend)

