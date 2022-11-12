



`Console.Write("Введите колличество элементов в массиве строк: ");`

`int sizeArray = Convert.ToInt32(Console.ReadLine());`
git commit -am "Внёс изменения"

string[] FillArray(int size)    // Метод для заполнения массива
{
    string[] ArrayStr = new string[size];
    for (int i = 0; i < size; i++)
    {
        Console.Write($"Введите {i + 1} элемент массива: ");
        ArrayStr[i] = Console.ReadLine();
    }
    return ArrayStr;
}


 void PrintArray(string[] arr)   
 {
     Console.Write("[");
     for (int i = 0; i < arr.Length; i++)
     {
         Console.Write($"\"{arr[i]}\"");
     
         if (i != arr.Length - 1)
         Console.Write($", ");
     }
     Console.Write("]");
 }


Первая часть:

string[] CountingChar(string[] arr) 
{

    int sizeNewArr = 0;

    for (int i = 0; i < arr.Length; i++) 
    {
        if (arr[i].Length <= 3)
        sizeNewArr++;
    }


Вторая часть:



   if (sizeNewArr != 0)
    {
        string[] newArrayStr = new string[sizeNewArr];
        int countIndex = 0;

        for (int k = 0; k < arr.Length; k++)
        {
            if (arr[k].Length <= 3)
            {
            newArrayStr[countIndex] = arr[k];
            countIndex++;
            }
        }
        return newArrayStr;
    }

    else
    {
        string[] newArrayStr = {"В массиве нет строк, длина которых меньше или равна 3 символа"};
        return newArrayStr;
    }
}




Console.Write("Введите колличество элементов в массиве строк: ");
int sizeArray = Convert.ToInt32(Console.ReadLine());


string[] fillArray = FillArray(sizeArray);
PrintArray(fillArray);


Console.WriteLine();


string[] arrayCountingChar = CountingChar(fillArray);
Console.Write("Итоговый массив: ");
PrintArray(arrayCountingChar);