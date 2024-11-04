//TUGAS MEMBAGI GAJI SESUAI GOLONGAN

#include <iostream>
using namespace std;

int main() {
    string nama;
    int gaji, golongan, jamkerja, uanglembur, totalgaji;

    cout << "Masukkan nama anda: ";
    cin >> nama;

    cout << "Masukkan golongan anda: ";
    cin >> golongan;

    cout << "Masukkan jam kerja per minggu: ";
    cin >> jamkerja;

   if (golongan == 2) {
        gaji = jamkerja * 35000;
    } else if (golongan == 3) {
        gaji = jamkerja * 50000;
    } else {
        cout << "Golongan tidak valid." << endl;
        return 1; 
    }

    if (jamkerja > 48) {
        uanglembur = (jamkerja - 48) * 10000;
    } else {
        uanglembur = 0;
    }


   
    totalgaji=gaji+uanglembur;
    cout<< endl;
    cout << "Total Gaji " << nama << " per minggu: " << totalgaji << endl;

    return 0
}



//TUGAS MENGHITUNG MOTOR,MOBIL DI PARKIRAN UNISBA

#include <iostream>
using namespace std;
int motor,mobil,masuk,keluar,totaljam;
const int tarifmotor = 2000, tarifmobil = 5000;
int main() {
	cout << "Masukkan jumlah motor : ";
	cin >> motor;
	cout << "Masukkan jumlah mobil : ";
	cin >> mobil;
	cout << "Input jam masuk (format 24 jam) : ";
	cin >> masuk;
	cout << "Input jam keluar (format 24 jam) : ";
	cin >> keluar;
	totaljam = keluar - masuk;
	if (masuk > keluar) {
		totaljam += 24;
	}
	cout << endl;
	cout << "Total biaya parkir: Rp " << (motor * tarifmotor * totaljam) + (mobil * tarifmobil * totaljam) << " (" << totaljam << "jam)";
	return 0;
}
