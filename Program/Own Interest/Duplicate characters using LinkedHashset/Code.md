import java.util.LinkedHashSet;
import java.util.Scanner;

class Main{
    public static void main(String[] args){
        Scanner ip=new Scanner(System.in);
        String str=ip.nextLine();
         LinkedHashSet<Character> seen=new LinkedHashSet<>();
         LinkedHashSet<Character> duplicate=new LinkedHashSet<>();
         
         for(int i=0;i<str.length();i++)
         {
            char ch=str.charAt(i);
            
            if(!seen.add(ch)){
                duplicate.add(ch);
            }
         }
         
         System.out.println("Seen: "+seen);
         System.out.println("Duplicate: "+duplicate);
    }
}
