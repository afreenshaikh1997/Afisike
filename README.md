# Afisike
CODE.FUN.DO repository

Our Earth has suffered a great deal from reoccurring natural disasters that have repeatedly put a strain on people’s lives. A natural disaster is a sudden event, an accident or a natural havoc, that causes great extents of damage or multiple deaths. It becomes really crucial to address people's concerns during these times. 
Hundreds and thousands of calls flood the rescue call lines, making it nearly impossible to address them by just using man-power to attend the calls.
We aim to handle this situation by developing a software, which would take the recorded input from a bot which attends the calls.
The first step would be that, the recorded speech of the user is made to pass through, what we call as a filter, an algorithm that detects intensity of the emotion from speech, thus probabilistically prioritizing the calls. The calls are given weights in decreasing order based on the priority.
In the second step,the calls are then processed to get the important information like the place and the severity of the calamity at that place. According to the weights based on the intensity of the emotion, which were aquired from the filtering step, each place is prioritized and a suggestion is made to the rescue team as to which areas need more support and attention.

For example,
Consider a situation where floods have occurred in West bengal.
Say, if the bot receives 10,000 calls and after the filtering (First step), 5,000 calls were given high priority, 3000 given medium priority and 2000 are given low priority. The fixed weights assigned to the priorities are say [5 : high ,3 : medium ,2 : low].

After the second step,
Out of 5000 calls of high priority, 3000 were classified to be received from Kolkata and 2000 from Durgapur.
Out of 3000 calls of medium priority, 2000 were classified to be received from Kolkata and 1000 from Durgapur
Out of 2000 calls of low priority, 500 were classified to be received from Kolkata and 1500 from Durgapur

Now the value for Kolkata would be = (3000 * 5 + 2000 * 3 + 500 * 2) / 10000 = 2.2. 
And the value for Durgapur would be = (2000 * 5 + 1000 * 3 + 1500 * 2) / 10000 = 1.6.

Based on these results, we could understand that support and attention to Kolkata is of more importance.
