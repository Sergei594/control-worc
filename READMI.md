# 1 создать переменную m

Console.Write("Введите количество элементов массива:" );
int m = Convert.ToInt32(Console.ReadLine());


# 2 создать массив размером с m

string [] stringArray = new string [m];
void array(string [] stringArray)
{
  for (int i = 0;i<stringArray.Length;i++)
  {
     Console.WriteLine($"Введите {i+1} элемент массива");
     stringArray[i] = Console.ReadLine();
  }
}


# 3 создаем 2 массив требующегося размера ( 3 символа) и передаем данные из 1 массива

string [] screening(string [] stringArray)
 {
  int n = 0;
  for (int i = 0;i<stringArray.Length;i++)
  {
    if(stringArray[i].Length <=3)
    n++;
  }
  string [] rez = new string [n];
  int j = 0;
  for (int i = 0;i<stringArray.Length;i++)
  
  {
    if(stringArray[i].Length <=3)
    {
        rez[j] = stringArray[i];
        j++;
    }
      
  }
  return rez;
 }


 
# 4 делаем вывод результата и вызовы функций

void printArr(string [] stringArray)
{
    Console.Write("[");
    for (int i = 0;i<stringArray.Length;i++)
    {
    Console.Write($"{stringArray[i]} ");
    }
    Console.Write("]");
}
array(stringArray);
printArr(screening(stringArray));
