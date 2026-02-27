## **Questions for better understanding TLS Data**
### This file contains all questions from the notebooks.

Solve these questions for yourself in preparation for the exam 😉

#### PART 1: 01_ARS_TLS_practical_RCT 

🤔 Reflection 1: rayextract terrain is used for isolating the terrain in the plot, and has some limited optional parameters. How could different terrain forms change this process? Would you expect higher slopes or rougher terrain to cause difficulties during data processing? Is there a way we can minimize this while collecting our data?

🤔 Reflection 2: At this point we already have a huge amount of results with relatively low processing time - point clouds, meshes, and structural data. You can take all of these data types in multiple directions for analysis. What are some ideas you have for how we can further use these products? Can you use multiple of them at once for even stronger analysis, or pair them with other data types?

🤔 Reflection 3: As you move to examine your segmented trees further in the lesson, you will see some errors in the automated segmentation and structural models. What aspects of the TLS data and forest do you think could be contributing to these errors in modeling? How would you expect other forest types and weather conditions to alter the results of this process? How would you design an experiment to test these questions?

#### PART 2: 03_ARS_TLS_practical_QSM

🤔 Reflection 1: Why do you think it is necessary to create a mesh to continue the process? That is - what aspect of the raycloudtools structure modeling approach do you think is dependant on the terrain mesh to model a tree?

🤔 Reflection 2: You have now completed all the the tree modeling and point cloud manipulation in the lesson and will move on to extracting metrics from the data. Keep in mind that in actual practice, we would want to apply this process to potentially hundreds or thousands of trees. How would you change or alter the workflow presented here to make it applicable on a much wider scale?

#### PART 3: 04_ARS_TLS_practical_ITSME

🤔 Reflection 1: which scenarios (regarding data collection, processing, ...) can you think of that could cause errors in this tree height estimation? For example, when there occlusion of the stem due to a bush surrounding the stem. Think of 2 other scenarios and if/how this could be mitigated.

🤔 Reflection 2: How accurate and precise do you think tree height is from TLS point clouds? Why?

🤔 Reflection 3: When would be best to use the circle fitting method and when would be best to use the concave hull method?

🤔 Reflection 4: What could cause problems with the diameter measurements using each of these methods?

🤔 Reflection 5: Which previous processing steps can have a impact on the DBH measurement?

🤔 Reflection 6: What are the advantages of measuring diameters with TLS compared to traditional measurement?

🤔 Reflection 7: What can influence the crown area value that you calculate?

🤔 Reflection 8: Is it always necessary to split the tree point cloud into crown and stem point clouds? If not, in which cases is it necessary?
