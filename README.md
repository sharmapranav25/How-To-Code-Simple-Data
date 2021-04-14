# How-To-Code-Simple-Data

# Itemization
item.ized: every object considered is assigned an item. In this case, the traffic light colour *Red* has been assigned 0, *Green* -> 1, *Yellow* -> 2.

### TRAFFIC LIFGT PROBLEM
Understanding our program, we conclude with the idea that we will interpret a number and give a string as output 


    #traffic light
    #int -> string

    # red- 0
    # green- 1
    # yellow- 2

*Initializing variables*

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
 
 
### NEWS YEAR COUNTDOWN

Understanding our problem, we can say that we will interpret time and give sting/integers as outputs

        # def CountDown()
        #     interp. time-> MoreThan-10 return string
        #     interp. time-> LessThan-10 return integer+string
        #     interp. time-> EqualTo-0 return string
        
*Initializing variables*

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
    
    
    

     




