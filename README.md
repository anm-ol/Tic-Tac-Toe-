\\# Tic-Tac-Toe-
\\Creating a program in java to play Tic Tac Toe  .
import java.util.Scanner;
public class tic_array
{
    static int[] win(int t[])
    { int comb[][] = {{1,2,3},{4,5,6},{7,8,9},{1,4,7},{2,5,8},{3,6,9},{1,5,9},{3,5,7}} ;
    int w1=0,w2=0,i,j,k,d;
    for(i=0;i<8;i++)
    {
        w1=0;w2=0;
        for(j=0;j<3;j++)
        {
            d= comb[i][j];
            if(t[d-1]==1)
             w1++;
            if(t[d-1]==2)
             w2++;
            
        }
    if(w1==3 || w2==3)
    break;}
    int win[]= new int[2];
    win[0]= w1;win[1]=w2;
    return win;
    }    
    public static void main()
{Scanner sc = new Scanner(System.in);
System.out.println("hey.....");
int t[],i,j,b,u,c=0;
t = new int[9];
for(b=1;b<10;b++)
{
    u = sc.nextInt() ;
    t[u-1] = b%2==1?1:2;
    c=0;
    for(i=1;i<=3;i++)
    {
     for(j=1;j<=3;j++)
     {
        if(t[c]==0)
        System.out.print(" - ");
        else if(t[c]==1)
        System.out.print(" X ");
        else if(t[c]==2)
        System.out.print(" O ");
        c++;
     }System.out.println();
  }
   if(tic_array.win(t)[0] == 3 || tic_array.win(t)[1] == 3)
   {   if(tic_array.win(t)[0] == 3)
       System.out.println("Player 1 won");
       if(tic_array.win(t)[1] == 3)
       System.out.println("Player 2 won");
       break;
    }
}
}
}  
