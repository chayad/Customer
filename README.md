# Customer

package in.ac.kletech;

public class Customer {
	private int icustomerID;
	private String sCustomername;
	
	public int getIcustomerID() {
		return icustomerID;
	}
	public void setIcustomerID(int icustomerID) {
		this.icustomerID = icustomerID;
	}
	public String getsCustomername() {
		return sCustomername;
	}
	public void setsCustomername(String sCustomername) {
		this.sCustomername = sCustomername;
	}
    
}

public class PrivillegedCustomer extends Customer {
private String sMemCardType;

public String getsMemCardType() {
	return sMemCardType;
}

public void setsMemCardType(String sMemCardType) {
	this.sMemCardType = sMemCardType;
}
static int counter;
static
{
counter=3000;
}
PrivillegedCustomer()
{
	setIcustomerID(++counter);
}
PrivillegedCustomer(String sName,String sCard)
{
	setIcustomerID(++counter);
	setsCustomername(sName);
	setsMemCardType(sCard);
	
}
}

public class RegularCustomer extends Customer {
private float fDiscount;

public float getfDiscount() {
	return fDiscount;
}

public void setfDiscount(float fDiscount) {
	this.fDiscount = fDiscount;
}
static int counter;
static
{
counter=1000;
}
RegularCustomer()
{
	setIcustomerID(++counter);
}
RegularCustomer(String name,float dis)
{
	setIcustomerID(++counter);
	setsCustomername(name);
	setfDiscount(dis);
}

public class Demo {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
       RegularCustomer r1=new RegularCustomer("p",20);
       RegularCustomer r2=new RegularCustomer("n",30);
       PrivillegedCustomer p1= new PrivillegedCustomer("s","Gold");
       PrivillegedCustomer p2= new PrivillegedCustomer("q","Silver");
      
       System.out.println("Regular customer details");
       System.out.println("ID1 " +r1.getIcustomerID());
       System.out.println("name1 " +r1.getsCustomername());
       System.out.println("discount1 " +r1.getfDiscount());
       System.out.println("ID2 " +r2.getIcustomerID());
       System.out.println("name2 " +r2.getsCustomername());
       System.out.println("discount2 " +r2.getfDiscount());
       System.out.println("Privilage customer details");
       System.out.println("ID1 " +p1.getIcustomerID());
       System.out.println("name1 " +p1.getsCustomername());
       System.out.println("cardtype1 " +p1.getsMemCardType());
       System.out.println("ID2 " +p2.getIcustomerID());
       System.out.println("name2 " +p2.getsCustomername());
       System.out.println("cardtype2 " +p2.getsMemCardType());
       
	} 
