import java.util.Scanner;

import java.util.Scanner;

public class Application {
	public static void main(String[] args) {
	Scanner input = new Scanner(System.in);
	String strAge = null;
	String strMonth = null;
	String strSibling = null;
	
	System.out.println("Please enter your first name");
	if (input.nextLine().equalsIgnoreCase("quit")) {
		System.out.println("Nobody likes a quitter...");
		System.exit(0);
	}
	String firstName = input.nextLine();
	
	System.out.println("Please enter your last name");
	if (input.nextLine().equalsIgnoreCase("quit")) {
		System.out.println("Nobody likes a quitter...");
		System.exit(0);
	}
	String lastName = input.nextLine();
	
	System.out.println("Please enter your age");
	String tmpAge = input.nextLine();
	//if (input.nextLine().equalsIgnoreCase("quit")) {
	if (tmpAge.equalsIgnoreCase("quit")) {
		System.out.println("Nobody likes a quitter...");
		System.exit(0);
	}
	int age = Integer.parseInt(tmpAge);
	//input.nextLine();
	//in age = input.nextInt();
	
	
	System.out.println("Please enter your birth month 1-12");
	String tmpMonth = input.nextLine();
	if (tmpMonth.equalsIgnoreCase("quit")) {
		System.out.println("Nobody likes a quitter...");
		System.exit(0);
	}
	int month = Integer.parseInt(tmpMonth);
	input.nextLine();
	
	System.out.println("What is your favorite ROYGBIV Color? or \"help\" if unsure");
	String color = input.nextLine();
	if (color.equalsIgnoreCase("quit")) {
		System.out.println("Nobody likes a quitter...");
		System.exit(0);
	}
	
	//input.nextLine();
	while (color.equalsIgnoreCase("help")) {
	//if (color.equalsIgnoreCase("help")) {
		System.out.println("The ROYGBIV colors are red, orange, yellow, green, blue, indigo, violet."
				+ "please enter your favorite color");
		color = input.nextLine();
	}

	System.out.println("Please enter how many siblings you have");
	String tmpSib = input.nextLine();
	if (tmpSib.equalsIgnoreCase("quit")) {
		System.out.println("Nobody likes a quitter...");
		System.exit(0);
	}
	int siblings = Integer.parseInt(tmpSib);


	//ageFortune(age);

	//monthFortune(month);

	//colorFortune(color);

	//siblingFortune(siblings);
	
	System.out.println("*" + firstName + "* *" + lastName + "* *" + colorFortune(color) + "* *" + monthFortune(month) + "* *" + siblingFortune(siblings) + "* *" + ageFortune(age) + "*");
	
	}

	private static String siblingFortune(int siblings) {
		String sibStr = null;
		if (siblings == 0) {
			sibStr = "You will have 1 child";
		} else if (siblings == 1) {
			sibStr = "You will have 3 children";

		} else if (siblings == 2) {
			sibStr = "You will have 2 children";
		} else {
			sibStr = "You will have 0 children";
		}
		return sibStr;
	}

	private static String colorFortune(String color) {
		switch (color.toLowerCase()) {
		case "red":
		    color = "You will be a firefighter";
		    break;
		case "orange":
		    color = "You will be a professional athlete";
		    break;
		case "yellow":
		    color = "You will be a doctor";
		    break;
		case "green":
		    color = "You will be an astronaut";
		    break;
		case "blue":
		    color = "You will be a programmer";
		    break;
		case "indigo":
		    color = "You will be an artist";
		    break;
		case "violet":
		    color = "You will be a chef";
		    break;
		default:
		    color = "You will be a teacher";
		}
		return color;
	}

	private static String monthFortune(int month) {
		String monthStr = null;
		if (month <= 0 || month >12) {
			monthStr = "Your income will make $50,000 per year ";
		} else if (month <4 ) {
			monthStr = "Your income will be $150,000 per year";
		} else if (month < 8) {
			monthStr = "Your income will be 250,000 per year";
		} else {
			monthStr = "Your income will be $100,000 per year";
		}
		return monthStr;
	}

	private static String ageFortune(int age) {
		String ageStr = null;
		if (age % 2 == 0) { // even will have remainder (%) of zero if divided by 2
			ageStr = "You will have dogs as pets";
		} else {
			ageStr = "You will have cats as pets";
		}
		return ageStr;
	}
	
	

}
