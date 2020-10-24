# checkarmstrongnumbergit
#python program to determie whether 
#the number is armstrong number or not
#function to calculate x raised to
#the power y
def power(x,y):

if y==0:
 return 1
 if y%2==0:
        return power(x,y//2)*power(x,y//2)

     return x* power(x,y//2)*power(x,y//2)
 #funtion to calcualte order of the number
 def order (x):
  
  #variable to store of the number
  n=0
  while(x!=0):
  n=n+1
  x=x//10
  return n
#function to check the given 
#number is armstrong number or not
def isarmstrong(x):
 
 n=order(x)
 temp=x
 sum1=0
 
 while (temp!=0):
 r=temp%10
 sum1=sum1+power(r,n)
 temp=temp//10
 #if condition satisifies
 return(sum1==x)
