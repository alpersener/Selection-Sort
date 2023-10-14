Selection Sort
==============
Selection Sort,listenin sıralanmamış kısmından en küçük veya en büyük öğeyi tekrar tekrar seçerek listenin sıralanmış kısmına taşıyan sorting algoritmasıdır.

![photo1](https://github.com/alpersener/Selection-Sort/blob/master/photo1.png)

Bir elementi seçip maximum ya da minimum durumuna göre sıralama yaparız

**Time Complexity**
-------------------

![photo2](https://github.com/alpersener/Selection-Sort/blob/master/photo2.png)

**Selection Sort,küçük listelerde iyi performans verir**

    package SelectionSort;
    
    import java.util.Arrays;
    
    public class Main {
        public static void main(String[] args) {
            int[] arr={2,1,-32,-88,5};
            selection(arr);
            System.out.println(Arrays.toString(arr));
    
        }
    
    
    
        public static void selection(int[] arr){
            for (int i = 0; i < arr.length; i++) {
                //find the max item in the remaining array and swap with correct index
                int last=arr.length-i-1; //en sondaki indexe yerleşmesi için.
                int maxIndex=getMaxIndex(arr,0,last);
                swapArray(arr,maxIndex,last);
    
                
            }
    
        }
    
        private static int getMaxIndex(int[] arr, int start, int end) {
            int max=start;
            for (int i= start; i <=end; i++) {
                if(arr[max]<arr[i]){
                    max=i;
                }
    
            }
            return max;
       }
    
    
       private static void swapArray(int[] arr,int first,int second){
            int temp=arr[first];
            arr[first]=arr[second];
            arr[second]=temp;
       }
    
    }

i=0’dayken en sondaki eleman 5-0-1=4.index yani 3 bu şekilde ilerliyor.
