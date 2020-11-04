# Oxygen-Level-of-an-gym-trainer-
Compare the oxygen level of the gym trainers and pick the best of them 
You can clone(download) the repository or copy the below code in your preferred editor

#include <iostream>

using namespace std;

int main()
{
    int o1[3],o2[3],o3[3]; // Oxygen Level of respective trainers
    int avg1 = 0,avg2 = 0,avg3 = 0;

    cout<<"Enter the first trainer data"<<endl;
    for(int i = 0;i<3;i++)
    {
        cin>>o1[i];
        if(o1[i]<0 || o1[i]>100)
        {cout<<"INVALID INPUT "<<endl;
            return 0;}
        avg1 = avg1 + o1[i];
    }
    avg1 = avg1/3;

    cout<<"Enter the second trainer data"<<endl;
    for(int i = 0;i<3;i++)
    {
        cin>>o2[i];
        if(o2[i]<0 || o2[i]>100)
        {cout<<"INVALID INPUT "<<endl;
            return 0;}
        avg2 = avg2 + o2[i];
    }
    avg2 = avg2/3;

    cout<<"Enter the third trainer data"<<endl;
    for(int i = 0;i<3;i++)
    {
        cin>>o3[i];
        if(o3[i]<0 || o3[i]>100)
        {cout<<"INVALID INPUT "<<endl;
            return 0;}
        avg3 = avg3 + o3[i];
    }
    avg3 = avg3/3;
    cout<<"Oxygen of Trainer 1 is"<<avg1<<endl;
    cout<<"Oxygen of Trainer 2 is"<<avg2<<endl;
    cout<<"Oxygen of Trainer 3 is"<<avg3<<endl;

    int fitTrainer ;

    if(avg1<70)
        cout<<"Trainer 1 unfit "<<endl;
    else if(avg1 >= avg2 && avg2>=avg3)
    {
        fitTrainer = avg1;
    }

    if(avg2<70)
        cout<<"Trainer 2 unfit "<<endl;
    else if(avg2 >= avg1 && avg1>=avg3)
    {
        fitTrainer = avg2;
    }

    if(avg3<70)
        cout<<"Trainer 3 unfit "<<endl;
    else if(avg3 >= avg2 && avg2>=avg1)
    {
        fitTrainer = avg3;
    }

    if(avg1 == fitTrainer)
    cout<<"Trainer 1 is fit"<<endl;
    if(avg2 == fitTrainer)
    cout<<"Trainer 2 is fit"<<endl;
    if(avg3 == fitTrainer)
    cout<<"Trainer 3 is fit"<<endl;
    return 0;
}

