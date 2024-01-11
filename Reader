import java.util.Scanner;
public class Reader2
{
    String name;
    int p1=1;
    int p2=6;
    double moni=0;
    int w;
    public void read()
    {
        Scanner sc=new Scanner(System.in);
        Printer2 pr=new Printer2();
        if(w==0)
        {
            System.out.println("Enter the Movement Speed of the Text");
            System.out.println("1-Fast");
            System.out.println("2-Medium");
            System.out.println("3-Slow");
            int tt=sc.nextInt();
            w=speed(tt);
        }
        Moving2 mr=new Moving2(w);
        pr.startMenu();
        int choice=sc.nextInt();
        int n=0;
        if(choice==1)
        {
               System.out.println("\fEnter the Player's Name");
               sc=new Scanner(System.in);
               name=sc.nextLine();
               char cho=' ';
               sc=new Scanner(System.in);
               int t=1;
               double a;
               System.out.println(name+" is Embarking on a Journey to Find the Hidden Treasure in the Temple of Java");
               while(cho!='/' || t!=2)
               {
                   a =mr.geta();
                   pr.time(a);
                   pr.print(p1,p2);
                   pr.direction(p1,p2);
                   p1=pr.getp1();
                   p2=pr.getp2();
                   cho=sc.next().charAt(0);
                   if(cho=='/')
                   break;
                   else if(cho==';')
                   a=0.005*a;
                   else if(cho=='h' || cho=='H')
                   {
                     rules();
                     continue;
                   }
                   mr.input(cho,p1,p2);
                   p1=mr.getp1();
                   p2=mr.getp2();
                   
                   pr.movement(cho,p1,p2,pr.map[p1][p2]);
                   mr.randomGift(pr.map[p1][p2]);
                   p1=pr.getp1();
                   p2=pr.getp2();
                   t=pr.map[p1][p2];
                   if(t==2)
                   break;
                   n++;
               }
               if(cho=='/')
               {
                   System.out.println("You Gave Up ");
                   System.out.println("You Found "+mr.getmoney()+" Money");
               }
               
               if(t==2)
               {
                   System.out.println("You Won the Got the Treasure of Java -The Book of Programming and Shortcut");
                   System.out.println("You Found "+(mr.getmoney()+50000)+" Money");
               }
                
               
               System.out.println("You Found "+mr.getwater()+" Litres of Water");
               System.out.println("Number of Turns Taken "+n);
        }
        else if(choice==2)
        {
            rules();
            read();
        }
    }
    public int speed(int tt)
    {
        if(tt==1)
        return 1;
        else if(tt==2)
        return 10;
        else if(tt==3)
        return 25;
        else
        {
            System.out.println("Invalid input. Text Speed set to Medium");
            return 10;
        }
    }
    public static void main(String[]arg)
    {
        Reader2 rr=new Reader2();
        rr.read();
    }
    public void rules()
    {
        System.out.println("You are about to enter the maze and the path is hidden ");
            System.out.println("@ represent the location at which the Character is located at ");
            System.out.println("^ represents the Rooms of the temple the room can either be a filled with stones or be empty to walk in");
            System.out.println("# represent the path already taken by the Character");
            System.out.println("| represent the Walls already seen by the Character");
            System.out.println("Movements");
            System.out.println("w-Top");
            System.out.println("a-Left");
            System.out.println("d-Right");
            System.out.println("s-Bottom");
            System.out.println("You can get to know which Door is open by the message given below the maze about which door is open");
            System.out.println("You get a random gift every turn, like gold which is valuable or coal which can reduce the prize");
            System.out.println("You can exit the temple by using /");
            System.out.println("Enter h for the Rules to Reappear");
            System.out.println("Enter any key to exit");
            Scanner sc=new Scanner(System.in);
            sc.next();
    }
}
