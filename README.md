#include <iostream>

using namespace std;

class PassportChecker
{
private:
    static int next; 
 
public:
     static int checknextpassport(); 
};
 

int PassportChecker::next{ 1 };
 

int PassportChecker::checknextpassport() { return next++; } 
 
int main()
{
    for (int count{ 0 }; count < 5; ++count)
        std::cout << "The next Passport is: " << PassportChecker::checknextpassport() << '\n';
 
    return 0;
}
