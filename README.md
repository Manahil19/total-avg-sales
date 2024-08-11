# total-avg-sales
limit = 12
month = 1
Q1, Q2, Q3, Q4 = 0,0,0,0
Max, Min = 0, 0
sales = 0
while(month <= limit):
    print("Enter sales for Month-",month,":", end='')
    sales = int(input())
    if(month <= 3):
        Q1 += sales
    elif(month <= 6):
        Q2 += sales
    elif(month <= 9):
        Q3 += sales
    else:
        Q4 += sales
    
    if(month == 1):
        Max = sales
        Min = sales
    
    if(sales > Max):
        Max = sales
    if(sales < Min):
        Min = sales
    month += 1

avg1 = Q1/3
avg2 = Q2/3
avg3 = Q3/3
avg4 = Q4/3
print("\nAverage Sales of Q1 : ",avg1)
print("Average Sales of Q2 : ",avg2)
print("Average Sales of Q3 : ",avg3)
print("Average Sales of Q4 : ",avg4)

max_avg = avg1  # Assuming quarter 1 initially
max_quarter = 1
if avg2 > max_avg:
    max_avg = avg2
    max_quarter = 2
if avg3 > max_avg:
    max_avg = avg3
    max_quarter = 3
if avg4 > max_avg:
    max_avg = avg4
    max_quarter = 4

min_avg = avg1  # Assuming quarter 1 initially
min_quarter = 1

if avg2 < min_avg:
    min_avg = avg2
    min_quarter = 2
if avg3 < min_avg:
    min_avg = avg3
    min_quarter = 3
if avg4 < min_avg:
    min_avg = avg4
    min_quarter = 4
    
print("\nQuarter-",max_quarter," has the Average Maximum Sales, Which is ", max_avg)
print("Quarter-",min_quarter," has the Average Minimum Sales, Which is ", min_avg)


print("\nMaximum Sales in a Month : ", Max)
print("Minimum Sales in a Month : ", Min)
    
