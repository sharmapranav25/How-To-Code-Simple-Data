# How-To-Code-Simple-Data

# Itemization
itemized: every object considered is assigned an item. In this case, the traffic light colour *Red* has been assigned 0, *Green* -> 1, *Yellow* -> 2.

### TRAFFIC LIFGT PROBLEM
Understanding our program, we conclude with the idea that we will interpret a INT and give a STRING as output 


    #traffic light
    #int -> string

    # red- 0
    # green- 1
    # yellow- 2

*Making Constants*

      trafficlight= [0, 1, 2]
      ChangeColour=iter(trafficlight)


*Main Body*

    try:
        light= next(ChangeColour)
        if light== 0:
            print("red")
        elif light== 1:
            print("green")
        elif light== 2:
            print("yellow")
    except:
        StopIteration
        ChangeColour= iter(trafficlight)
        light= next(ChangeColour)
        print("red")
        
*Running the main body multiple times*
 
     run1 -> red
     run2 -> green
     run3 -> yellow
     run4 -> *enters exception block - stops iteration* -recreats iterator -red
     run5 -> repeats
     
     
# Interval Itemization
Interval: all the numbers between two given numbers are assigned to one class of object

 
### NEWS YEAR COUNTDOWN

Understanding our problem, we can say that we will interpret TIME and give STRING/INT as outputs

        # def CountDown()
        #     interp. time-> MoreThan-10 return string
        #     interp. time-> LessThan-10 return integer+string
        #     interp. time-> EqualTo-0 return string
        
*Making Constants*

        time =range(12, 0, -1)
        count= iter(time)
        
*Main Body*

        def CountDown():
            try:
                CountNum=next(count)
                if CountNum >10:
                    print("Count Down hasn't started")
                else:
                    print(str(CountNum)+"!")
            except:
                StopIteration
                print("Happy New Year!!")
                
         CountDown()


*Running the main body multiple times*

    run1 -> Count Down hasn't started
    run2 -> Count Down hasn't started
    run3 -> 10!
    run4 -> 9!
    ...
    run11 -> 2!
    run12! -> 1!
    all consecutive runs -> Happy New Year!!
    
    
    
# Interval

Interval: all the numbers between two given numbers

### CHECK FOR AISLE SEATS IN A THEATRE
     

Understanding our problem, we arrive at the conclusion that we will interpret ROWS AN COLUMNS and give a BOOLEAN output

    #funtion to check for aisle seat

    # def isAisle(row, col):
    #     interp. row:column -> boolean


*Making Constant Data*


        import numpy as np
        #data
        r1=[1,2,3,4,5,6,7,8,9,10]
        r2=[1,2,3,4,5,6,7,8,9,10]
        r3=[1,2,3,4,5,6,7,8,9,10]
        theatre_seats= np.array(r1+r2+r3).reshape(3,10)

*Main Body*

        def isAisle(row, col):
            if theatre_seats[row,col] in theatre_seats[row: ,:1] or theatre_seats[row ,col] in theatre_seats[row:,-1:]:
                return True
            return False
    
*Outputs*

        isAisle(2,9) -> True
        isAisle(2,1) -> False

# Enumeration

Enumeration means one of the give items 

### TAKE GRADE FROM ONE OF A,B ANDC. BUMP IT UP.

Understanding our problem, we arrive at the conclusion that we will STRING and give a STRING output

    #fn_grade
    #def fn_grade(Grd): template
    #    interp. str -> str if str in grades
    
    #bumpUp grade
    # def bumpUp(grd): template
    #     interp. grade -> higher grade 
    
    
*Making Constants*

    grades =['A', 'B', 'C']
    

*Function for taking grade*



    def fn_grade(Grd):
        if Grd.upper() in grades:
            return Grd.upper()
    grd= input('Enter Grade')
    grd= fn_grade(grd)
    
*Function for bump up grade*   

    def bumpUp(grd):
        if grd == 'C':
            grd ='B'
            return grd
        elif grd == 'B':
            grd= 'A'
            return grd
        return "A"
   

*Outputs*

    Entre Grade: c
    bumpUp(grd) -> B

    Entre Grade: b
    bumpUp(grd) -> A

    Entre Grade: A
    bumpUp(grd) -> A
    
    
# Arbitrary Sized Data

So far we have been working with data that is known. But if we have to store unknown data, or arbitrary sized data, we have to use different data definition. List is an  arbitrary sized data

*Making Variables*

    #Employee data
    Emp1= list()

*Adding Data To Our Employee Variable*

    
    Emp1.append("Pranav")
    Emp1.extend([25, "Male"])
    
*Outputs*


    ['Pranav', 25, 'Male']



    
    
