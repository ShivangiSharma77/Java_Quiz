import java.util.*;
abstract class basic1{
	
	abstract void choose();
	abstract void test_math();
	abstract void test_phy();
	abstract void test_hist();
	abstract void test_bio();
	abstract void test_eng();
	abstract void result();
	
}
class student1 extends course1{
	  //ENCAPSULATION
	private String name;
	private String roll;
	private int sapid;
	
	void set(String name,String roll,int sapid)    //Setter 
	{
		this.name=name;
		this.roll=roll;
		this.sapid=sapid;
	}
	String get_name()                                //Getter 
	{
		return name;
	}
	String get_roll()                                //Getter 
	{
		return roll;
	}
	int get_id()                                 //Getter 
	{
		return sapid;
	}
	
	
}
class course1 extends basic1{
	//ABSTRACTION
	Scanner cs=new Scanner(System.in);
	public int ch1;
	public String ch2;
	String ans1[]=new String[5];
	String ans2[]=new String[5];
	String ans3[]=new String[5];
	String ans4[]=new String[5];
	String ans5[]=new String[5];
	int res[]=new int[5];
	int total1=0;
	int total2=0;
	int total3=0;
	int total4=0;
	int total5=0;
	int a=0;
	int b=0;
	String choice="";
	String ch3="";
	
	void choose()                                               //implementation of abstract class
	{  
		res[0]=0;
		res[1]=0;
		res[2]=0;
		res[3]=0;
		res[4]=0;
		do {
		System.out.println("BROCHURE:");
		System.out.println("------------------------------");
		System.out.println("Choose the appropriate option:");
		System.out.println("FINAL_RESULT");
		System.out.println("COURSES");
		ch3=cs.next();
		if(ch3.equalsIgnoreCase("courses")) {
		System.out.println("	1.MATHS");
		System.out.println("	2.PHYSICS");
		System.out.println("	3.HISTORY");
		System.out.println("	4.BIOLOGY");
		System.out.println("	5.ENGLISH");
		ch1=cs.nextInt();
		System.out.println("Select your choice : ");
		System.out.println("QUIZ");
		System.out.println("GRADES");		
		ch2=cs.next();

		if(ch2.equalsIgnoreCase("quiz"))
		{
			switch(ch1) {
		case 1:
			test_math();
			break;
		case 2:
			test_phy();
			break;
		case 3:
			test_hist();
			break;
		case 4:
			test_bio();
			break;
		case 5:
			test_eng();
			break;	
		}}
		else if(ch2.equalsIgnoreCase("grades")) {                                        //displaying grades
            	System.out.println("--------------RESULT---------------");
            	switch(ch1) {
        		case 1:
        			for(int i=0;i<ans1.length;i++)
  					System.out.println(i+1+"."+ans1[i]);
  					System.out.println("You scored "+total1*2+" out of 10");
        			break;
        		case 2:
        			for(int i=0;i<ans2.length;i++)
      					System.out.println(i+1+"."+ans2[i]);
      					System.out.println("You scored "+total2*2+" out of 10");
        			break;
        		case 3:
        			for(int i=0;i<ans3.length;i++)
      					System.out.println(i+1+"."+ans3[i]);
      					System.out.println("You scored "+total3*2+" out of 10");
        			break;
        		case 4:
        			for(int i=0;i<ans4.length;i++)
      					System.out.println(i+1+"."+ans4[i]);
      					System.out.println("You scored "+total4*2+" out of 10");     					
        			break;
        		case 5:
        			for(int i=0;i<ans5.length;i++)
      					System.out.println(i+1+"."+ans5[i]);
      					System.out.println("You scored "+total5*2+" out of 10");
        			break;
//            	}
//			System.out.println("Your final Score is:");
			
		}
            	System.out.println("");
            	}
		}
		else if(ch3.equalsIgnoreCase("final_result"))
	    result();
		else
			System.out.println("INVALID INPUT");
		    System.out.println("");
			System.out.println("Do you wish to return to brochure ?");
			choice=cs.next();}
		while(choice.equalsIgnoreCase("yes"));
	       
		}
	void test_math()                                         //Math Test
	{   
		System.out.println("-------------MATHS QUIZ-----------");
		System.out.println("The quiz contains 5 questions of 2 marks each (total-10 marks");
		System.out.println("");
		System.out.println("Q1. 2*2 is ?");
		ans1[0]=cs.next();
		if(ans1[0].equalsIgnoreCase("4"))
			{ans1[0]="Correct Answer";
			total1=total1+1;
			}
		else {
			ans1[0]="Wrong answer";}
		
		System.out.println("Q2. 6+4 is ?");
		ans1[1]=cs.next();
		if(ans1[1].equalsIgnoreCase("10"))
		{ans1[1]="Correct Answer";
		total1=total1+1;
		}
	    else {
		ans1[1]="Wrong answer";}
		
		System.out.println("Q3. 9-5 is ?");
		ans1[2]=cs.next();
		if(ans1[2].equalsIgnoreCase("4"))
		{ans1[2]="Correct Answer";
		total1=total1+1;
		}
	    else {
		ans1[2]="Wrong answer";}
		
		System.out.println("Q4. 25/5 is ?");
		ans1[3]=cs.next();
		if(ans1[3].equalsIgnoreCase("5"))
		{ans1[3]="Correct Answer";
		total1=total1+1;
		}
	    else {
		ans1[3]="Wrong answer";}
		
		System.out.println("Q5. 4^2 is ?");
		ans1[4]=cs.next();
		if(ans1[4].equalsIgnoreCase("16"))
		{ans1[4]="Correct Answer";
		total1=total1+1;
		}
	    else {
		ans1[4]="Wrong answer";}
		res[0]=total1*2;
		System.out.println(res[0]);
	}
	void test_phy()                                             //Physics test
	{  
		System.out.println("-------------PHYSICS QUIZ-----------");
		System.out.println("The quiz contains 5 questions of 2 marks each (total-10 marks");
		System.out.println("");
		System.out.println("Q1. Which instrument is used to measure altitudes in aircraft's ?");
		ans2[0]=cs.next();
		if(ans2[0].equalsIgnoreCase("Altimete"))
		{ans2[0]="Correct Answer";
		total2=total2+1;
		}
	else {
		ans2[0]="Wrong answer";}
		
		System.out.println("Q2. Which instrument is used to measure depth of ocean ?");
		ans2[1]=cs.next();
		if(ans2[1].equalsIgnoreCase("Fathometer"))
		{ans2[1]="Correct Answer";
		total2=total2+1;
		}
	else {
		ans2[1]="Wrong answer";}
		
		System.out.println("Q3. Name of the instrument to measure atomspheric pressure ?");
		ans2[2]=cs.next();
		if(ans2[2].equalsIgnoreCase("Barometer"))
		{ans2[2]="Correct Answer";
		total2=total2+1;
		}
	else {
		ans2[2]="Wrong answer";}
		
		System.out.println("Q4. Which instrument is used to measure the power of electric circuit ?");
		ans2[3]=cs.next();
		if(ans2[3].equalsIgnoreCase("Wattmeter"))
		{ans2[3]="Correct Answer";
		total2=total2+1;
		}
	else {
		ans2[3]="Wrong answer";}
		
		System.out.println("Q5. Which instrument is used in submarine to see the objects above sea level ?");
		ans2[4]=cs.next();
		if(ans2[4].equalsIgnoreCase("Periscope"))
		{ans2[4]="Correct Answer";
		total2=total2+1;
		}
	else {
		ans2[4]="Wrong answer";}
		res[1]=total2*2;
	}
	void test_hist()                                     //history test
	{   b=3;
		System.out.println("-------------HISTORY QUIZ-----------");
		System.out.println("The quiz contains 5 questions of 2 marks each (total-10 marks");
		System.out.println("");
		System.out.println("Q1. Where did the miniature Bani Thani paintings of Indian heritage develop?");
		ans3[0]=cs.next();
		if(ans3[0].equalsIgnoreCase("Kishengarh"))
		{ans3[0]="Correct Answer";
		total3=total3+1;
		}
	else {
		ans3[0]="Wrong answer";}
		
		System.out.println("Q2. At which place did Buddha die?");
		ans3[1]=cs.next();
		if(ans3[1].equalsIgnoreCase("Kusinagara"))
		{ans3[1]="Correct Answer";
		total3=total3+1;
		}
	else {
		ans3[1]="Wrong answer";}
		
		System.out.println("Q3. Who wrote the Indian National Anthem 'Jana Gana Mana'?");
		ans3[2]=cs.next();
		if(ans3[2].equalsIgnoreCase("RabindranathTagore"))
		{ans3[2]="Correct Answer";
		total3=total3+1;
		}
	else {
		ans3[2]="Wrong answer";}
		
		System.out.println("Q4. Who was the grandson of Ashoka?");
		ans3[3]=cs.next();
		if(ans3[3].equalsIgnoreCase("Dashkumar"))
		{ans3[3]="Correct Answer";
		total3=total3+1;
		}
	else {
		ans3[3]="Wrong answer";}
		
		System.out.println("Q5. The All India Muslim League was founded in December 1906 at ?");
		ans3[4]=cs.next();
		if(ans3[4].equalsIgnoreCase("Dacca"))
		{ans3[4]="Correct Answer";
		total3=total3+1;
		}
	else {
		ans3[4]="Wrong answer";}
		res[2]=total3*2;
	}
	
	void test_bio()                                                   //biology test
	{   
		System.out.println("-------------BIOLOGY QUIZ-----------");
		System.out.println("The quiz contains 5 questions of 2 marks each (total-10 marks");
		System.out.println("");
        System.out.println("Q1. Which is a large blood vessel that carries blood away from the heart?");
		ans4[0]=cs.next();
		if(ans4[0].equalsIgnoreCase("Artery"))
		{ans4[0]="Correct Answer";
		total4=total4+1;
		}
	else {
		ans4[0]="Wrong answer";}
		
		System.out.println("Q2. Which is not a member of the vitamin B complex?");
		ans4[1]=cs.next();
		if(ans4[1].equalsIgnoreCase("Ascorbic"))
		{ans4[1]="Correct Answer";
		total4=total4+1;
		}
	else {
		ans4[1]="Wrong answer";}
		
		System.out.println("Q3. Fungi are plants that lack ?");
		ans4[2]=cs.next();
		if(ans4[2].equalsIgnoreCase("Chlorophyll"))
		{ans4[2]="Correct Answer";
		total4=total4+1;
		}
	else {
		ans4[2]="Wrong answer";}
		
		System.out.println("Q4. What makes a reptile a reptile ?");
		ans4[3]=cs.next();
		if(ans4[3].equalsIgnoreCase("Egglaying"))
		{ans4[3]="Correct Answer";
		total4=total4+1;
		}
	else {
		ans4[3]="Wrong answer";}
		
		System.out.println("Q5. Which blood vessels have the smallest diameter?");
		ans4[4]=cs.next();
		if(ans4[4].equalsIgnoreCase("Capillaries"))
		{ans4[4]="Correct Answer";
		total4=total4+1;
		}
	else {
		ans4[4]="Wrong answer";}
		res[3]=total4*2;
	}
	
	void test_eng()                                              //English test
	{   
	cs.nextLine();
		System.out.println("-------------ENGLISH QUIZ-----------");
		System.out.println("The quiz contains 5 questions of 2 marks each (total-10 marks");
		System.out.println("");
		System.out.println("Q1. Who wrote Fahrenheit 451?");
		ans5[0]=cs.nextLine();
		if(ans5[0].equalsIgnoreCase("Ray Ban"))
		{ans5[0]="Correct Answer";
		total5=total5+1;
		}
	else {
		ans5[0]="Wrong answer";}
		System.out.println("Q2. Who wrote Cat’s Cradle?");
		ans5[1]=cs.nextLine();
		if(ans5[1].equalsIgnoreCase("Kurt"))
		{ans5[1]="Correct Answer";
		total5=total5+1;
		}
	else {
		ans5[1]="Wrong answer";}
		System.out.println("Q3. Who wrote The Shining?");
		ans5[2]=cs.nextLine();
		if(ans5[2].equalsIgnoreCase("Stephen"))
		{ans5[2]="Correct Answer";
		total5=total5+1;
		}
	else {
		ans5[2]="Wrong answer";}
		System.out.println("Q4. Who wrote Walden?");
		ans5[3]=cs.nextLine();
		if(ans5[3].equalsIgnoreCase("Henry"))
		{ans5[3]="Correct Answer";
		total5=total5+1;
		}
	else {
		ans5[3]="Wrong answer";}
		System.out.println("Q5. Who wrote Life on the Mississippi?");
		ans5[4]=cs.nextLine();
		if(ans5[4].equalsIgnoreCase("Mark Twain"))
		{ans5[4]="Correct Answer";
		total5=total5+1;
		}
	else {
		ans5[4]="Wrong answer";}
		res[4]=total5*2;
	}
	void result()                                                         // final result of all subjects
	{ float sum=0;
	System.out.println(res[0]);
	   System.out.println("The final result is: ");
	   System.out.println("SUBJECT    "+"SCORE"+"     TOTAL");
	   System.out.println("----------------------------------");
	   System.out.println("1.MATHS    "+res[0]+"       10");
	   System.out.println("2.PHYSICS  "+res[1]+"       10");
	   System.out.println("3.HISTORY  "+res[2]+"       10");
	   System.out.println("4.BIOLOGY  "+res[3]+"       10");
	   System.out.println("5.ENGILSH  "+res[4]+"       10");
	   System.out.println("");
	   for(int i=0;i<5;i++)
		   sum=sum+res[i];
	   System.out.println("Your final result is : "+sum/50*100+"%");
	   System.out.println("------------------------------------------------------");
	}
	
}
class teacher1 extends course1{
	private String name;
	private String dept;
	private int ID;
	int num;
	String sel="";
	String choice2="";
   	List<String> l1 = new ArrayList<String>();                     //List interface implementation
	void set(String name,String dept,int ID)    //Setter 
	{
		this.name=name;
		this.dept=dept;
		this.ID=ID;
	}
	String get_name()                                //Getter 
	{
		return name;
	}
	String get_dept()                                //Getter 
	{
		return dept;
	}
	int get_ID()                                 //Getter 
	{
		return ID;
	}
	//Polymorphism (run-time)
	void choose() {                                                     //method overriding
		do {
		System.out.println("Choose the appropriate option ?");	
		System.out.println("ADD QUESTIONS");
		System.out.println("VIEW QUESTIONS");
		sel=cs.next();
		if(sel.equalsIgnoreCase("add"))
			add();
		else if(sel.equalsIgnoreCase("view"))
			view();
		else
			System.out.println("INVALID OPTION");
		System.out.println("");
	System.out.println("Do you wish to return to the menu again?");
	choice2=cs.next();
		}
	while(choice2.equalsIgnoreCase("yes"));		
}  
	void add() {                                                   //add desired amount of questions
		a=1;
	String q="";
	cs.nextLine();
	do {
	System.out.println("Enter the question");
	l1.add(cs.nextLine());
	System.out.println("");
	System.out.println("Do you want to add more ?");
	q=cs.nextLine();
	}while(q.equalsIgnoreCase("yes"));
	}
void view() {
	System.out.println("VIEW ALL ADDED QUESTIONS:");
	System.out.println("");
	if(a>0)
	for(int i=0;i<l1.size();i++) {
		System.out.println(l1.get(i));
		}
	else
		System.out.println("NO ADDED QUESTIONS");
}}
public class drive {                                                           //Driver class
	public static void main(String args[])
	{ 
		Scanner sc=new Scanner(System.in);
		String option="";
		String name="";
		String roll="";
		int sapid;
		int ID;
		String dept="";
		student1 obj1=new student1();
//		quiz obj2=new quiz();
		//course1 obj3=new course1();
		teacher1 obj2=new teacher1();
		do
		{
		System.out.println("ARE YOU A TEACHER OR STUDENT");
		String type=sc.nextLine();

		if(type.equalsIgnoreCase("teacher"))
		{   
			System.out.println("Enter your name:");
		    name=sc.nextLine();
			System.out.println("Enter your Department");
			dept=sc.nextLine();
			System.out.println("Enter your id");
			ID=sc.nextInt();
			sc.nextLine();
			obj2.set(name,dept,ID);
			System.out.println("name : "+obj2.get_name());
			System.out.println("Department : "+obj2.get_dept());
			System.out.println("ID : "+obj2.get_ID());
			System.out.println("");
			obj2.choose();
		}
		else if(type.equalsIgnoreCase("student"))
		{
			System.out.println("Enter your name:");
			name=sc.nextLine();
			System.out.println("Enter your roll number");
			roll=sc.nextLine();
			System.out.println("Enter your sapid");
			sapid=sc.nextInt();
			sc.nextLine();
			obj1.set(name, roll, sapid);
			System.out.println("name : "+obj1.get_name());
			System.out.println("rollnumber : "+obj1.get_roll());
			System.out.println("SAP ID : "+obj1.get_id());
			System.out.println("");
			obj1.choose();	
		}
		else
		{
			System.out.println("WRONG INPUT");
		}
		System.out.println("");
		System.out.println("-------------------------------------------------");
		System.out.println("Do you wish to start again :");
		option=sc.nextLine();
	}
		while(option.equalsIgnoreCase("yes")); 
	}
}


