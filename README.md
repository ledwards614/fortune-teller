import java.util.Scanner;

public class Application {
	public static void main(String[] args) {
	Scanner input = new Scanner(System.in);
	
	System.out.println("Please enter your first name");
	String firstName = input.nextLine();
	
	System.out.println("Please enter your last name");
	String lastName = input.nextLine();
	
	System.out.println("Please enter your age");
	int age = input.nextInt();
	
	System.out.println("Please enter your birth month 1-12");
	int month = input.nextInt();
	input.nextLine();
	
	System.out.println("What is your favorite ROYGBIV Color? or \"help\" if unsure");
	String color = input.nextLine();
	//input.nextLine();
	if (color.equalsIgnoreCase("help")) {
		System.out.println("Red, Orange, yellow, green, blue, indigo, or violet, "
				+ "please enter your favorite color");
		color = input.nextLine();	
	}

	System.out.println("Please enter how many siblings you have");
	int siblings = input.nextInt();


	ageFortune(age);

	monthFortune(month);

	colorFortune(color);

	siblingFortune(siblings);
	}

	private static void siblingFortune(int siblings) {
		if (siblings == 0) {
			System.out.println("You will have 1 child");
		} else if (siblings == 1) {
			System.out.println("You will have 3 children");

		} else if (siblings == 2) {
			System.out.println("You will have 2 children");
		} else {
			System.out.println("You will have 0 children");
		}
	}

	private static void colorFortune(String color) {
		switch (color.toLowerCase()) {
		case "red":
		    System.out.println("You will be a firefighter");
		    break;
		case "orange":
		    System.out.println("You will be a professional athlete");
		    break;
		case "yellow":
		    System.out.println("You will be a doctor");
		    break;
		case "green":
		    System.out.println("You will be a surfer");
		    break;
		case "blue":
		    System.out.println("You will be a programmer");
		    break;
		case "indigo":
		    System.out.println("You will be an artist.");
		    break;
		default:
		    System.out.println("You will be a teacher");
		}
	}

	private static void monthFortune(int month) {
		if (month <= 0 || month >12) {
			System.out.println("Your income will make $50,000 per year ");
		} else if (month <4 ) {
			System.out.println("Your income will be $150,000 per year");
		} else if (month < 8) {
			System.out.println("Your income will be 250,000 per year");
		} else {
			System.out.println("Your income will be $100,000 per year");
		}
	}

	private static void ageFortune(int age) {
		if (age % 2 == 0) { // even will have remainder (%) of zero if divided by 2
			System.out.println("You have dogs as pets");
		} else {
			System.out.println("You will have cats as pets");
		}
	}
	
	

}
