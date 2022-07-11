import java.util.*;
public class Stack{
    int size;
    int array[];
    int top;
    int capacity;
        
        Stack(int n){
            array=new int[n];
            size=n;
            top= -1;
            capacity=size;
        }
   
    public void  push(int x){
        if(isFull()){
            System.out.println("stack is full");
            System.exit(1);
        }
        else{
            array[++top]=x;
            System.out.println("pushed  into the stack is:"+x);
            
        }
    }
    //pop elements from top of the stack
    public int pop(){
        if(isEmpty()){
            System.out.println("stack is empty you can't pop: ");
        }
        return array[top--];
    }
    //check if the stack is empty
     public Boolean isEmpty() {
    return top == -1;
  }

  // Check if the stack is full
  public Boolean isFull() {
    return top == capacity - 1;
  }


    
    void display(){
        for(int i=0;i<=top;i++){
            System.out.println(array[i]);
        }
    }
    public static void main(String args[]){
        Stack stack=new Stack(7);
        Scanner sc=new Scanner(System.in);
        for(int i=0;i<5;i++){
            int x=sc.nextInt();
            stack.push(x);
        }
        
        
        
        stack.display();
    }
}
