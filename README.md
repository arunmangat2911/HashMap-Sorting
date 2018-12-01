# HashMap-Sorting

import java.util.HashMap;
import java.util.Iterator;
import java.util.Map;
import java.util.Set;
import java.util.TreeMap;

public class HashMapSorting {
    public static void main(String[] args) {
        HashMap<Integer, String> hmap = new HashMap<Integer, String>();
        hmap.put(12, "XX");
        hmap.put(17, "YY");
        hmap.put(2, "AB");
        hmap.put(20, "XXZY");
        Set set = hmap.entrySet();
        Iterator iter = set.iterator();
        while(iter.hasNext()) {
            Map.Entry mentry = (Map.Entry)iter.next();
            System.out.println("Key is : " +mentry.getKey() + ", Value :" + mentry.getValue());
            System.out.println(hmap);
            
            Map<Integer, String> map = new TreeMap<Integer, String>(hmap);
            System.out.println("After sorting:");
            Set set2 = map.entrySet();
            Iterator iter1 = set2.iterator();
            while(iter1.hasNext()) {
                Map.Entry mentry2 = (Map.Entry)iter1.next();
                System.out.println("Key " + mentry2.getKey()+ "Value" + mentry2.getValue());
                //System.out.println(mentry2.getValue());
            }
        }
        
    }
}
