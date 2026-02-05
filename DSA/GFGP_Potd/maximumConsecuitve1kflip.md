Given a binary array arr[] containing only 0s and 1s and an integer k, you are allowed to flip at most k 0s to 1s. Find the maximum number of consecutive 1's that can be obtained in the array after performing the operation at most k times.

Examples:

Input: arr[] = [1, 0, 1], k = 1
Output: 3
Explanation: By flipping the zero at index 1, we get the longest subarray from index 0 to 2 containing all 1’s.
Input: arr[] = [1, 0, 0, 1, 0, 1, 0, 1], k = 2
Output: 5
Explanation: By flipping the zeroes at indices 4 and 6, we get the longest subarray from index 3 to 7 containing all 1’s.
Input: arr[] = [1, 1], k = 2
Output: 2
Explanation: Since the array is already having the max consecutive 1's, hence we dont need to perform any operation. Hence the answer is 2.

my code
brute forse hune sub hi arry generte kr di

class Solution {
    public int maxOnes(int arr[], int k) {
        // code here
        int n=arr.length;
        int ans=0;
        for(int i=0;i<n;i++){
            int t=k;
            int count=0;
           int tmp[] = Arrays.copyOf(arr, n);

            for(int j=i;j<n;j++){
                if( count<k&&tmp[j]==0){
                    tmp[j]=1;
                   // System.out.println(tmp[j]);
                    count++;
                }
            }
              for(int f=0;f<n;f++){
            //  System.out.println(tmp[f]);
            }
                         // System.out.println("............");
            int tmpans=0,fans=0;
            int chk=0;
            for(int f=0;f<n-1;f++){
                if(tmp[f]==1||tmp[f+1]==1){chk=1;}
                if(tmp[f]==1&& tmp[f+1]==1){
                    //  System.out.println("conse");
                    tmpans++;
                     fans=Math.max(fans,tmpans);
                    
                }
                else{tmpans=0;}
            }
            if(fans>0){fans=fans+1;};
            if(fans==0 && chk==1){fans=1;}
            
            ans=Math.max(fans,ans);
            
        }
        if(n==1 && arr[0]==1)return 1;
      //  if(ans>0)return ans+1;
        return ans;
    }
}class Solution {
    public int maxOnes(int arr[], int k) {
        // code here
        int n=arr.length;
        int ans=0;
        for(int i=0;i<n;i++){
            int t=k;
            int count=0;
           int tmp[] = Arrays.copyOf(arr, n);

            for(int j=i;j<n;j++){
                if( count<k&&tmp[j]==0){
                    tmp[j]=1;
                   // System.out.println(tmp[j]);
                    count++;
                }
            }
              for(int f=0;f<n;f++){
            //  System.out.println(tmp[f]);
            }
                         // System.out.println("............");
            int tmpans=0,fans=0;
            int chk=0;
            for(int f=0;f<n-1;f++){
                if(tmp[f]==1||tmp[f+1]==1){chk=1;}
                if(tmp[f]==1&& tmp[f+1]==1){
                    //  System.out.println("conse");
                    tmpans++;
                     fans=Math.max(fans,tmpans);
                    
                }
                else{tmpans=0;}
            }
            if(fans>0){fans=fans+1;};
            if(fans==0 && chk==1){fans=1;}
            
            ans=Math.max(fans,ans);
            
        }
        if(n==1 && arr[0]==1)return 1;
      //  if(ans>0)return ans+1;
        return ans;
    }
}