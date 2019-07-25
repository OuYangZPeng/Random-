# Random-
伪随机算法可用保证不同机器同一时刻随机到相同的值

例子


RandomC randomC = new RandomC();
randomC.SetSeed(DateTime.Now.Second);
List<int> indexList = new List<int>();
indexList.Add(0);
indexList.Add(1);
indexList.Add(2);
indexList.Add(3);
for (int i = 0; i < 4; i++)
{
    int index = randomC.RandomInt(0, indexList.Count - 1);
    System.Console.WriteLine(" random =" + indexList[index]);
    indexList.RemoveAt(index);
}
