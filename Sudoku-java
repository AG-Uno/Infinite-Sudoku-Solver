//java

//ADITYA GUHA

import java.io.*;
class Sudoku
{private int []a;
 private long count;
 public Sudoku()
  {a=new int[81];
   count=0;
  }
 int check(int i)
  {int p,j,q,k;
  //row check
  p=i/9;
  for(j=0;j<9;j++)
   {q=p*9+j;
    if(q!=i&&a[q]==a[i])
      return 0;
   }
   //column check
   p=i%9;
   for(j=0;j<9;j++)
   {q=p+j*9;
    if(q!=i&&a[q]==a[i])
      return 0;
   }
   //square check
   p=(i/27)*27+((i%9)/3)*3;
   for(j=0;j<3;j++)
    {for(k=0;k<3;k++)
      { q=p+9*j+k;
      if(q!=i&&a[q]==a[i])
      return 0;
      }
    }
   return 1;
 }
 void fillUp(int p)throws IOException//recursive
  {BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
   int i;
   while(p<81&&a[p]!=0)//find next 0
   p++;
   if(p<81)
    {for(i=1;i<10;i++)
      {a[p]=i;//fill
       if(check(p)==1)
        fillUp(p+1);
       //else
        a[p]=0;//undo change
    }
   }
   else//sudoku complete
    {System.out.print("\f");
    System.out.print("SOLUTION NO."+(++count)+"\n\n");
    for(i=1;i<=81;i++)
     {System.out.print(a[i-1]+"	");//output
      if(i%9==0)//nxt line
       System.out.print("\n\n");
      }
    br.readLine();
   }
  }
 void get()throws IOException
  {BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
   count=0;
   int i,j,p=0;
   String w="";
   System.out.print("THE SUDOKU IS TO BE INPUTTED LINE BY LINE:::\n");
   System.out.println("\nTHE PROGRAM WILL TAKE IN VALUES AS CLUES AND \nEMPTY SPACES/BLANKS AS 0");
   System.out.println("FOR EXAMPLE: 025689000 IS A VALID INPUT.(NOTE THAT INPUT IS LINE BY LINE.)\n");
   System.out.println("THIS IS UNIQUE BECAUSE IT OUTPUTS \"ALL POSSIBLE SOLUTIONS\" \nTO A GIVEN SUDOKU");
   System.out.println("IN FACT IF AN EMPTY GRID IS INPUTTED, IT PROVIDES SOLUTIONS TO ALL THE POSSIBLE SUDOKUS...\nWITHOUT CRASHING!!!");
   System.out.println("IF YOU HAVE THE TIME, JUST KEEP PRESSING ENTER!");
   for(i=1;i<=9;i++)
    {System.out.print("Enter line"+i+"	");//take as string
    w=br.readLine();
    for(j=0;j<9;j++)//put them in a linear array
     a[p++]=w.charAt(j)-48;
    }
 }
 void main() throws IOException
  {Sudoku a=new Sudoku();
   a.get();
   a.fillUp(0);//to start
  }
}
//THE END
