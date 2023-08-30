![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/ef19f594-c923-410f-8a62-5c44b533a6b1)# TCL_Workshop_Basic-to-advance
#TCL_scripting #VSD_learning #verilog #VLSI #Verification #YOSYS #Opentimer #Scripting_language

TCL Workshop_5 DAYS: Learning from  Basic of TCL basics to Advance Scripting Techniques in VLSI. IN this workshop we are going to learn to build a user Interface which will conver the constraits in .csv file to sdc format. With help of Tools Yosys and Opentimer, This user interface will generate a detailed report of the synthesized netlist and prelayout timing report.
TCL is widely used in VLSI industry for processing synthesis results, timing reports, automate the physical design flow such as floorplan, placement, and routing. 
Tcl stands for Tool Command Language. A command follow the instructions given and generate output as example, output a string, compute a math expression, or display a widget on the screen.

This strong language can creäte everything into the frame of a command, even programming constructs.
First understand the task and then break it to the many subtasks to learn step by step and generate the detailed report, which will be our Final output of the task. 

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/daeeb09f-1bcc-43b7-bfbb-ece2eb4332a3)

First Task:  
Create a command TCLbox(any name) and .csv file from UNIX shell to TCL script. 
This task has three scenarios to run here which are included in this first task to create a command the TCLbox and work on .csv file
Three scenarios are here given below to understand the user behaviour in different mode.

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/69e780c4-59f9-48c9-8391-603631d3a4c3)

First scenarios when user do not provide the .csv file:

screenshot is given below:

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/42f1aadd-1cd2-414b-9d40-2c0a2c644cd6)

Second scenarios when user give wrong  .csv file which does not exists:

screenshot is given below:

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/2e28991f-e645-4e3c-96ce-23236d3e2daa)

Third scenarios when user ask for help to know more about the usage:

screenshot is given below:

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/f2af7b74-80bc-4428-89d4-663d9ad5be58)

Second Task:
First Task has completed than second Task is to Convert all inputs to format [1] &SDC format, pass to synthesis tool ‘Yosys’. To complete this task we need to break down the task into subtask and deep dive into the learning skill mode.  Tasks are mentioned one by one here in the snippet to achieve the final outcome of this task.

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/68c95ac5-a03c-42b2-9cda-5f978c3b8f31)

First subtask is to creat the varibales and convert all the information available into the excel sheet. and make a matrix to make things more simpler and proceed further to create variable. 
Lets understand with help of screenshot than perform the task on VM>, with completion of the task,it will autocreate the variable. 

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/27004ff0-361f-46b0-8097-7a4e408c20f3)

Now Perform the task on the VM and create variables.give command ./TCLbox openMSP430_design_details.csv
here is the outcome of the  performing task on VM.

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/5eb76eab-33fc-488b-a7e6-8dbca88589ca)

Now checking the existence of files or not. second subtask is to check the all files are existing in the directory or not. With code adding in the tcl file, task has performed on  the terminal and screenshot for the same is given below.

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/a6843d5c-ea73-4e2f-908b-d44a29e9bb83)

on the way to Processing of the constraints openMSP430_design_constraints.csv file here, we have put some puts command to find out the results and data avaiavle in the constraints.csv file. here we have put the return in the scipt to stop at that point and show th results after that we will match this data to the orogonal file existing in the directory. 

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/c7feca7c-8e83-48aa-bc51-8ada6b12a476)

If we check and open the constraints file, given below snippet here.the given columns and rows are matching here.Clocks[rows,coulmn] are starting from zero
Inputs starting from the row 4
outputs starting from the row 27

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/23304ef5-9cd3-41fe-9af6-1d8c33c32b63)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/de62b37b-1e0e-4b88-913f-a7f2dc7ebfe8)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/29b0b05a-20ce-4039-a2a0-a0491dc314a1)

Third task:
convert the format[1] & SDC formgat to the format[2] and pass to timing tool Opentimer tool.
first look at this blue box and the position of the coulumn here which need to convert into the standard format data.Process the clock and inputs and dump into the .csv file. Now understad the clock latency and  work our algorithm to convert this to Industry standared format which is the SDC format
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/17735390-074e-4d8e-8f7c-78debbc7dbd4)

 This perticular section of the script dum the  process the clocks and dump it into the the .csv file
 Check the snippet of code here given below
 ![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/16490439-b8c5-4bff-ba38-bdc20e6a5627)
 When run the scirpt wit the command ./TCLbox openMSP430_design_details.csv
 here is the outcome of the performing task and how the script works on the clock section and dumping on the .csv file. 

 ![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/db9cdab7-7bb5-4ab3-86e5-9cf92617efb6)

 Now we will open the file and check the necessary constraints are written over or not.
 give the command over terminal: vim outdir_openMSP430/openMSP430.sdc
 It can be observe here that the file has written with the clock constraints.

 ![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/20b41a63-913d-4e26-9a14-394f9f5815df)

Process the input constraints and dump them in to the .csv file.  In this given below search space we need to apply the algorithm ro convert this data into the data which can than pass to the opentimer tool. inputs contarints in the .csv files are gipresented here in the given screenshot.
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/504dc13b-c08c-4068-bb2a-e3d9113b4ad8)

This is the section of script which will work on this particluar sub task. 
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/c2f1628f-5285-4374-b872-3aba8562456c)
!![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/9eddb3ee-c241-4093-858d-2e5bc6b7f748)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/17fe3de2-61bb-4e1e-9076-e9f709769870)





















