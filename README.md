public class MyClass {
    public static void main(String args[]) {
     
        int[][] mas = new int[5][8];
        int[][] mas2;
        
        zapolnenie(mas);
        printMasiv(mas);
        
        for (int[] arr : mas){
            sort(arr);
        }
        System.out.println();
         printMasiv(mas);
         System.out.println();
         mas2 = ext(mas);
         printMasiv(mas2);
         
        
 
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
    public static int[][] ext(int arr[][]) {
        int [][] minMax = new int[5][2];
        int min = 0, max = 0;
        
        for (int i = 0; i < 5; i++) {
            min = arr[i][0];
            max = arr[i][0];
            
            for (int j = 1; j <8; j++) {
                if (arr[i][j] < min) {
                    min = arr[i][j];
                }
                if (arr[i][j] > max) {
                    max = arr[i][j];
                }
            }
            minMax[i][0] = min;
            minMax[i][1] = max;
        }
        return minMax;
    }
    
}
