#include <iostream>
#include <string>
#include<math.h>
using namespace std;
float totsigmaX1, totsigmaY1, kuadratX, kuadratY, totsigmaX1Y, total,  sigmaXY, kuadratXtotal, kuadratYtotal, r;
int main(){
	int jumlah, x[50], y[50];
	cout << "masukan data: ";cin >> jumlah;	
	for (int i=0;i<jumlah;i++){
		cout << "Data "<<i+1<<". "<<endl;
		cout << "X: ";cin >> x[i];
		if (x==0){
		cout << "MASUKAN BILANGAN YANG SAMA ATAU LEBIH DARI 0"<<endl;
		}
		cout << "Y: ";cin >> y[i];

		if (y==0){
			cout << "MASUKAN BILANGAN YANG SAMA ATAU LEBIH DARI 0"<<endl;
		}
		totsigmaX1=totsigmaX1+x[i];
		totsigmaY1=totsigmaY1+y[i]; 
		sigmaXY=x[i]*y[i];
		kuadratX=pow(x[i],2);
		kuadratXtotal=kuadratXtotal+kuadratX;
		kuadratY=pow(y[i],2);
		kuadratYtotal=kuadratXtotal+kuadratY;
		cout << "Total Sigma XY: " << sigmaXY << endl;
		total = total+sigmaXY;
	}
	totsigmaX1Y=totsigmaX1+totsigmaY1;
	cout << "Sigma X: " << totsigmaX1 <<	endl;
	cout << "Sigma Y: " << totsigmaY1 <<	endl;
	cout << "Sigma X+Y: "<< totsigmaX1Y << endl;
	cout << "X kuadrat: " << kuadratX << endl;
	cout << "Total sigma X*Y: "<< total << endl;
	r= (total-totsigmaX1Y)/sqrt(kuadratXtotal)-pow(totsigmaX1,2)*sqrt(kuadratYtotal)-pow(totsigmaY1,2);
	cout << "niali korelasi r: " << r << endl;
	cout << "Nilai koefisien determinasi :" << pow(r,2)*50/50 << endl;
	if (r>0){
		cout << "Hubungan Antara Variabel X dan Y adalah positif, dimana jika nilai X bertambah, maka nilai Y pun bertambah sebaliknya, dan juga sebaliknya" << endl;
	}else if (r<0){
		cout << "Hubungan Antara Variabel X dan Y adalah negatif, dimana jika X bertambah, maka nilai Y oun mengecil, dan juga sebaliknya" << endl;
	}else if (r=0){
		cout << "Tidak ada hubungan antara Variable X dan Y" << endl;
	}
	}
		
		
float sigmaXYs(int _X, int _Y){
	float hasil=0;
	hasil = _X*_Y;
	return hasil;
}
