# python16(24-7-25)
RECURSIONS
#fibnocci on tree recurssions
def fib(n):
    if n<=1:
        return n
    return fib(n-1)+fib(n-2)
terms =int(input("enter number of terms to print:"))
print(("fibnocci series...."))
for i in range(terms):
    print(fib(i),end=" ")


 #permutations
def permute(s,bucket=' '):
    if not s:
        print(bucket)
        return
    for i in range(len(s)):
        new_str=s[ :i]+s[i+1: ]
        permute(new_str,bucket+s[i])
text=input("enter a name/word:")
print("possibilities of combinations...")
permute(text)




#binary combinations
'def binary(n,b=" "):
    if n==0:
        print(b)
        return
    binary(n-1,b+"0")
    binary(n-1,b+"1")
length=int(input("enter length of string:"))
print("binary combinations...")
binary(length)


#tail recursion
def head(n):
    if n==0:
        return
    print(n)
    head(n-1)
num=int(input("enter a number:"))




#TAIL RECURSION
def sumtail(n,temp=0):
    if n==0:
        return temp
    return sumtail(n-1,temp+n)
num=int(input("enter  a number:"))
print('sum:',sumtail(num))

