# Seminar012923
Домашняя работа №2 к семинару "Знакомство с языками программирования" 

# Задача 10: Напишите программу, которая принимает на вход трёхзначное число и на выходе показывает вторую цифру этого числа.
```
Console.Clear();
Console.WriteLine("Введите трёхзначное число n: ");
int n = Convert.ToInt32(Console.ReadLine());

while ((n<100) || (n>=1000))
{
    Console.Write("Вы ошиблись!\nВведите трёхзначное число n: ");
    n = Convert.ToInt32(Console.ReadLine());
}
int result = (n / 10) % 10;
Console.WriteLine($"{n} -> {result} ");
```

# Задача 13: Напишите программу, которая выводит третью цифру заданного числа или сообщает, что третьей цифры нет.
```
Console.Clear();
Console.WriteLine("Введите число n: ");
int n = Convert.ToInt32(Console.ReadLine());
int d = n;
if (n < 100)
    Console.WriteLine($"{n} -> третьей цифры нет ");
else
{
    while (n > 999)
    {
        n = n / 10;
    }
    int result = n % 10;
    Console.WriteLine($"{d} -> {result} ");
}
```

# Задача 15: Напишите программу, которая принимает на вход цифру, обозначающую день недели, и проверяет, является ли этот день выходным.
```
Console.Clear();
Console.WriteLine("Введите цифру, обозначающую день недели: ");
int n = Convert.ToInt32(Console.ReadLine());

while ((n < 1) || (n >= 8))
{
    Console.Write("Вы ошиблись!\nВведите цифру, обозначающую день недели: ");
    n = Convert.ToInt32(Console.ReadLine());
}
if (n < 6)
    Console.WriteLine($"{n} -> нет ");
else
    Console.WriteLine($"{n} -> да ");
```

# Дополнительная задача (https://acmp.ru/asp/do/index.asp?main=task&id_course=1&id_section=3&id_topic=35&id_problem=223)
```
Console.Clear();
int n = Convert.ToInt32(Console.ReadLine());
int m1 = 0;
int m2 = 0;
string s = "";
while (n != 0)
{
    if (n >= m1)
    {
        m2 = m1;
        m1 = n;
    }
    else if ((m2 < n) & (n < m1))
        m2 = n;

    s = s + ($"{n} ");
    n = Convert.ToInt32(Console.ReadLine());
}
Console.WriteLine($"{s} -> {m2} ");
```
