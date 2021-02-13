public class Test 

{
 
 public static void main(String[] args) 
	
  {
	
    Account account = new Account(1122, 20000);
		account.withdraw(2500);
		account.deposit(3000);
		System.out.println("Balance is " + account.getBalance());
		System.out.println("This account was created at " +
		account.getDateCreated());
  }

}

class Account 

{
  private int id;
	private double balance;
	private Date dateCreated;
	
	public Account() 
	{
	id = 0;
	balance = 0;
	}
	
	public Account(int newId , double newBalance ) 
	{
		id = newId;
		balance = newBalance;
		dateCreated = new Date();
	}
	
	public double getBalance() 
	{
		return balance;
	}
	
	public int getId() 
	{
		return id;
	}
	
	public String getDateCreated() 
	{
		return dateCreated.toString();
	}
	
	public void withdraw(double money)
	{
		if (money < balance)
		{
		balance = balance - money;
		}
		else 
		{
			System.out.println("your balance is lower than withdraw!!");
		}
	}
	
	public double deposit(double money)
	{
		return balance = balance + money;
	}
}
