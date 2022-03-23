# Codeforcescpp-353A
#include <bits/stdc++.h>
using namespace std;

int main() {
	int n,x[101],y[101],sum_x(0),sum_y(0);
  cin >> n;
  for(int i=0;i<n;i++){
    cin >> x[i] >> y[i];
    sum_x+=x[i];
    sum_y+=y[i];
  }
  if(sum_x%2==0 && sum_y%2==0){
    cout << 0;
    return 0;
  }
  else if(sum_x%2==1 && sum_y%2==1){
    for(int i=0;i<n;i++){
      if((x[i]%2==0 && y[i]%2==1) || (x[i]%2==1 && y[i]%2==0)){
        cout << 1;
        return 0;
      }
    }
  }
  cout << -1;
	return 0;
}
