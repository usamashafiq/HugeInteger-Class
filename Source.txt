#include<iostream>
using namespace std;
class hugeint {
private:
	int ar1[5], ar2[5];
public:
	void input(int[], int[]);
	void output();
	void add();
	void sub();
	bool isequalto();
	bool isnotequalto();
	bool isgreaterthan();
	bool islessthan();
	bool isgreaterthanorequal();
	bool islessthanorequal();
};
int main() {
	int a1[5], a2[5];
	cout << "enter first huge number :" << endl;
	for (int i = 0; i<5; i++) {
		cin >> a1[i];
	}
	cout << "enter second huge number: " << endl;
	for (int i = 0; i<5; i++) {
		cin >> a2[i];
	}
	hugeint h;
	h.input(a1, a2);
	h.output();
	h.add();
	h.sub();
	if (h.isequalto() == true) {
		cout << "the two huge numbers are equal" << endl;
	}
	if (h.isnotequalto() == true) {
		cout << "two huge numbers are not equal" << endl;
	}
	if (h.isgreaterthan() == true) {
		cout << "First huge number is greater than the second" << endl;
	}
	if (h.islessthan() == true) {
		cout << "First huge number is less than the second" << endl;
	}
	if (h.isgreaterthanorequal() == true) {
		cout << "First huge number is greater than or equal to second huge number" << endl;
	}
	if (h.islessthanorequal() == true) {
		cout << "first huge number is less than or equal to the second" << endl;
	}
	system("pause")
	return 0;
}
void hugeint::input(int a1[5], int a2[5]) {
	for (int i = 0; i<5; i++) {
		ar1[i] = a1[i];
	}
	for (int i = 0; i<5; i++) {
		ar2[i] = a2[i];
	}
}
void hugeint::output() {
	cout << "first huge number is: " << endl;
	for (int i = 0; i<5; i++) {
		cout << ar1[i] << endl;
	}
	cout << "second huge number is: " << endl;
	for (int i = 0; i<5; i++) {
		cout << ar2[i] << endl;
	}
}
void hugeint::sub() {
	cout << "subtraction of the entered huge numbers is: " << endl;
	for (int i = 0; i<5; i++) {
		cout << ar1[i] - ar2[i] << endl;
	}
}
bool hugeint::isequalto() {
	bool check = true;
	for (int i = 0; i<5; i++) {
		if (ar1[i] == ar2[i]) {
			check = true;
		}
		else
			return false;
	}
	return check;
}
bool hugeint::isnotequalto() {
	bool check = true;
	for (int i = 0; i<5; i++) {
		if (ar1[i] == ar2[i]) {
			check = false;
		}
		else
			return true;
	}
	return check;
}
void hugeint::add() {
	cout << "addition of the entered huge numbers is: " << endl;
	for (int i = 0; i<5; i++) {
		cout << ar1[i] + ar2[i] << endl;
	}
}
bool hugeint::isgreaterthan() {
	bool check = true;
	for (int i = 0; i<5; i++) {
		if (ar1[i]>ar2[i]) {
			check = true;
		}
		else
			return false;
	}
	return check;
}
bool hugeint::islessthan() {
	bool check = true;
	for (int i = 0; i<5; i++) {
		if (ar1[i]<ar2[i]) {
			check = true;
		}
		else
			return false;
	}
	return check;
}
bool hugeint::isgreaterthanorequal() {
	bool check = true;
	for (int i = 0; i<5; i++) {
		if (ar1[i]>ar2[i] || ar1[i] == ar2[i]) {
			check = true;
		}
		else
			return false;
	}
	return check;
}
bool hugeint::islessthanorequal() {
	bool check = true;
	for (int i = 0; i<5; i++) {
		if (ar1[i] == ar2[i] || ar1[i]<ar2[i]) {
			check = true;
		}
		else
			return false;
	}
	return check;
}
