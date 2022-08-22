# node-js
===========================================================================================================
Major topics : -
1] what is node js
2] how it works
3] install and run 
4] make basic api
5] use with express.js
6] ui with node : ui event, forms , web pages etc.
7] node js events 
8] middleware
9] major package
10] connect with db
11] make major api
12] api validation
13] interview question.
===========================================================================================================
[1]                    what is node js
* diff. between node js and js :
    - node js is not language 
    - node js connect with db , js cannot connect with db
    - js run in browser thats why its not connect with db
    - node js is present on server and db also present in server thats why node js connect with db.
    - node js and js code and syntax is similar
    - node js is free and open source (we can contribute in code ).
    - node js use chrome v8 engine for run.
    - v8 engine is fastest server side enviorment for api.

[2]                  why do we use node js
    - is mostly use for making api , but it also use for making website.
    - we can also use java , php , python for making api.
* why make api ? 
    -> mobile application ( react , angular , webapps etc) it can't be connect directly  with db , it run on browser or mobile . so for making connection between application and data  , api are created.

    - with node js and js , you can become full stack developers.

[3]             History  and More 
    - first release : may 27 2009
    - written in c , c++ , js


[4]         Basic theory of node js
    - what are client side and server side in web  development?
    - where do we use node js ( client side or server side)
    - how node js use js
    - what developer make with node js in compeny

    (1) Client side and server side :-
        - whenever we search on internet there are two machine envolves , server side and client side .
          we send request to server using client side and the server respose with data . 
        - 2 types languages : server side (node js , python , php) and client side ( js , html, css)
        . The communication for data is make through api between server side and client side.
    
    (2) How node js use js :-
        - js are execute in chrome browser. 
        - using v8 engine chrome execute the js
        - v8 engine take the code and give result to the browser.
        - node js developer add v8 engine in node js thats why js also run in server side . 
          so using node js and js we can make full stack developer.
        - v8 engine written in c++

    (3)  what developer make with node js in compeny
        - generelly node js developers make api with node js
        - using this api we can connect server side to client side
        - node can make api for web android and ios etc. ( api are same for all) 
        - we can also make website using node js

    (4) Install and setup node js 
        - Download node js : www.nodejs.org -> download recommended for most user version
        - install npm  and node
        - check instlall version of node js :-{ node -v }
        - check instlall version of npm :-{ npm -v}
        - use code editor ( vs code etc.)
        - run .js file in vs code : {node .\a.js}
    
    [5]         First script programm with node js
        * how can use node js with command prompt
        - we don't need to any specific folder to run node js 
         we can run node js  from any folder bcoz node js is globally install.
        -when statement doesnt return anything its give undefined in console.
    * how to pass data from one file to another in node js
        EX.- node js module install from a.js to b.js
            a.js :- 
            module.exports={
                x:10,
            }
            b.js :-
            const a= require(./a); 

        - we cannot use export ,emport directly like js bcoz node js is lower version than js.
        may be in future version we can use.

[6]        modules in node js
    (1) types 
        - modules are two types 
        - core modules -> global and non global  
        - external modules
        {1} core modules : in every lang there are some basic feature available for connecting with db , createing files , code process , api calling  etc.   this features is called core modules.
        eg. console , fs , Buffer , HTTP 

        - Global modules : module that does not need to import . eg. console etc.
        console.log(__dirname);  // it prints the current directory name (path)
        console.log(__filename);  // it prints the current file name

        - non-Global modules : module that need to import 
        eg. 
        const fs= require('fs');
        fs.writeFileSync("hello.txt", "msg");  // function present in filesystem modules use for creating
                                                                      file  pass (file name.type , msg).
          const fs= require('fs').writeFileSync;
          fs("hello.txt", "msg");        // work same as above code

[7]         Make basic server output on browser
        - for making server firstly need to install http modules 
            const http = require("http");
        - http.createServer( (req, resp) => {            // createServer function take callback functionff-+
             resp.write("hello")); // it print hello on browser
             resp.end();              // responce must be end 
        }
        ).listen(4500);

        - http.createServer(funcitonname).listen(4500)  // we can also write this 

        - http.createServer() pass the callback function 

[8]         All about package.json
        - ------------what is package file--------------------
        - it takes details of our projects ( version , name , depository , package , command )

        ------------- how to make package.json--------------
        - to install package.json type command : {npm init}         
        - npm(node package manager) , init(initilizer)

        ------------install package ------------
        - {npm i packagename}             ( it install package)
        - all packages all present in node modules folder
        - if node modules folder delete , we can install using {npm intall} command 
        - used package present in dependencies in pakcage.json
        - package-lock.json    ( it takes all details regarding the install packages)
        - node js is a single thread .
        - signle thread means one time only one command will be run.
        - .gitignore file used for file which we dont want to push on github.
        - node modules folder we cannot push on github

[9]    Nodemon  ( time saving modules )
        ------------what is nodemon package------------
        - without nodemon package we want to run code each time when we do any changes in code , it is time wasting process.
        - nodemon package continusly run our project , we dont need to run each time when we do some changes in code.
        - install nodemon package : { npm i nodemon -g }     -g means it install globally
        - use nodemon {nodemon .jsfilename}

 [10]   make a simple API
        - make a server :
        const http =require("http");
        http.createServer( (req,resp)=>{

        } ).listen(6000);
        - create header and api body
        - create an api with static data
        - put data in another file

[11]    http header
        - if the response from the http server want to desplay as html , you should include an http header with the correct content type.
        - syntax : resp.writeHead(200, {"Content-Type" : "text : html"}); 
        - it takes 2 argument status code and content type
        - status code 200 means all is ok , second argument is the object containing the response header.
        - status code 404 means data is not getting.
        - status code 500 means error in server.

[12]    Input from command line 
        - {process.argv}          : show all input 
        - {process.argv[index]}   : show specific index input
        - fs.writeFileSync()  : write /create file
        - fs.unlinkSync()     : remove file

[13]    - Show file list
        - make file in a folder
        - use path module
        - get file name and print

        - create file :
        eg. const fs= require('fs')'
            fs.writeFileSync("apple.txt","this is a apple fiel");
        - create file in folder : { const path = require('path');}
[14]    - CRUD with file system
        = create file : fs.writeFileSync("hello.txt", "good morning");

[15]    - synchronous and asynchronous 
        - in synchronous opeation tasks are perforemed one at a time
        - in asynchronous opeatio second tasks do not wait to finish first taks.
        
[16]    Express Js
        - install : { npm i express}
        - path module is used to acces folder

[17]    Template Engine
        - using it we can make dynamic pages.
        - before use it , we need to install this like npm pakcage
        - for using template engine we need views folder

[18]    mongodb in node js
        - 
