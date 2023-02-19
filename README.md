x// 20-02-2023
#include <iostream>
#include <conio.h>
#include <string>
#include <iomanip>
#include <regex> 
#include <iterator> 
using namespace std;
-----------------
char  x[100] = {};
int Count, a;
char File[] = "C:\\Users\\User\\Desktop\\alice.txt";
FILE* Fa;
-----------------
int main()
{
    cout << "\t TASK 1\n";
    char  x[100] = {}, * m = 0, n;
    int l = 0;
    int a = 0;
    int i = 0;
    if ((Fa = fopen("C:\\Users\\User\\Desktop\\alice.txt", "rt")) == NULL)
    {
        puts("FILE IS NOT OPEN!");
        exit(1);
    }
    getc(Fa);
    while (!feof(Fa))
    {
        m = fgets(x, 100, Fa);
        a++;
        l += strlen(x);
    }
    cout << a << l;
    fclose(Fa);
    //------------------------------------------------------------------------------
    cout << "\t TASK 2\n";
    if ((Fa = fopen("C:\\Users\\User\\Desktop\\alice.txt", "rt")) == NULL)
    {
        cout << "FILE IS NOT OPEN!" << endl;
    }
    fread(&a, sizeof(a), 1, Fa);
    for (int i = 0; i < a; i++)
    {
        fread(&x[i], sizeof(x[i]), 1, Fa);
    }
    fclose(Fa);
    //------------------------------------------------------------------------------
    cout << "\t TASK 4\n";
    if ((Fa = fopen("C:\\Users\\User\\Desktop\\alice.txt, "rb")) == NULL)
    {
        cout << "FILE IS NOT OPEN!\n";
    }
    fwrite(&x[i], sizeof(x), 1, Fa);

    for (int i = 0; i < a + 1; i++)
        if (x[i] != a)
        {
            fwrite(&x[i], sizeof(x[i]), 1, Fa);
        }
    fclose(F_tel);
    //------------------------------------------------------------------------------
    cout << "\t TASK 3\n";
    ifstream alice("C:\\Users\\User\\Desktop\\alice.txt");
    if (alice!)
        cout << "FILE IS NOT OPEN!" << endl;
    else
    {
        int kol = 0;
        regex r("[A-a-E-W]);
        string a;
        string w;
        cout << "Enter the word - ";
        cin >> w;
        while (getline(alice, a))
        {
            regex_iterator<string::iterator> it(a.begin(), a.end(), r);
            regex_iterator<string::iterator> end;
            for (int i; i != end; i++)
            {
                if (i->a() == w)
                    k++;
            }
        }
        if (k > 0)
        {
            cout << "This word appears in the text " << k << " times";
        } 
        else 
            cout << "there is no such word in the text";
        alice.close();
    } 
    //------------------------------------------------------------------------------
}
