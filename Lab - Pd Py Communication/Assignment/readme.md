Assignment for Week 5 Lab
------

Extending the functionalities of the pd/python examples reviewed in the lab
----

 
 **Deliverables**
 1. Your pd files (to be placed in the Assignment/PdPatch/ directory)
 2. Your python source codes (to be placed in the Assignment/SourceCode/ directory)
 3. A video reporting/discussing your submissions (to be placed in the Assignment/Report/ directory). 
 For the video, I would like a recording showing that the code/patches work as intended. 
 You should also talk about your implementations in the video. (**1 Mark**)
 If you fail to make some part work, make sure to discuss the issues and the process in the video for partial marks. 
 Lastly, If you prefer not to talk over the video, please write a short document instead to accompany the video.     

#### Important Notes About Submissions:
1. The Main folder you submit, must be named as:

   
     /[FirstName_LastName_uNumber]/

2. The same filename with a .py extension must be used for your main python script and pd patch

   
     /[FirstName_LastName_uNumber]/*/[FirstName_LastName_uNumber].pd
     /[FirstName_LastName_uNumber]/*/[FirstName_LastName_uNumber].py


 
3. **The assignment won't be marked if no report is delivered**  
4. The tasks add up to 8 marks and 2 marks are dedicated to the report. 

**Don't spend too much time on the report. As long as the video (and the written document in case you don't like to narrate on the video)
 shows what works/doesnt work and comments on your implementation, you will get full marks on the report submission requirement.** 

Feel free to use any of the source codes/patches provided. 
   
## Tasks 
You are asked to modify the patches/source codes provided for Example 3 (two-way communication). 

### Task A. (1 Mark)
Extend the existing pd patch (Example_3_two_way_communication.pd) to 4 quarter notes (i.e. extend to 16 steps).

### Task B. (1 Mark)
Implement two sliders or number boxes to specify the minimum and maximum pitch allowed to be generated in the python script.

### Task D. (2 Marks)
Right now the drum generation is uniformly random. Modify the drum generator such that a set of user-defined weights denote the relative likelihood of each voice generated. 
For example, let's assume we are dealing with Kick, Snare and Hat generation. If we randomly sample these, there is a 1/3 probability of any of these to be active.
if we want to modify the code such that kicks are 3 times and snares are 2 times more likely than hats, 
then the probability of a kick happening would be 3/(3+2+1) and snare would be 2/(3+2+1) and hats would be 1/(3+2+1).

