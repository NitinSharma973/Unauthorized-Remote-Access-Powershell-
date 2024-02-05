# Unauthorized-Remote-Access-Powershell
## PROJECT DESIGN AND ARCHITECTURE
![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/43b0828f-17e8-4d30-9047-3fa4c88c3481)

## IMPLEMENTATION
Running Powershell Empire:
First we make a Empire server that store a information of service are currently listening on my local machine which the help of powershell-empire server command.
       
  ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/d5b48947-bdc3-4c36-b16d-90a4ec4a2546)
                                                                
After that we make client that interact with server with the help of powershell-empire client command .After that when we  start Empire, it will display a message as shown below.
On completion, Empire will show the following screen as shown below.
 
  ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/b8aee0a7-5cd3-47aa-86c4-f79a8cb94ea2)
                                                               

With the help command , which will display the help menu as shown below.
 
                                                          
![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/33c828fb-575d-462a-95c2-eba900cfea7b)


### Using Listeners:
Now we move to listener management menu by typing command listeners as show below. we can see itssub menu by codifying the help command. Let's take a look at what each command will do.
 
![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/8f411762-31c3-431f-952e-831c7610fbc3)
                                                             
agents- Will allow us to jump to agents menu empire.
back & main – Will take  back to the main menu of empire.
exit – Will  help in exit from empire.
help – Will display help menu.
info – Will display information about the active listener on machine.
kill – Will kill a particular listener at is generated.
launcher – Used to induce an original launcher for a listener.
list – Will list all the active listeners on the machine.
usestager – Used to use a stager.
uselistener – Used to start a listener module in empire.
Every listener required certain options to be set .The set command is used to assign these values. Similarly the unset command is used to clear these value.
When all options are set , then we start a listener using execute command.


 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/f3238d93-fc1a-4536-8464-493f28923e87)

                                                        

Once we go back to main menu , we can see that our listener is currently active.




### Using Stagers:
The stager can be accessed using the usestager command as shown below.
 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/b4878617-d529-43cc-a46b-b64eff3716de)
                                                                    

Then we type usestager windows/launcher_bat command to load the stager. With the help of help command we can look at stager menu as shown below.

 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/ea627ed3-f701-48bf-8986-d4ff9add2243)

                                                                  
agents- Will allow us to jump directly to agents menu of empire.
back & main – Will take us back to the main menu of empire.
exit – Will exit from Empire.
help- Will display help menu.
info- Will display information about the active listeneron the machine.
kill- Is used to kill a particular listener on active machine.
execute or induce – Will execute or induce the stager.
interact – Is used to interact with a particular agent in victim pc.
list- Will list all the active listeners or agents on host machine.
options- Used to see all the options we need to set for the particular agent.
listeners- Used to jump to listeners menu.

Then we need a set listener in order for stager to able to communicate with empire. Using set Listerner command we set listener and then type execute command to generate a stager.
 
 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/84c77591-0aa7-43be-b2c2-786f4d10e93e)
                                                                    
After execute command we successfully make a launcher.bat file in a attacking machine as shown in below. 
       ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/7e57d7ce-91de-475c-807e-a121e896cab1)

Then we need to move  this file to apache server so that this file can be download  form any where to  make a connection with attacking machine.
Now we move this file to server as shown below using sudo mv command.

 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/a1d67dc4-4137-4320-8cbf-080d83c71321)

                                                                
To gain access of remote we deploy a website on Netlify so that this payload download from this site to victim pc. 
 
  ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/5f13f943-ef1f-4565-9f2b-a09fb0cf8f69)
                                                               
On click the login Button of this website payload will be automatically download in victim pc as shown below.
 
  ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/83838ebd-7cc2-4146-9eaa-a13456de45d6)
                                                           
![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/3e431644-87c8-4037-a859-6aed42d2bfce)

### Using Agents:
The agent menu  can be accessed using agent command as shown below. But , as it started , we do not currently have any agents registered.
 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/e72a6ae9-97fa-42f3-9f62-6eb313619344)

                                                               
 When a user of victim  double click on the payload then we get access of remote pc. Now using list command we will see all the active agents we have shown below.
 
  ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/dcee345a-c117-4547-a8b0-83be43d6926c)
                                                          

Using Modules:
Modules in empire are used to perform specific functions in remote pc. We can access modules using a usemodule command as shown below.

  ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/30ccd4e2-358b-4551-9ca5-841506dd1036)

                                                        
Now we type usemodule external/generate_agent to load the module. Once a required module is loaded we used help command to show all details about the module as show below.
  ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/2c1d1140-4b10-4b9c-8f03-e42370f5c6af)
                                                                
Now we used a set command and when complete use the execute command to generate  the module and we get a session id as shown below.


![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/820f1c65-385e-4b13-a697-b0629455bac2)

![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/a40bb9eb-606d-4654-94ad-072909b70448)


## KEY CHALLENGES
Detection by Security Tools:
Security tool  such as antivirus software and intrusion detection systems are becoming more adept at identifying and blocking powershell based attack. Powershell empire may be detected by security solutions and  reducing its effectiveness.
 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/1dc42d90-52fb-4c87-ae05-3280f851f09d)

                                                                      
Continuous Updates and Patches:
Organization regularly apply security updates and patches to mitigate vulnerabilities. PowerShell Empire's effectiveness may diminish as system are updated and vulnerabilities are addressed.
Risk of Exposure:
Using PowerShell Empire carries a risk of exposure. If the tool is not used carefully or if there are mistake in the testing process, there is a risk of unintentional harm or data breaches or disruption to systems.

 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/79456a5a-5227-4f02-bd31-9bf11e063454)

                                                                    



No Guarantees of Success:
The success of using powershell empire depends on various factors which including the security posture of the target environment, the awareness of the defenders  and the specific tactics employed by the attacker. Success is not guaranteed.

 ![image](https://github.com/NitinSharma973/Unauthorized-Remote-Access-Powershell-/assets/89895011/eda6a691-8ef8-4672-be79-bd503caf4e70)

                                                                

