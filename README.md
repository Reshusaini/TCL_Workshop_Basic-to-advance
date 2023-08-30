![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/9cc4e1d2-225c-4deb-8006-f5bc90cdbb7d)


# TCL_Workshop_Basic-to-advance
#TCL_scripting #VSD_learning #verilog #VLSI #Verification #YOSYS #Opentimer #Scripting_language

TCL Workshop_5 DAYS: Learning from  Basic of TCL basics to Advance Scripting Techniques in VLSI. IN this workshop we are going to learn to build a user Interface which will convert the constraits in .csv file to sdc format. With help of Tools Yosys and Opentimer, This user interface will generate a detailed report of the synthesized netlist and prelayout timing report.
TCL is widely used in VLSI industry for processing synthesis results, timing reports, automate the physical design flow such as floorplan, placement, and routing. 
Tcl stands for Tool Command Language. A command follow the instructions given and generate output as example, output a string, compute a math expression, or display a widget on the screen. This strong language can creäte everything into the frame of a command, even programming constructs.

DAY 1: Inception of the TCL workshop

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

DAY 2: Variable creation and processing constraints from CSV file

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

DAY 3: Clock and Input constraints

convert the format[1] & SDC formgat to the format[2] and pass to timing tool Opentimer tool.
first look at this blue box and the position of the coulumn here which need to convert into the standard format data.Process the clock and inputs and dump into the .csv file. Now understad the clock latency and  work our algorithm to convert this to Industry standared format which is the SDC format
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/17735390-074e-4d8e-8f7c-78debbc7dbd4)

 This perticular section of the script dum the  process the clocks and dump it into the the .csv file
 Check the snippet of code here given below
 ![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/16490439-b8c5-4bff-ba38-bdc20e6a5627)
 When run the scirpt with the command over the terminal: ./TCLbox openMSP430_design_details.csv
 here is the outcome of the performing task and how the script works on the clock section and dumping on the .csv file. 

 ![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/db9cdab7-7bb5-4ab3-86e5-9cf92617efb6)

 Now we will open the file and check the necessary constraints are written over or not.
 give the command over terminal: vim outdir_openMSP430/openMSP430.sdc
 It can be observe here that the file has written with the clock constraints.

 ![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/20b41a63-913d-4e26-9a14-394f9f5815df)

Process the input constraints and dump them in to the .csv file.  In this given below search space we need to apply the algorithm ro convert this data into the data which can than pass to the further. inputs constarints in the .csv files are presented here in the given screenshot.

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/504dc13b-c08c-4068-bb2a-e3d9113b4ad8)


This is the code of script which will process the input constraints and dump it into the .csv file.

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/c2f1628f-5285-4374-b872-3aba8562456c)
!![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/9eddb3ee-c241-4093-858d-2e5bc6b7f748)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/17fe3de2-61bb-4e1e-9076-e9f709769870)

 Now give the command the  ./TCLbox openMSP430_design_details.csv and observe how it works:
 
 ![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/91f26916-ae8f-40e1-8669-c164f4728fd3)

 Now we will open the file and check the necessary constraints are written over or not.
 give the command over terminal: vim outdir_openMSP430/openMSP430.sdc
 It can be observe here that the file has written with the Input constraints.
 
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/9abe0c14-18c1-4717-a6fe-eb3fa42bd152)

Process the output constraints and dump them in to the .csv file.  In this given below search space we need to apply the algorithm ro convert this data into the data which can than pass to the tool. OUTPUT constarints in the .csv files are presented here in the given screenshot

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/1aa4a51b-993f-4342-9d28-bafd7625432b)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/63e3e68f-4214-4857-909d-c305ba630417)

This is the code of script which will process the output constraints and dump it into the .csv file.

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/cab0af64-ba0f-4732-8943-1c9b56529985)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/cda037e6-31fc-42f9-ba09-4718d64ecf5b)

Now give the command the  ./TCLbox openMSP430_design_details.csv and observe how it works:

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/7f55aa8c-d310-44ae-b9cf-a992907b5cd9)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/6c7daa43-cb3c-43a0-9466-0f577a49b856)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/48cd031f-fa8e-4765-8577-7e1b1b1bcdc4)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/b58512d8-ff00-4be2-9396-57794f11133d)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/00794fa5-c7c2-4bde-81b1-ae6b084c78b1)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/86e7ed2d-6f17-493e-a72f-73ae418d048a)
![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/2fa6578a-128f-4fd9-8c72-35fad66ab28e)

 Now we will open the file and check the necessary constraints are written over or not.
 give the command over terminal: vim outdir_openMSP430/openMSP430.sdc
 After scrolling down to the bottom of the document,It can be observe here that the file has written with the OUTPUT constraints.
 
 ![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/8ab3166a-8918-423c-bd81-df179c8ee11b)

 Now SDC final file has created, Now last task is to involved here was to perform hierarchy check. This task  which reads all 
 the RTL files and elaborates. If either of the sub-module is not found then it will error out.Successfully created the hierarchy
 check script to be used by the yosys.
 First scenrio is hierarchy check passed

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/87e10441-7e3e-45c6-9c3e-f170777bf610)

Second scenrio is hierarchy check fail: to check this task. In verilog directory,  instance name changed to omsp_alu_new from omsp_alu.
And th tcl script raised a flag and give message as the hirerachy check fail. Screenshot is given below

![image](https://github.com/Reshusaini/TCL_Workshop_Basic-to-advance/assets/111287601/d9fec2c0-b1f1-40b6-bc40-d07f4e15ac86)





 


 

 
 




 




















