#include <iostream>
#include <string>
#include <vector> 
using namespace std;
string::size_type lol(const string& S, int begin, const string& lol_not)
{
	vector<int> pf(lol_not.length());
	pf[0] = 0;
	for (int k = 0, i = 1; i < lol_not.length(); ++i)
	{
		while ((k > 0) && (lol_not[i] != lol_not[k]))
			k = pf[k - 1];
		if (lol_not[i] == lol_not[k])
			k++;
		pf[i] = k;
	}

	for (int k = 0, i = begin; i < S.length(); ++i)
	{
		while ((k > 0) && (lol_not[k] != S[i]))
			k = pf[k - 1];
		if (lol_not[k] == S[i])std::cout << k <<"," <<i+1 << ",";
			k++;
		if (k == lol_not.length())
			return (i - lol_not.length() + 1);
		
	}
	return (string::npos);
	std::cout << string::npos;
}
int main()
{
	setlocale(LC_ALL, "ru");
	printf ("Введи текст:");
	string lol_not;
	cin>>lol_not;
    printf ("Введи то,что хочешь найти:");
    string ss;
    cin>>ss;
	int begin = 3;
	lol( ss, begin, lol_not);

	return 0;
}
