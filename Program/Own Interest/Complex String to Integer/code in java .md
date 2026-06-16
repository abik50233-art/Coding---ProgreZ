// You are using Java
import java.util.Scanner;

class Main{
    public static void main(String[] args){
        Scanner ip=new Scanner(System.in);
        String c1=ip.nextLine();
        String c2=ip.nextLine();
        int r1=Integer.parseInt(c1.replaceAll("[+-]?j.*",""));
        int i1=Integer.parseInt(c1.replaceAll(".*j",""));
        if(c1.contains("-j"))
        {
            i1=(-1)*i1;
        }
        int r2=Integer.parseInt(c2.replaceAll("[+-]?j.*",""));
        int i2=Integer.parseInt(c2.replaceAll(".*j",""));
        if(c2.contains("-j"))
        {
            i2=i2*(-1);
        }
        System.out.println("real 1: "+r1);
        System.out.println("Imaginary 1: "+i1);
        System.out.println("real 2: "+r2);
        System.out.println("Imaginary 2: "+i2);
    }
}
