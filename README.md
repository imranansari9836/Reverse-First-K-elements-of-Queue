# Reverse-First-K-elements-of-Queue
#Reverse First K elements of Queue#Input: k= 3 
1 2 3 4 5

class GfG {
    // Function to reverse first k elements of a queue.
    public Queue<Integer> modifyQueue(Queue<Integer> q, int k) {
        // add code here.
        int n=q.size();//5
        Stack<Integer>st=new Stack<>();
        for(int i=0;i<k;i++)
        {
            st.push(q.poll());
        }
        while(!st.isEmpty())
        {
            q.add(st.pop());//4 5 3 2 1
        }
        for(int i=0;i<n-k;i++)
        {
           q.add(q.poll());
        }
        return q;
    }
}

