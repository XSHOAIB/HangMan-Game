
import random

name=input('in Name: ')
print('ATB',name)

word=['rain','cloud','mango','orange','papaya','king','queen','man','women']

choice=random.choice(word)
count=8
guesses=''


def man(j):
    if j==8:
        print("_________\n|      |\n|     \n|    \n|      \n|      \n|      \n|     \n|       \n---------------------")
    elif j==7:
        print("_________\n|      |\n|     (~)\n|    \n|      \n|      \n|      \n|     \n|       \n---------------------")
    elif j==6:
        print("_________\n|      |\n|     (~)\n|    \_|_/\n|      \n|      \n|      \n|     \n|       \n---------------------")
    elif j==5:
        print("_________\n|      |\n|     (~)\n|    \_|_/\n|      |\n|      \n|     \n|    \n|       \n---------------------")
    elif j==4:
        print("_________\n|      |\n|     (~)\n|    \_|_/\n|      |\n|      |\n|      n|\n|       \n---------------------")
    elif j==3:
        print("_________\n|      |\n|     (~)\n|    \_|_/\n|      |\n|      |\n|     / \ \n|    /   \ \n|       \n---------------------")
    elif j==2:
        print("_________\n|      |\n|     (~)\n|    \_|_/\n|      |\n|      |\n|     / \ \n|     \n|       \n---------------------")
    elif j==1:
        print("_________\n|      |\n|     (~)\n|    \_|_/\n|      |\n|      |\n|     / \ \n|    /   \ \n|       \n---------------------")
        

while count>0 :
    f=0
    for char in choice:
        if char in guesses:
            print(char,end=' ')
        else:
            print('_',end=' ')
            f+=1
    if f==0:
        print('\nyou win!')
        print("_________\n|      \n|\n|     (~)\n|     _|_\n|    / | \ \n|      |\n|     / \ \n|    /   \         \n---------------------")
        break
    print()
    guess=input('enter guess: ')
    if guess not in choice:
        print('wrong')
    else:
        guesses+=guess
    
    man(count)
    count-=1
    if count==0:
        print('you loose')
