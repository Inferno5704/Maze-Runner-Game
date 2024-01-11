public class Printer2 
{
    int map[][];
    int p1;
    int p2;
    Reader2 rr=new Reader2();
    public void startMenu()
    {
        System.out.println("\f**********************************************************************************************************************************************************************************************************************************");
        System.out.println("                                            Maze Runner ");
        System.out.println("**********************************************************************************************************************************************************************************************************************************");
        System.out.println("                              ");
        System.out.println("                                      1.Start the Maze");
        System.out.println("                                           2.Help ");
        System.out.println("                              ");
        System.out.println("***********************************************************************************************************************************************************************************************************************************");
    }
    public Printer2()
    {
         int mapp[][]={{0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0},
                       {0,0,0,0,0,0,1,0,0,0,0,0,0,0,0,0,0},
                       {0,1,1,1,1,1,1,0,1,1,0,1,1,1,0,0,0},
                       {0,1,0,1,0,0,0,0,0,1,0,1,0,1,1,1,0},
                       {0,1,0,1,0,1,1,1,0,1,0,1,0,1,0,1,0},
                       {0,1,0,1,0,1,0,0,0,1,0,1,0,1,0,1,0},
                       {0,1,0,1,0,1,1,1,1,1,0,1,0,1,0,1,0},
                       {0,1,0,1,0,0,1,1,1,0,0,1,0,1,0,1,0},
                       {0,1,0,1,0,0,1,0,1,0,1,1,0,1,0,1,0},
                       {0,1,0,1,0,0,1,0,1,0,0,1,0,1,0,1,0},
                       {0,1,0,1,1,1,1,0,1,1,0,1,0,1,0,1,0},
                       {0,1,0,1,0,0,1,0,1,0,0,1,0,1,0,0,0},
                       {0,0,1,1,0,1,1,0,1,1,1,1,0,1,1,1,0},
                       {0,0,0,1,0,1,0,1,1,0,0,1,0,1,0,0,0},
                       {0,1,1,1,0,1,0,1,0,1,1,1,0,1,1,1,2},
                       {0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0,0}};
             map=mapp;
    }
    
    public void direction(int e,int j)
    {
        p1=e;
        p2=j;
        Moving2 mm=new Moving2(25);
        String str=mm.visible(p1,p2);
        for(int i=0;i<str.length();i++)
        {
            char ch=str.charAt(i);
            if(ch=='a')
            System.out.println("Left Door is Open");
            else if(ch=='s')
            System.out.println("Bottom Door is Open");
            else if(ch=='d')
            System.out.println("Right Door is Open");
            else if(ch=='w')
            System.out.println("Top Door is Open");
        }
    }
    public int movement(char ch,int i,int j,int no)
    {
        p1=i;
        p2=j;
        if(no==0 || no==4){
        switch(ch)
                {
                    case 'a':
                        System.out.println("You dashed into the Left Wall and wasted a Turn");p2++;
                        break;
                    case 's':
                        System.out.println("You dashed into the Bottom Wall and wasted a Turn");p1--;
                        break;
                    case 'd':
                        System.out.println("You Dashed into the Right Wall and Wasted a Turn");p2--;
                        break;
                    case 'w':
                        System.out.println("You Dashed into the Top Wall and Wasted a Turn");p1++;
                        break;
                    default:
                        System.out.println("Invalid Movement and Wasted a Turn");
                        return 0;
                }}
        else if(no==1)
        {
            switch(ch)
                {
                    case 'a':
                        System.out.println("You Dashed the Left Door");
                        break;
                    case 's':
                        System.out.println("You Dashed the Bottom Door");
                        break;
                    case 'd':
                        System.out.println("You Dashed into the Right Door");
                        break;
                    case 'w':
                        System.out.println("You Dashed into the Top Door");
                        break;
                    default:
                        System.out.println("Invalid Movement and Wasted a Turn");
                        return 1;
                }
        }
        else if(no==2)
        {
            System.out.println("You Won");
            return 99;
        }
        return 1;
    }
    public int getp1()
    {
        return p1;
    }
    public int getp2()
    {
        return p2;
    }
    public void print(int k,int l)
    {
        p1=k;
        p2=l;
        Printer2 pr=new Printer2();
              System.out.println("\f**********************************************************************************************************************************************************************************************************************************");
        System.out.println("                                            Maze Runner ");
        System.out.println("**********************************************************************************************************************************************************************************************************************************");
        for(int i=0;i<pr.map.length;i++)
        {
            for(int j=0;j<pr.map[i].length;j++)
            {
            {
                String str="";
                if(pr.map[p1-1][p2]==0)
                    map[p1-1][p2]=4;
                if(pr.map[1+p1][p2]==0)
                    map[1+p1][p2]=4;
                if(pr.map[p1][p2-1]==0)
                    map[p1][p2-1]=4;
                if(pr.map[p1][1+p2]==0)
                    map[p1][1+p2]=4;
                }
                if(p1==i && p2==j)
                System.out.print("@  ");
                else if(map[i][j]==2)
                System.out.print("^  End");
                else if(map[i][j]==3)
                System.out.print("#  ");
                else if(map[i][j]==4)
                System.out.print("|  ");
                else
                System.out.print("^  ");
                map[p1][p2]=3;
                
            }
            System.out.println();
        }
    }
    public void time(double a)
    {
        for(double i=0.1;i<10000000*a;i+=0.1);
        System.out.println("\f");
    }
    public void walls(int i,int j)
    {
        p1=i;
        p2=j;
        Printer2 pr=new Printer2();
        String str="";
        if(pr.map[p1-1][p2]==0)
        {
            pr.map[p1-1][p2]=4;
        }
        if(pr.map[1+p1][p2]==0)
        pr.map[1+p1][p2]=4;
        if(pr.map[p1][p2-1]==0)
        pr.map[p1][p2-1]=4;
         if(pr.map[p1][1+p2]==0)
        pr.map[p1][1+p2]=4;
    }
}
