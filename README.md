#include<iostream>
using namespace std;

class SumAvg {
    private:
int n;
        double sum; 
        double avg; 
    public:
    
        SumAvg() {
            sum = 0;
            avg = 0;
        }

        friend void calcSumAvg(SumAvg& obj, int n);

        void display() {
            cout << "Sum of " << n << " numbers: " << sum << endl;
            cout << "Average of " << n << " numbers: " << avg << endl;
        }
};

void calcSumAvg(SumAvg& obj, int n) {
    int i, a;
    for (i = 0; i < n; i++) {
        cout << "Enter the number " << i + 1 << ": ";
        cin >> a;
        obj.sum += a; 
    }
    obj.avg = obj.sum / n;
}

int main() {
    int n;
    cout << "\nEnter the number of elements: " << endl;
    cin >> n;
    SumAvg obj; 
    calcSumAvg(obj, n); 
    obj.display(); 
    return 0;
}
# Average-of-numbers
