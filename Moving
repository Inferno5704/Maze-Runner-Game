public class Moving2
{
    int p1;
    int p2;
    String ary;
    double moni=0;
    double a=5;
    double wat=0;
    Reader2 rr=new Reader2();
    public Moving2(int w)
    {
        a=w;
    }
    public void input(char c,int i ,int j)
    {
        p1=i;
        p2=j;
        if(c=='W' || c=='w')
        {
            p1--;
        }
        else if(c=='A' || c=='a')
        {
            p2--;
        }
        else if(c=='d' || c=='D')
        {
            p2++;
        }
        else if(c=='S' || c=='s')
        {
            p1++;
        }
    }
    public String visible(int i, int j)
    {
        p1=i;
        p2=j;
        Printer2 pr=new Printer2();
        String str="";
        if(pr.map[p1-1][p2]==1)
        {
            str=str+"w";
        }
        if(pr.map[1+p1][p2]==1)
        str=str+"s";
         if(pr.map[p1][p2-1]==1)
        str=str+"a";
         if(pr.map[p1][1+p2]==1 || pr.map[p1][1+p2]==2)
        str=str+"d";
        return str;
    }
    public void randomGift(int tt)
    {
        if(tt==0)
        return;
        String gift="";
        int ran=(int)(Math.random()*100+1);
        if(ran>50)
        {
            double ran2=(Math.random()*100+1);
            if(ran2<1)
            {
                gift="Gold Interger Numbers";
                moni+=10000000;
            }
            else if(ran2<10)
            {
                gift="Speed Boost";
                a=0.5*a;
            }
            else if(ran2<40)
            {
               gift="Gold Coin";
               moni+=1000;
            }
            else if(ran2<70)
            {
                gift="Water";
                wat+=1;
            }

            else 
            gift="Nothing";
        }
        else
        {
            double ran2=(Math.random()*100+1);
            if(ran2<1)
            {
                gift="Coal";
                moni-=100000;
            }
            else if(ran2<10)
            {
                gift="Speed Decreaser";
                a=5*a;
            }
            else if(ran2<40)
            {
                gift="Water";
                wat+=1;
            }
            else if(ran2<70)
            {
                gift="Thorns";
                wat-=1;
            }
            else 
            gift="Nothing";
        }
        System.out.println("You Encountered "+gift);
    }
    
    public int getp1()
    {
        return p1;
    }
    public int getp2()
    {
        return p2;
    }
    public double geta()
    {
        return a;
    }
    public double getwater()
    {
        return wat;
    }
    public double getmoney()
    {
        return moni;
    }
}
