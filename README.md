//# Task7...
#include <string.h>
#include <cstdlib>
#include <iostream>
#include <fstream>
#include <string>
#include <cstring>
 
using namespace std;
 
int main()
 {
    
    setlocale(  LC_ALL, "" );
    int i; //объявляем переменную
    cout << "Введите текст который хотите разбить" <<endl;
    char str[1000]; //объявляем массив символов
    cin.get(str, 999);
    for (i=0;i!=strlen(str);i++) //цикл прогоняется от первого до последнего символа массива text
        if ((str[i]=='.' || str[i]=='!' || str[i]=='?' ))
        {
            cout<< str[i];
            cout << endl;
                    
        }
        else
            cout << str[i];
system("pause");
return 0;
}

int amain()
{
    setlocale(  LC_ALL, "rus" );
    int i;
    std::string line;
    std::ifstream in(" mim.txt "); // окрываем файл для чтения
    if (in.is_open())
    {
        while (getline(in, line))
        {
         //   for (i=0;i!=strlen(line);i++) //цикл прогоняется от первого до последнего символа массива text
                   if ((line[i]=='.' || line[i]=='!' || line[i]=='?' ))
                   {
                       cout<< line[i];
                        cout << endl;
                                
                   }
                    else
                       cout << line[i];
            
        }
    }
    in.close();     // закрываем файл
    std::cout << "Конец программы" << std::endl;
    return 0;
}

int menu()
{
    while (true)
    {
        float check;
        cout << "Хотите произвести расчет? (произвести расчет для первого задания: 1, произвести расчет для второго задания: 2, непроизводить расчет: 0) ";
        cin >> check;

        if (check == 0) break;
        else if (check == 1) main();
        else if (check == 2) amain();
        else
        {
            cout << "Введено не коректное значение, попробуйте снова" << endl;
        }
    }
}

int tmain()
{
    setlocale(0,"");
    menu();
}
