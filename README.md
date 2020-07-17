# Hello-world
# my first respository
#I imported random to generate the random Number for the OTP numbers
#date time is just a fancy one and time for monitoring of the code time and when it expires
import random
import datetime
import time

#Otp code is generated immediately the enter button is being pressed and the expiry time starts to count 
x = random.randint(1000, 9999)
while True:
    otp = input("Press enter to generate your OTP code:")
    if otp == "":
        print("Your OTP code is:", x, "Do not share it with anyone, OTP expires after 30 seconds")
        break
    else:
        print("press enter")
        continue

#starTime is the particular time the OTP was generated
starTime = time.time()
mes = """





"""
#mes is just to space the otp generator(Server) from the Client's(User). Not useful in real time situation
print(mes)

#endTime is time the Otp code generated is being input on the Client's side
endTime = starTime - time.time()
ty = datetime.datetime.now()

#The Client's view where the OTP code being generated is being entered and if time taken is longer than the given time, the code expires and breaks out, 
#while if the code is incorrect, it prints "Incorrect OTP code"
while True:
    new = int(input("Enter your OTP code:"))
    try:
        if x == new:
            endTime = starTime - time.time()
            if endTime < -30.31637120246887:
                print("OTP code expired")
                break
            print(f"Successful, you logged in on Jupyter Notebook on {ty}")
            break

        else:
            print("Incorrect OTP code")
    except ValueError:
        print("Incorrect format")

endTime = starTime - time.time()
