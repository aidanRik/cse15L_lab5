# Lab 5 
## Aidan Rikic

## Part 1  
Post from student:  
Hi everyone, I’m having trouble with the merge method in ListExamples.java. It doesn’t seem to return the correct merged list when I run my bash script to test it. Here is a screenshot of the test output and the relevant code snippet. I think that the problem might be with the way the indices are being handled, but I'm not sure how to confirm this.  
![Image](ss11_lab5)

Response from Ta:  
Hi, it looks like there might be an issue with how the merge method handles the elements from the two lists. Could you add some print statements inside the while loops to track the values of index1, index2, and the current elements being compared? This might give us more insight into where things are going wrong.  

Students follow up:  
Hi again, I added the print statements and ran the script. Here’s the new code:  
![Image](ss22_lab5)

Heres the output:  
`Comparing apple and banana
Comparing apple and cherry
Comparing banana and cherry
Comparing date and cherry
Comparing fig and cherry`  
After adding the print statements, I realized that the issue is when the two lists have elements with the same value. The merge method adds the element from the second list and increments index2, but it doesn’t handle the duplicate value correctly, causing some elements to be missed or duplicated incorrectly.  

Setup:  
Contents of `ListExamples.java` before fixing the bug:  
![Image](ss33_lab5)  

Contents of `test.sh` the bash scrpit to compile and run the test:  
![Image](ss44_lab5)  

Command line to trigger the bug:  
`bash test.sh`  

Description of edit:  
To fix the bug, we need to handle the case where the elements being compared are equal. We should add both elements to the result list and increment both indices.  

## Part 2  
