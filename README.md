# Study Hours Analyzer
This repository showcases my journey as a Python developer, featuring a collection of projects that demonstrate my skills in programming, problem-solving, and software development. From beginner exercises to more advanced applications, this portfolio highlights my growth and dedication to mastering Python.

#Study Hours Analyzer Program

#Display a welcome message and a brief description
print("----------Welcome to Study Hours Analyzer!----------")
print("With this program you can obtain the average of the hours that you study per week.") 

#Create an empty list to store the hours studied each day
hours = []

#List containing the day of the week
week_days = ["monday", "tuesday", "wednesday", "thursday", "friday", "saturday", "sunday"] 

#Function to calculate and display study stadistics
def avg():
    for day in week_days:
        #Asks the how many hours studied on each day
        data = float(input(f"How many hours you studied on {day.capitalize()}: ")) 
        hours.append(data) #Add the input to the hours list
    
    average = sum(hours)/len(hours)  #Calculate the average hours per day
    add_total= sum(hours)            #Calculate the total hours studied

    print("-" * 30) #Separator for clarity
    print(f"Total hours studied: {add_total}")
    print(f"Average per day: {average:.2f}")

    #Provide feedback based on the average study time
    message = "Feedback: "
    if average >= 4:
        print(f"{message}Great consistency!")
    elif 2 < average < 4:
        print(f"{message}Not bad. Try to increase a bit.")
    else:
        print(f"{message}You need to study more!")

#Call the function to run the analysis
avg()
