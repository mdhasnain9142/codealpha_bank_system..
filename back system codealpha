
// TASK 4: BANKING SYSTEM
#include<iostream>
#include<iomanip>
using namespace std;
class BANK
{
    string name;
    double account;
    double account1;  
    int balance[100];
    int withdrawals[100];
    int deposits[100];
    int fundtransfer[100];
    int currbalance=0;
    int count=0;
    int amount;
    int n;
    int i;
    public:
    void getinfo()
    {
        cout<<"enter customer name:"<<endl;
        getline(cin,name);
        while(true)
        {
        cout<<"enter account number(6 digit):"<<endl;
        cin>>account;
        if(account>=100000 && account<=999999)
        {
            cout<<"account accepted"<<endl;
            break;
        }
        else
        {
            cout<<"invalid account number.Please enter exactly 6 digits"<<endl;
        }
    }
}
    int show()
    {
        while(true)
        {
        cout<<"\n welcome "<<name<<endl;
        cout<<"1. view Balance"<<endl;
        cout<<"2. Deposit"<<endl;
        cout<<"3. Withdraw"<<endl;
        cout<<"4. Fund Transfer"<<endl;
        cout<<"5. transaction history"<<endl;
        cout<< "Any other key to Exit"<<endl;
        cout<< "Enter choice: ";
        cin>>n;
        switch(n)
        {
            case 1:
            cout<<"balance: "<<currbalance<<endl;
            break;
            case 2:
            cout<<"enter deposit amount"<<endl;
            cin>>amount;
            currbalance=currbalance+amount;
            count++;
            deposits[count]=amount;
            withdrawals[count]=0;
            balance[count]=currbalance;
            fundtransfer[count]=0;
            cout << "Amount deposited successfully" << endl;
            break;
            case 3:

            cout<<"enter withdrawal amount"<<endl;
            cin>>amount;
            if(amount>currbalance)
            {
                cout<<"Withdrawal can't be processed (Insufficient balance)"<<endl;
            }
            else
            {
                currbalance=currbalance-amount;
                count++;
                 deposits[count]=0;
                 withdrawals[count]=amount;
                 balance[count]=currbalance;
                 fundtransfer[count]=0;
                cout << "Withdrawal successfully" << endl;
            }
            break;
            case 4:
                while(true)
                {
            cout<<"enter recipient account number to transfer fund"<<endl;
            cin>>account1;
            if(account1>=100000 && account1<=999999)
        {
            cout<<"recipient account accepted"<<endl;
            break;
        }
        else
        {
            cout<<"invalid recipient account number.Please enter exactly 6 digits"<<endl;
        }
    }
            cout<<"enter amount to tranfer"<<endl;
            cin>>amount;
            if(amount>currbalance)
            {
                cout<<"fund transfer can't be processed (Insufficient balance)"<<endl;
            }
            else
            {
                currbalance=currbalance-amount;
                count++;
                 deposits[count]=0;
                 withdrawals[count]=0;
                 balance[count]=currbalance;
                 fundtransfer[count]=amount;
                cout<<"fund transfered successfully";
            }
            break;
            case 5:
             cout << "\n\t ----- Transaction History -----\n";
                    cout << left << setw(10) << "Index" 
                         << setw(15) << "Deposit" 
                         << setw(15) << "Withdraw" 
                         << setw(15) << "Transfer" 
                         << setw(15) << "Balance" << endl;

                    for (i = 1; i <= count; i++) {
                        cout << left << setw(10) << i
                             << "Rs " << setw(12) << deposits[i]
                             << "Rs " << setw(12) << withdrawals[i]
                             << "Rs " << setw(12) << fundtransfer[i]
                             << "Rs " << setw(12) << balance[i]
                             << endl;
                    }
                    break;
            default:
            cout<<"\n...Transaction Completed..."<<endl<<"---Exiting--"<<endl;;
            return 0;
            
    }
    }
    }
};

int main()
{
    BANK B;
    B.getinfo();
B.show();
}
