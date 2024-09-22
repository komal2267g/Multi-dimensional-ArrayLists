# Multi-dimensional-ArrayLists

import java.util.*;
public class Main {
    public static void swap(ArrayList<Integer> list, int idx1, int idx2) {
        int temp = list.get(idx1);
        list.set(idx1, list.get(idx2));
        list.set(idx2, temp);
    }

    public static void main(String args[]) {
        ArrayList<ArrayList<Integer>> mainlist = new ArrayList<>();

        ArrayList<Integer> list = new ArrayList<>();
        list.add(1); list.add(2); list.add(3);

        ArrayList<Integer> list2 = new ArrayList<>();
        list2.add(4); list2.add(5); list2.add(6);

        // Adding both lists to the main list
        mainlist.add(list);
        mainlist.add(list2);

        for (int i = 0; i < mainlist.size(); i++) {
            ArrayList<Integer> currList = mainlist.get(i);
            for (int j = 0; j < currList.size(); j++) {
                System.out.print(currList.get(j) + " ");
            }
            System.out.println();
        }
    }
}
