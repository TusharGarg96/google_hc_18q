# google_hc_18q
import java.util.*;
public class NewClass {
    public static void main(String args[])
    {
        Scanner s=new Scanner(System.in);
        int r=s.nextInt();
        int c=s.nextInt();
        int[][] grid=new int[r][c];
        int F=s.nextInt();        //vechials
        int N=s.nextInt();         //Ride
        int B=s.nextInt();        //Bonus
        int T=s.nextInt();           //Number of steps
        int[] v=new int[F];
        for(int i=0;i<F;i++)
        {v[i]=grid[0][0];}
      
        
        int[] a=new int[r];
         int[] b=new int[r];
          int[] x=new int[r];
          int[] count=new int[r];
           int[] y=new int[r];
            int[] s1=new int[r]; //early step
             int[] f=new int[r];  //finishing step
            
             
             for(int i=0;i<N;i++)
             
             {a[i]=s.nextInt();
            b[i]=s.nextInt();
            x[i]=s.nextInt();
            y[i]=s.nextInt();
            s1[i]=s.nextInt();
            f[i]=s.nextInt();
            count[i]=0;
             }
            
             int sum=0;
             for(int i=0;i<N;i++)
             { while(count[i]<s1[i])
             {count[i]=count[i]+1;
             }
             }int res;
             for(int i=0;i<N;i++)
              {int n; int d;
              n=a[i]-x[i];
              d=b[i]-y[i];
              res=Math.abs(n)+Math.abs(d);
              sum=res+count[i];
             }
             System.out.println(sum);
    }
}
