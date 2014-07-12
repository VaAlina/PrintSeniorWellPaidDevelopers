PrintSeniorWellPaidDevelopers 1.0
=============================


public class MainS {
    DeveloperS[] list = {
			new JuniorDeveloperS("Petr", 2300),
			new SeniorDeveloperS("Dima", 1600),
			new JuniorDeveloperS("Vova", 1050),
			new SeniorDeveloperS("Jan", 1780),
			new TeamLeadDeveloperS("Roman", 8900),
			new SeniorDeveloperS("Mishka", 1000),
			new SeniorDeveloperS("Kostia", 3400),
			new JuniorDeveloperS("Oleg", 2590),
			new SeniorDeveloperS("Oksana", 1600),
			new SeniorDeveloperS("Jacov", 1400),
			new TeamLeadDeveloperS("Rita", 6000),
			new SeniorDeveloperS("Masha", 1200)
    		
    };
    
    StringBuilder sb;
    {
	for (DeveloperS d : list) {
		sb = new StringBuilder() 
			.append(d.printDeveloper());

		
		System.out.println(sb.toString());
	}
}
}





public abstract class DeveloperS {
	protected String name;
	protected int salary;
	
	public DeveloperS(String name, int salary){
		this.name = name;
		this.salary = salary;
			}
	public String getName(){
		return name;
	}
    
	public int getSalary(){
		return salary;
	}
	
	public abstract String printDeveloper();
}






public class SeniorDeveloperS extends DeveloperS {
	public SeniorDeveloperS (String name, int salary){
		super(name, salary);
	}
	
	@Override
	public String printDeveloper() {
			if (salary > 1500)
			return (name + " : " + salary);
			else
			return "";
	}
}






public class JuniorDeveloperS extends DeveloperS {
	public JuniorDeveloperS(String name, int salary) {
		super(name, salary);
	}
	
	@Override
	public String printDeveloper() {
			return "";
}
}





public class TeamLeadDeveloperS extends DeveloperS {
	public TeamLeadDeveloperS(String name, int salary) {
		super(name, salary);
	}
	
	@Override
	public String printDeveloper() {
			return "";
	}
}

