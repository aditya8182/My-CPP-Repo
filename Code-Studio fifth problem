bool check(vector<int> &box1)
{
    for(int i=0;i<box1.size()-1;i++)
    {
        if(box1[i]>=box1[i+1])
        {
            return 1;
        }
    }
    return 0;
}
int makeIncreasing(vector<int> &box1, vector<int> &box2)
{
  int count = 0, flag = 0;
  for (int i = 0; i < box1.size(); i++)
  {
    flag = 0;
    if ((box1[i + 1] > box1[i] && box1[i + 1] > box1[i + 2]) || box1[i + 1] == box1[i])
    {
      for (int j = 0; j < box2.size(); j++)
      {
        if (box2[j] > box1[i] && box2[j] < box1[i + 2])
        {
          box1[i + 1] = box2[j];
          count++;
          flag = 1;
          break;
        }
      }
      if (flag == 0)
      {
        for (int j = 0; j < box2.size(); j++)
        {
          if (box2[j] > box1[i] && box2[j] == box1[i + 2])
          {
            box1[i + 1] = box2[j];
            count++;
            flag = 1;
            break;
          }
        }
      }
    }
  }
  
  if(check(box1))
  {
      return -1;
  }
  else{
      return count;
  }
  
}
