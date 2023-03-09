# minimize-sum
class Solution {
public:
    int minimizeSum(int N, vector<int> arr) {
        // code here
        int sum=0;
      priority_queue<int,vector<int>,greater<int>>pq;
   
   for(int i=0;i<N;i++){
          pq.push(arr[i]);
      }
      while(pq.size()>1)
      {
          int x=pq.top();
          pq.pop();
          int y=pq.top();
          pq.pop();
          sum+=x+y;
          pq.push(x+y);
      }
      return sum;
    }
