import string #import the string module
rec=[]

def reverse(a):#defining reverse function
	return a[::-1]
#define palindrome checking function
def palindrome(a):
	#call reverse function
	rev = reverse(a) 
	if (a==rev):
		return True
	return False
#Driver code 
while True: 
	a=input('Enter String: ')
	a=a.lower() #converts all input to lower case
	exclude=set(string.punctuation)
	a=''.join(ch for ch in a if ch not in exclude)#ignores punctuation
	a=''.join(a.split()) #removes all the whitespaces

	if a=="":
		break
	rec.append(a)	
	ans=palindrome(a)
	if ans==1:
		print(a,'is a palindrome')
	else:
		print(a,'is not a palindrome')
print('No String Entered, Exiting...')

record = rec[-5:] #select from the list of entries the last five entries made by user
print('The last entries entered by user are: ',record)			
