# helloworld
/* Save this in a file called Main.java to compile and test it */

/* Do not add a package declaration */
import java.util.*;
import java.io.*;

/* You may add any imports here, if you wish, but only from the 
   standard library */

public class Main {
    
public static int processData(ArrayList<String> array)
 {

Collections.sort(array);
String str=(String)array.get((array.size())-1);
int length=str.length();
char ch;
int count=0,p,i;

for( i=0;i<length;i++)
{
        ch=str.charAt(i);
            if(ch[i]==' ')
          count++;

if(count==4)
break;
}
}
p=i;
p++;

String sub=str.substring(p);

int res=Integer.parseInt(sub);

  
 return res;

}

    public static void main (String[] args) {
        ArrayList<String> inputData = new ArrayList<String>();
        try {
            Scanner in = new Scanner(new BufferedReader(new FileReader("input.txt")));
            while(in.hasNextLine()) {
                String line = in.nextLine().trim();
                if (!line.isEmpty()) // Ignore blank lines
                    inputData.add(line);
            }
            int retVal = processData(inputData);
            PrintWriter output = new PrintWriter(new BufferedWriter(new FileWriter("output.txt")));
            output.println("" + retVal);
            output.close();
        } catch (IOException e) {
            System.out.println("IO error in input.txt or output.txt");
        }
    }
}

