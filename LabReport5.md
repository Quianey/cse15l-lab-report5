**part 1 -Debugging Scenario**
1. The original post from a student with a screenshot showing a symptom and a description of a guess at the bug/some sense of what the failure-inducing input is. (Don’t actually make the post! Just write the content that would go in such a post)
   
Title: Bugging in StringServer

Catagory: Lab Reports

Hi, I'm working on my lab report 2 on Edstem. I don't know what happed in my StringServer.java. Everytime when I 'm using ```/add-message?s=<string>```, it always returns ```404 no found```.
![image](https://github.com/Quianey/cse15l-lab-report5/assets/147276821/46c715fd-c753-4867-8b2a-3578f809cf5b)
![image](https://github.com/Quianey/cse15l-lab-report5/assets/147276821/1500e02b-69d1-4abe-8817-af092f49fa1e)
![image](https://github.com/Quianey/cse15l-lab-report5/assets/147276821/410a3804-69de-454b-8f14-516930635f50)

I guess there are some bugs in the location of return statement. I think my code actually doesn't go into the if statement of finding path ```/add-message``` and directly return ```404 no found```. 

2. A response from a TA asking a leading question or suggesting a command to try (To be clear, you are mimicking a TA here.)

Hi Qianyi, thanks for the question and the screenshot.I believe the issue comes from your if statement instead of return part. Please make sure that your if statement includes exactly ```/add-message```. In your if statement, you should split the query by ```=```. And your ```parameter[0]```
should be ```s```. 

3.Another screenshot/terminal output showing what information the student got from trying that, and a clear description of what the bug is.
