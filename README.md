#project1
#include<iostream>;
using namespace std;
int fact(int n){
    int factorial=1;
    for (int i = 1; i <=n; i++)
    {
     factorial=factorial*i;
    }
    return factorial;

    
}

float power(float z,float y){
    int ans=1;
    
    for (int i=1; i <=y; i++)
    {

       ans *= z;

    }
    return ans;
    
}
float sin(float x)
{
    float y = 0;
    for (int i = 3; i <= 19; i += 4)
    {
        y -= (power(x, i) / fact(i));
    }
    for (int s = 1; s <= 15; s += 4)
    {
        y += (power(x, s) / fact(s));
    }

    return y;
}
float cos(float x)
{
    float y = 0;
    for (int i = 2; i <= 15; i += 4)
    {
        y -= (power(x, i) / fact(i));
    }
    for (int s = 0; s <= 15; s += 4)
    {
        y += (power(x, s) / fact(s));
    }

    return y;
}
float tan(float x){
    float y;
    y=sin(x)/cos(x);
return y;}
int main(){
int a;

cout<<"Enter the operation:"<<endl;
cout<<"1:addition"<<endl;
cout<<"2:subtraction"<<endl;
cout<<"3:multiplication"<<endl;
cout<<"4:division"<<endl;
cout<<"5:trigonometry function"<<endl;
cout<<"6:exponent"<<endl;
cin>>a;
if(a==1){double num,num2;
cout<<"enter num1:";
cin>>num;
cout<<"enter num2:"<<endl;
cin>>num2;
cout<<"the value is:"<<endl;
cout<<num+num2;}
else if(a==2){double num,num2;
cout<<"enter num1:";
cin>>num;
cout<<"enter num2:"<<endl;
cin>>num2;
cout<<"the value is:"<<endl;
cout<<num-num2;}
else if(a==3){double num,num2;
cout<<"enter num1:";
cin>>num;
cout<<"enter num2:"<<endl;
cin>>num2;
cout<<"the value is:"<<endl;
cout<<num*num2;}
else if(a==4){double num,num2;
cout<<"enter num1:";
cin>>num;
cout<<"enter num2:"<<endl;
cin>>num2;
cout<<"the value is:"<<endl;
cout<<num/num2;}
else if(a==5){
    cout<<"choose trigonometric function"<<endl;
    cout<<"1.sine function"<<endl;
    cout<<"2.cosine function"<<endl;
    cout<<"3. tan function"<<endl;
    int b;
    cin>>b;
    if(b==1){
        cout<<"enter angle in radians";
float xx;
cin>>xx;
cout<<sin(xx);
    }
    else if(b==2){
        cout<<"enter angle in radians";
        float xx;
        cin>>xx;
        cout<<cos(xx);
    }
    else{
        cout<<"enter angle in radians";
        float xx;
        cin>>xx;
        cout<<tan(xx);

    }
}
else{float xx,yy;
    cout<<"enter base";
    cin>>xx;
    cout<<"enter power";
    cin>>yy;
    cout<<power(xx,yy);
}



















    return 0;
}
