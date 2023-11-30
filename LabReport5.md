**part 1 -Debugging Scenario**
1. The original post from a student with a screenshot showing a symptom and a description of a guess at the bug/some sense of what the failure-inducing input is. (Don’t actually make the post! Just write the content that would go in such a post)
   
Title: Bugging in StringServer

Catagory: Lab Reports

Hi, I'm working on my lab report 2 on Edstem. I don't know what happed in my StringServer.java. Everytime when I 'm using ```/add-message?s=<string>```, and then ```/increment```, the next call of ```/add-message?s=<string>``` becomes ```n+2.<string>``` instead of ```n+1.<string>```. 
![image](https://github.com/Quianey/cse15l-lab-report5/assets/147276821/915db010-a360-4403-96e3-3d17d9eb4243)
![image](https://github.com/Quianey/cse15l-lab-report5/assets/147276821/117a9428-6896-453a-8755-a63ef2d490db)
![image](https://github.com/Quianey/cse15l-lab-report5/assets/147276821/3c515d2c-8c5c-4838-9b46-57de635556d3)
![image](https://github.com/Quianey/cse15l-lab-report5/assets/147276821/2ac3c7cc-60c3-411a-b1dc-e8cfc6e390d2)





I guess there are some bugs in ```else if (url.getPath().contains("/add-message")) {```. I think this statement is reached even though I called ```/increment```, which means ```/increment``` and ```/add-message?s=<string>``` are called at the same time. . 

2. A response from a TA asking a leading question or suggesting a command to try (To be clear, you are mimicking a TA here.)

Hi Qianyi, thanks for the question and the screenshot.I believe the issue comes from your counter of the method. In your code, the ```/increment``` and ```/add-message?s=<string>``` share the same counter ```num```. Thus, to solve the bug, you need to separate them. One way is to 
create another counter for ```/add-message```. 

3.Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is.
