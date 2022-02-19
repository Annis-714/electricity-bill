# electricity-bill
print("                 WELCOME TO INFY ELECTRICITY BILL       ")


print("Kindly fill the below form to step further")


#NAME INPUT
fname=input("Enter your first name:")
sname=input("Enter your Second name:")

#MOBILE NUMBER
while True:
    num=input("Enter mobile number:")
    if num.isdigit() and len(num)==10:
        break
    else:
        print("Enter valid number of 10 digit")
        
#ACCOUNT NUMBER
while True:
    acc=input("ECnumber:")
    if acc.isdigit()and len(acc)==12:
        break
    else:
        print("Verify and give 12 digit number")
        
#ADDRESS
add1=input("Enter your addres line1:")
add2=input("Enter your addres line2:")
add3=input("Enter your addres line3:")
print("\n")

#BILLING
def electricitybill(unit):
    rate=2.3*unit
    CGST=rate*(1.5/100)
    SGST=rate*(1.5/100)
    TOT=rate+100+CGST+SGST
    print("\tEC charges:",rate)
    print("\tRC charges:100")
    print("\tCGST:",CGST)
    print("\tSGST:",SGST)
    print("Total amount:",TOT)

print("Choices")
print(" 1.View details \n 2.View bill \n 3.Exist")
print("\n")
while True:
    choice=int(input("Enter your choice(1,2,3):"))
    print("\n")
    if choice==1:
        #DETAILS
        print("CUSTOMER DETAILS")
        print("Name:",fname.upper(),sname.upper())
        print("Mobile number:",num)
        print("ECnumber:",acc)
        print("Address:",add1.upper(),add2.upper(),add3.upper())
        print('\n')
        CH=input("To continue type S:")
        if CH.upper()=="S":
            continue
        else:
            break
    if choice==2:
        #BILL
        unit=int(input("Enter units used:"))
        print('\n')
        if unit<=100:
            print("Lessthan 100 units electricity is free to all Inian citizens")
        else:
            electricitybill(unit)
        print('\n')
        CH=input("To continue type S:")
        if CH.upper()=="S":
            continue
        else:
            break
    if choice==3:
        break
    
    else:
        print("ENTER VALID CHOICE AND RESTART THE PROGRAM")
print("\n")
print("THANK YOU FOR VISITING US")
print("\n")
print("*********************Today's wastage is tomorrow's shortage*********************")
print("************************use it wisely!!************************")
      

        
        
        
        
