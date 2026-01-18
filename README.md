# CONTACT-LIST
CREATING A CONTACT LIST ON JAVA
import java.util.ArrayList;
import java.util.Scanner;
class Contacts{
    static String names;
   static int num;
   static ArrayList<String> name = new ArrayList<>();
    static ArrayList<Integer> numbers = new ArrayList<>();
    static void contact(){
        //names
        name.add("ron");
        name.add("ronan");
        name.add("louis");
        //numbers
        numbers.add(6767);
        numbers.add(6161);
        numbers.add(123);
    }
    static void enter_names(){
        Scanner sc = new Scanner(System.in);
        System.out.print("enter name: ");
        names = sc.nextLine();
        System.out.print("enter contact number: ");
        num = sc.nextInt();
        name.add(names);
        numbers.add(num);
    }
    static void search(){
        boolean found = false;
        Scanner find = new Scanner(System.in);
        System.out.print("search name: ");
        String sname;
        sname = find.nextLine();
        for(int i = 0; i < name.size(); i++){
            if(name.get(i).equalsIgnoreCase(sname)) {
                System.out.println("name found: " + name.get(i) + "contact numbers: " + numbers.get(i));
                found = true;
                break;
            }
        }
        if(!found){
            System.out.println("contatc not found");
        }
    }
}
public class aminah {
    public static void main(String[] args) {
        Contacts Contact = new Contacts();
        Contact.contact();
        Contact.enter_names();
        Contact.search();
    }
}
