# programmingkemsu
progi m-165
// prog125.cpp: определяет точку входа для консольного приложения.
//

#include "stdafx.h"

int zad1(float x);
int zad2(float x);
int zad5(float x);
int main()
{
	int x;
	float v,y,c,z,S;
	scanf_s("%d", &x);
	if (fabs(x) > 1) {
		printf("ZADANIE1%f\n", zad1(x));
		printf("\nZADANIE2%f\n", zad2(x));
	}
	else
	{
		c = zad5(x);
		printf("%f", c);
	}
	
    return 0;
}
int zad1(float x) {
	int n = 1;
	float S, y, u=0,eps=1.E-5,z;
	//scanf_s("%f", x);
	for (S = 1 / x, y = x; fabs(u) > eps; n++) {
		y *= x*x;
		u = 1 / ((2*n+1)*y);
		S += u;
	}
	S = 2 * S;
	z=log10((x+1)/(x-1));
	printf("z=%f\n", z);
	printf("S=%f\n", S);
	return z;
	return S;
}
	int zad2(float x) {
	int n = 1, c=1;
	float S, y, u=0, eps = 1.E-5, z;
	//scanf_s("%f", x);
	for (S = 1 - x, y = -x; fabs(u) > eps; n++) {
		y *= -x;
		c *= n + 1;
		u = y / c;
		S += u;
	}
	z = exp(-x);
	printf("exp=%f\n", z);
	printf("Summa=%f\n", S);
	return z;
	return S;
}
	int zad5(float x) {
	int n = 1;
	float S, y, u=0, eps = 1.E-5, z;
	//scanf_s("%f", x);
	for (S = x, y = x; fabs(u) > eps; n++) {
		y *= x*x;
		u = y / (2 * n + 1);
		S += u;
	}
	S = 2 * S;
	z = log10((x + 1) / (x - 1));
	printf("zad5=Z=%f\n", z);
	printf("zad5=S=%f\n", S);
	return z;
	return S;
}
