mport time

print("please insert your card")

time.sleep(5)

password=1234

pin=int(input("enter your atm pin"))

balance=5000

if pin==password:
  while True:

    print("""
       1 == balance
       2 == withdraw amount balance
       3 == deposit balance
       4 == exit
       """
       )
    try:
      option=int(input("please enter your choice"))
    except:
      print("please enter valid option")

    if option==1:
      print(f"your current balance is {balance}")

    if option==2:

      withdraw_amount=int(input("please enter withdraw_amount"))

      balance=balance-withdraw_amount

      print(f"your updates balance is {balance}")

    if option==3:

      deposit_amount=int(input("please enterdeposit_amount"))

      balance=balance+deposit_amount

      print(f"{deposit_amount} is credited to your account")

      print(f"your current balance is {balance}")

    if option==4:
      break

else:
  print("wrong pin please try again")
