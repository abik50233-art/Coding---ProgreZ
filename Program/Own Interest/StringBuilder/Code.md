public class Main
{
	public static void main(String[] args) {
		StringBuilder sb=new StringBuilder(100);
		sb.insert(0,"Hello");
		sb.append(" Abishek");
		sb.delete(0,5);
		sb.deleteCharAt(0);
		sb.replace(0,5,"Hi");
		String str=sb.toString();
		StringBuilder sb1=new StringBuilder(str);
		System.out.println(str);
	}
}
