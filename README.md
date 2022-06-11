# Interface

## Aim:
To Develop a small bank application by declaring deposit() and withdrawal() as abstract methods in the interface.  Get the choice from the user whether to perform withdrawal or deposit operation. After the operation completes, display the balance amount

## Algorithm:
### step 1: 
Create an interface.

### step 2:
Create a child class.

### step 3:
Declare 2 functions deposit() and withdrawal() as abstract methods in the interface.

### step 4:
Create those 2 functions in the child class and perform respective operation.

### step 4:
Use while loop and and switch case to Get the choice from the user whether to perform withdrawal or deposit operation.

### step 5:
After performing the functions display the remaining balance of the user.

## Program:
```c#
using System;

namespace ConsoleApp2
{
    public interface bank
    {
        void deposit();
        void withdraw();
    }

    public class Acc : bank
    {
        public int amount, ch, balance = 500;
        public Acc()
        {
            Console.WriteLine("Choose the option");
            Console.WriteLine("1.Deposit\n2.Withdraw");
            int o = Convert.ToInt32(Console.ReadLine());
            switch(o)
            {
                case 1: deposit();
                    break;
                case 2: withdraw();
                    break;
                default: Console.WriteLine("Enter a valid choice");
                    break;
            }
        }
        public void deposit()
        {
            Console.WriteLine("Enter the amount to deposit");
            amount = Convert.ToInt32(Console.ReadLine());
            balance += amount;
        }
        public void withdraw()
        {
            Console.WriteLine("Enter the amount to withdraw");
            amount = Convert.ToInt32(Console.ReadLine());
            balance -= amount;
        }
    }
    public class program
    {
        public static void Main()
        {
            Acc a = new Acc();
            Console.WriteLine("Balance: "+a.balance);
        }
    }
}
```

## Output:
![Screenshot (230)](https://user-images.githubusercontent.com/75234807/173194563-f13bc9cd-63e6-4143-ba7d-3d0f341c0bd0.png)

## Result:
C# program to develop a bank application using interface is implemented successfully.
