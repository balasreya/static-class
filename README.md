# static-class
class usestatic
{
    static int a=3;
    static float b;
    int c=9;
    static void met1()
   {
       System.out.println("static method 1");
       System.out.println("enter the value of a"+a);
       System.out.println("enter the value of b"+b);
   }
   void met2()
   {
       System.out.println("non-static method 2");
       System.out.println("enter the value of c"+c);
   }
   static
   {
       System.out.println("in static block");
       b=a*64;
   }
   static class nested
   {
       void met3()
       {
           System.out.println("non-static nested class method 3");
           System.out.println("enter the value of a"+a);
           System.out.println("enter the value of b"+b);
           
       }
       void met4()
       {
           System.out.println("in static method of nested class");
       }
       
   }
}
class Main
{
    public static void main(String[]args)
    {
        usestatic.met1();
        usestatic s=new usestatic();
        s.met1();
        s.met2();
        usestatic.nested o=new usestatic.nested();
        o.met3();
        o.met4();
    }
}
       
