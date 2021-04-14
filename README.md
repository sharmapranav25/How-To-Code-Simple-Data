# How-To-Code-Simple-Data

## Itemization
item.ized: every object considered is assigned an item. In this case, the traffic light colour *Red* has been assigned 0, *Green* -> 1, *Yellow* -> 2.


Understanding our program, we conclude with the idea that we will interpret a number and give a string as output 


    #traffic light
    #int -> string

    # red- 0
    # green- 1
    # yellow- 2

+Initializing variables*

      trafficlight= [0, 1, 2]
      ChangeColour=iter(trafficlight)


*Main body*

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
 
 
