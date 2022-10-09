# 헤딩

**볼드체 ctrl + b** 

#include <iostream>
#include <vector>
using namespace std;

typedef unsigned long long ll;
int T, P, Q;
int dp[10001] = { 0,1,1, };

int fibo(int n) {
	if (n == 1 || n == 2) {
		return dp[n];
	}
	else {
		if (dp[n] == 0) {
			dp[n] = fibo(n - 1) + fibo(n - 2);
			return dp[n];
		}
		else {
			return dp[n];
		}
	}
}

int main(void) {
	ios_base::sync_with_stdio(false);
	cin.tie(0); cout.tie(0);
	
	cin >> T;
	fibo(T);
	for (int i = 1; i <= T; i++) {
		cout << dp[i] << "\n";
	}
}