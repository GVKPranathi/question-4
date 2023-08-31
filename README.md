# question-4
Problem Statement – FOE college wants to recognize the department which has succeeded in getting the maximum number of placements for this academic year. The departments that have participated in the recruitment drive are CSE,ECE, MECH. Help the college find the department getting maximum placements. Check for all the possible output given in the sample snapshot

Note : If any input is negative, the output should be “Input is Invalid”.  If all department has equal number of placements, the output should be “None of the department has got the highest placement”.

Sample Input 1:

Enter the no of students placed in CSE:90
Enter the no of students placed in ECE:45
Enter the no of students placed in MECH:70
Sample Output 1:

Highest placement
CSE

Sample Input 2:

Enter the no of students placed in CSE:55
Enter the no of students placed in ECE:85
Enter the no of students placed in MECH:85
Sample Output 2:

Highest placement
ECE

MECH

Sample Input 3:

Enter the no of students placed in CSE:0
Enter the no of students placed in ECE:0
Enter the no of students placed in MECH:0
Sample Output 3:

None of the department has got the highest placement
Sample Input 4:

Enter the no of students placed in CSE:10
Enter the no of students placed in ECE:-50
Enter the no of students placed in MECH:40
Sample Output 4:

Input is Invalid


CODE
print("enter the number of students placed in CSE")
cse=int(input())
print("enter the number of students placed in ECE")
ece=int(input())
print("enter the number of students placed in Mech")
mech=int(input())

def fun(cse,ece,mech):
  if (cse or ece or mech)<0:
    return "invalid number of students"
  if cse==0 and ece==0 and mech==0:
    return "no department has highest placement"
  if cse>ece and cse>mech:
    return "CSE has highest placement"
  if ece>cse and ece>mech:
    return "ECE  has highest placement"
  if mech>cse and mech>ece:
    return "Mech  has highest placement"
  if cse==ece:
    return "both CSE and ECE has highest placemeny"
  if cse==mech:
    return "both CSE and Mech has highest placemeny"
  if ece==mech:
    return "both Mech and ECE has highest placemeny"
  if cse==0 and ece==0 and mech==0:
    return "No department has highest placement" 

print(fun(cse,ece,mech))

CODE2
import sys
cse=int(input("Enter the no of students placed in CSE:"))

ece=int(input("Enter the no of students placed in ECE:"))

mech=int(input("Enter the no of students placed in MECH:"))

if(cse< 0 or ece< 0 or mech< 0):
    print("Input is Invalid")
    sys.exit()

elif(cse == ece and ece == mech ):
    print("None of the department has got the highest placement")

sys.exit()

print("Highest placement")

m=max(cse,ece,mech)

if(cse==m):
 print("CSE")

if(ece==m):
    print("ECE")

if(mech==m):
    print("MECH")


 
 

  
