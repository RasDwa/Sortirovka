public class MyClass {
    public static void main(String args[]) {
     
        int[][] mas = new int[5][8];
        
        zapolnenie(mas);
        printMasiv(mas);
        
        for (int[] arr : mas){
            sort(arr);
        }
        System.out.println();
         printMasiv(mas);
        
 
    }
    
    //заполнение масива
    public static void zapolnenie(int[][] mas) {
        for(int i = 0; i<mas.length; i++){
            for(int j = 0; j<mas[i].length; j++){
                mas[i][j] =(int) (Math.random()*10);
            }
        }
    }
    // вывод масива
    public static void printMasiv(int[][] mas) {
        for(int i = 0; i<mas.length; i++){
            for(int j = 0; j<mas[i].length; j++){
               System.out.print(mas[i][j]+ " ");
            }
            System.out.println();
        }
    }
    //сортировка масива
    public static void sort(int[] a){
        for(int i=0; i<a.length; i++){
            for(int j = a.length-1; j > i; j--) {
                if(a[j-1] > a[j]) {
                    int tmp = a[j-1];
                    a[j-1] = a[j];
                    a[j] = tmp;
                }
            }
        }
    }
    
}
