invertir-vector
===============
#include <iostream>
#include <conio.h>
#include <math.h>
#define N 100
using namespace std;

struct vector{

	int vec[N];

 };

void cargar(int n, vector v[]){
int i,j; 
for(i=0;i<n;i++){
	for(j=0;j<n;j++){
	cout<<"ingrese vector";
	cout<<"v["<<i<<"].["<<j<<"]= ";
	cin>>v[i].vec[j];
	}
}
}
void invertir(int n, vector v[]){
int i,j,aux=0; 
for(i=0;i<n*0.5;i++){
	for(j=0;j<n;j++){
	aux=v[n-1-i].vec[n-1-j];
	v[n-1-i].vec[n-1-j]=v[i].vec[j];
	v[i].vec[j]=aux;
	}
}
}
void mostrar(int n, vector v[]){
int i,j; 
for(i=0;i<n;i++){
	for(j=0;j<n;j++){
		cout<<"v["<<i<<"].["<<j<<"]= ";
		cout<<v[i].vec[j]<<"\t";
	}
}

}
void main(){
int n;
vector v[N];
cout<<"ingrese tamano del array";
cin>>n;
cargar(n,v);
invertir(n,v);
mostrar(n,v);
getch();
}
