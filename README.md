# Birth-Day-of-the-Week
To find the Birth Day of the week by using Java. By entering the date, month, and Year we can calculate the day of the week in which you born.

import java.util.Scanner;

class person{
	
	public void personInfo(String month) {
		System.out.println("Month - "+ month);
		
	}
	
	public void personInfo(byte day) {
		System.out.println("Day - "+day);
		
	}
	
	public void personInfo(int year) {
		System.out.println("Year - "+year);
	}
	
	
	
	
}
class calculation extends person{
	byte day;
	byte g;
	String month;
	int a;
	int b;
	int d;
	int f;
	int jan,feb,mar,apr,may,jun,jul,aug,sep,oct,nov,dec;
	int year;
	int output;
	int week;
	
	public void personInfo(byte day) {
		byte g=day;
		Byte h = new Byte(g);
		output = h.intValue();
//		System.out.println(output);
	}
	
	public void personInfo(int year) {
		
		if(year>=1600 && year<=1699) {
			a=6;
			year=year%100;
			b=year/4;
			
		}
		else if(year>=1700 && year<=1799) {
			a=4;
			year=year%100;
			b=year/4;
			
		}
		else if(year>=1800 && year<=1899) {
			a=2;
			year=year%100;
			b=year/4;
			
		}
		else if(year>=1900 && year<=1999) {
			a=0;
			year=year%100;
			b=year/4;
			
		}
		else if(year>=2000 && year<=2099) {
			a=6;
			year=year%100;
			b=year/4;
			
		}
		else {
			System.err.println("Sorry");
		}
		
		d=year+b+a+output;
//		System.out.println(d);
			
	}
	
	
	
	public void personInfo(String month) {
		switch(month) {
		case "January":
			jan=0;
			f=d+jan+day;
			week=f%7;
			break;
		case "February":
			feb=3;
			f=d+feb;
			week=f%7;
			break;
		case "March":
			mar=3;
			f=d+mar;
			week=f%7;
			break;
		case "April":
			apr=6;
			f=d+apr;
			week=f%7;
			break;
		case "May":
			may=1;
			f=d+may;
			week=f%7;
			break;
		case "June":
			jun=4;
			f=d+jun;
			week=f%7;
			break;
		case "July":
			jul=6;
			f=d+jul;
			week=f%7;
			break;
		case "August":
			aug=2;
			f=d+aug;
			week=f%7;
			break;
		case "September":
			sep=5;
			f=d+sep;
			week=f%7;
			break;
		case "October":
			oct=0;
			f=d+oct;
			week=f%7;
			break;
		case "November":
			nov=3;
			f=d+nov;
			week=f%7;
			break;
		case "December":
			dec=5;
			f=d+dec;
			week=f%7;
			break;
		default:
			System.err.println("Sorry");
		}

		System.out.println("");
		
		System.out.println("The Day of the Week which you are born is - ");
		
		if(week==0) {
			System.out.println("Sunday");
		}
		else if(week==1) {
			System.out.println("Monday");
		}
		else if(week==2) {
			System.out.println("Tuesday");
		}
		else if(week==3) {
			System.out.println("Wednesday");
		}
		else if(week==4) {
			System.out.println("Thursday");
		}
		else if(week==5) {
			System.out.println("Friday");
		}
		else if(week==6) {
			System.out.println("Saturday");
		}
		else {
			System.err.println("Sorry");
		}
	}
	

}





public class human {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner sc = new Scanner(System.in);

		
		
		System.out.print("Month - ");
		String month=sc.nextLine();

		
		System.out.print("Day - ");
		byte day=sc.nextByte();
	
		System.out.print("Year - ");
		int year=sc.nextInt();
		
		
		
		
		System.out.println();

		person p1=new person();
		calculation c1=new calculation();
		
		p1.personInfo(day);
		p1.personInfo(month);
		p1.personInfo(year);
		
		c1.personInfo(day);
		c1.personInfo(year);
		c1.personInfo(month);

	}

}

