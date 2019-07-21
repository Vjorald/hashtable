# hashtable

import java.util.Enumeration;
import java.util.Hashtable;

public class HashtableTest {

	public static void main(String[] args) {
		Hashtable h = new Hashtable();
		
		h.put("Willi Frankien", "willi.franken@fh-xxx.de");
		h.put("Hugo Meier", "hugo.meier@abc.de");
		h.put("Sabine Moll", "sabine.moll@fh-xxx.de");
		
		System.out.println("NAME -> ADRESSE");
		
		Enumeration keys = h.keys();
		
		while (keys.hasMoreElements()){
			String key = (String) keys.nextElement();
			String value = (String) h.get(key);
			System.out.println(key + " -> " + value);
		}

		System.out.println();
		
		System.out.println("Email- Adressen: ");
		Enumeration elements = h.elements();
		
		while (elements.hasMoreElements()){
			String value = (String) elements.nextElement();
			System.out.println(value);
		}
	}

}
