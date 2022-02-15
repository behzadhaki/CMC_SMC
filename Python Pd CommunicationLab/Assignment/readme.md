Assignment for Week 5 Lab
------
For this assignment, you have two options to choose from:
 - Option 1: Extending the functionalities of the pd/python examples reviewed in the lab
 - Option 2: Implementing a note delay in python 
 See below for detailed explanation
 
 **Deliverables**
 1. Your pd files (to be placed in the Assignment/PdPatch/ directory)
 2. Your python source codes (to be placed in the Assignment/SourceCode/ directory)
 3. A report discussing your submissions (to be placed in the Assignment/Report/ directory). 
 For the video, I would like a recording showing that the code/patches work as intended. 
 You should also talk about your implementations in the video. (**2 Marks**)
 If you fail to make some part work, make sure to discuss the issues and the process in the video for partial marks.  

Lastly, If you prefer not to talk over the video, please write a short document instead to accompany the video.     

#### Important Notes About Submissions:
1. The main pd patch you use, must be named in this format FirstName_LastName_uNumber.pd where uNumber is your student number starting with u.
The same filename with a .py extension must be used for your main python script. 
2. **The assignment won't be marked if no report is delivered**  
3. Each option is 8 Marks overall and 2 marks are dedicated to the report.

Feel free to use any of the source codes/patches provided. 
   
## Option 1 
In this option, you are asked to modify the patches/source codes provided for Example 3 (two-way communication). 

### Task A. (1 Mark)
Extend the existing pd patch (Example_3_two_way_communication.pd) to 4 quarter notes (i.e. extend to 16 steps).

### Task B. (2 Marks)
Implement two sliders or number boxes to specify the minimum and maximum pitch allowed to be generated in the python script.

### Task C. (2 Marks)
Remove the note quantizer from the pd patch. Instead, implement a note quantizer in python such that only specific notes can be generated.

### Task D. (2 Marks)
Right now the drum generation is uniformly random. Modify the drum generator such that the generations are not sampled given a set of weights for each instrument. 
For example, let's assume we are dealing with Kick Snare and Hat generation. If we randomly sample these, there is a 1/3 probability of any of these to be active.
if we want to modify the code such that kicks are 3 times and snares are 2 times more likely than hats, 
then the probability of a kick happening would be 3/(3+2+1) and snare would be 2/(3+2+1) and hats would be 1/(3+2+1). 

## Option 2 (7 Marks)
**Please only attempt this option if you are experienced with the concepts discussed in class as well as multi-threaded programming.** 
Implement a note delay in python. The delay time and feedback should be controllable from pd. 
For this work, we assume notes come via osc from pd, and the delayed versions are broadcast back to pd at the right time specified by the delay time and the feedback. 
You don't need to implement a sequencer in pd to send notes, you can manually do so via a trigger button that signals osc sender to send a specified pitch, velocity, duration to python

One approach here would be to use a separate Thread for each note received, in which the repetitions are sent back to pd at correct times. 

**Note** You can assume that the delay time and feedback for a note are constant after the note is received in python  