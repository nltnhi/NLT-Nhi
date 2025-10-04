#include <iostream>
using namespace std;

int a[100];

int demSoLuongPhanTuKhacNhau(int n){
	int dem = 0;
	for (int i = 0; i < n; i++) {
	    bool daCo = false;
	    for (int j = 0; j < i; j++) {
	        if (a[i] == a[j]) {
	            daCo = true;
	            break;
	        }
	    }
	    if (!daCo)
	        dem++;
	}
	return dem;
}
int main(){
	int n;
	cout<<"Nhap so phan tu: ";
	cin>>n;
	cout<<"\nNhap cac phan tu: ";
	for (int i = 0; i < n; i++){
		cin>>a[i];
	}
	cout<<"Ket qua: "<<demSoLuongPhanTuKhacNhau(n);
	return 0;
}
