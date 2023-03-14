import random
import string
import sys

lenght = int(input("How long would you like your password to be?\n"))

if lenght < 8:
  print("\nA safe password cannot contain less than 8 characters.")
  exit()

else:
  addnumb = input("Would you like to add numbers to your passwords?\n")
  addchar = input("Would you like to add special characters to your passwords?\n")

  if addnumb.lower() == "no" and addchar.lower() == "no": #I want to execute the code only if the two conditions are met: in this case, generate only an alphabetic pssw
    letters = [] #I create an empty list, to assign items later on and manipulate them

    for i in range(lenght):
      random_letter = random.choice(string.ascii_letters)
      letters.append(str(random_letter))
  
    letters = ''.join(letters)
    print(letters)

  elif addnumb.lower() == "yes" and addchar.lower() == "no": #in this case I only want a password with letters and digits
    letters = []

    for i in range(lenght):
      random_letter = random.choice(string.ascii_letters)
      letters.append(str(random_letter))
  
    nr_of_num = int(lenght / 3) #this could also be indicated as (lenght // 3)
            #this variable tells me how many random numbers I want to include in the password, in a way that around 1 third of the password is numerical
            #the number I will obtain will be used to create another loop (for "i" in "nr_of_num"), so that I generate as many random numbers as this variable
            # then I assign each of those numbers to a random position in my string                 
                               
    for i in range(nr_of_num):
      rn = random.randint(0, 9) #I generate a random number and I assign the number to a variable, which is an integer
      rn = str(rn) #Since I wanna put the variable within a list, I convert the type of the variable (rn), from int to a str
      ri = random.randint(0, lenght-1) #I generate a variable called random item, to which I assign a random number, so that a random item is chosen from my list
                                    #this will tell me the position of the item in the list I want to sobstitute with the variable rn
      letters[ri] = rn #I assign the new value (rn, which is now an str and not int) to a random item from my list letters (ri)
          
    letters = ''.join(letters)
    print(letters)

  elif addnumb.lower() == "yes" and addchar.lower() == "yes": #in this case I only want a password with letters, digits, and special characters
    letters = []

    for i in range(lenght):
      random_letter = random.choice(string.ascii_letters)
      letters.append(str(random_letter))
  
    nr_of_num = int(lenght / 3)               
                               
    for i in range(nr_of_num):
      rn = random.randint(0, 9) 
      rn = str(rn) 
      ri = random.randint(0, lenght-1) 
      letters[ri] = rn 
    
    for i in range(nr_of_num):
      spc = random.choice(string.punctuation) #I create a random special charachter and I assign to special_character variable (spc)
      ri = random.randint(0, lenght-1) 
      letters[ri] = spc 

    letters = ''.join(letters)
    print(letters)
    
  elif addnumb.lower() == "no" and addchar.lower() == "yes": #in this case I only want a password with letters, digits, and special characters
    letters = []

    for i in range(lenght):
      random_letter = random.choice(string.ascii_letters)
      letters.append(str(random_letter))
  
    nr_of_num = int(lenght / 3)               
    
    for i in range(nr_of_num):
      spc = random.choice(string.punctuation) #I create a random special charachter and I assign to special_character variable (spc)
      ri = random.randint(0, lenght-1) 
      letters[ri] = spc 

    letters = ''.join(letters)
    print(letters)