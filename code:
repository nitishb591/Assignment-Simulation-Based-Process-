#include<iostream>
#include<cstring>
using namespace std;
void Leave(int x){
cout<<"Vehicle "<<x<<" left the intersection\n";
}
void check(int x,int y,int z){
if((x+2==0 && x+3==2)||(x+2==1 && x+3== 2)){
cout<<"Vehicle "<<z<<" entered the intersection\n";
Leave(z);
}
}
int Enter(int a,int b,int x){
if(a>2 || a < 0 || b >2 || b < 0){
cout<<"error : Invalid input !\n";
}
else if((a==0&&b==0)||(a==1&&b==1)||(a==2&&b==2)){
cout<<"U-Turn not possible !\n";
}
else if(a==1 && b==0){
cout<<"Vehicle "<<x<<" entered the intersection\n";
Leave(x);
}
else if((a==0 && b==2) || (a==1 && b==2)){
cout<<"Vehicle "<<x<<" entered the intersection\n";
Leave(x);
check(a,b,x);
}
return 1;
}
int main(){
int n,i,p,k=0;
char indir[5],outdir[5];
cout<<"Enter no of vehicles : ";
cin>>n;
p=2*n;
int a[p];
for (i=0;i< n;i++,k+=2){
cout<<"Enter the direction which it enters the intersection of vehicle "<<i+1<<" : ";
cin>>indir;
cout<<"Enter the direction which it exits the intersection of vehicle "<<i+1<<" : ";
cin>>outdir;
if(indir == " north"){
a[k]=0;}
if(strcmp(indir,"east")==0){
a[k]=1;}
if(strcmp(indir,"west")==0){
a[k]=2;}
if(outdir==" north"){
a[k+1]=0;}
if(strcmp(outdir,"east")==0){
a[k+1]=1;}
if(strcmp(outdir,"west")==0){
a[k+1]=2;}
}
for (i=0;i<p;i++){
cout<<a[i]<<"";
}cout<<endl;
for(i=0,p=0;i<n;i++,p+=2){
Enter(a[p],a[p+1],i+1);
}
return 1;
}
