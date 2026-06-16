// You are using Java
import java.util.Scanner;

class Main{
    public static void main(String[] args){
        Scanner ip=new Scanner(System.in);
        String str;
        str=ip.nextLine();
        String rev="";
        for(int i=str.length()-1;i>=0;i--)
        {
            rev+=str.charAt(i);
        }
        System.out.println(rev);
    }
}
