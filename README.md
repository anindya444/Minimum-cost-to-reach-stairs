# Minimum-cost-to-reach-stairs
minimum cost
minCostClimbingStairs
#include <iostream>
#include <vector>
using namespace std;
int minimumcost(vector<int>&cost,int i)
{
    if (i==1||i==0)
    return cost[i];
    return cost[i]+min(minimumcost(cost,i-1),minimumcost(cost,i-2));
}

int main()
{
  vector<int> cost= {16,19,10,12,18};
  int n=cost.size();
  cout<<min(minimumcost(cost,n-1),minimumcost(cost,n-2));
  return 0;
}
