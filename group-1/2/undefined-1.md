# 🐢 배열 : 구현

## <mark style="background-color:orange;">**🫧 벡터 구현하기**</mark>

*   size() - 항목의 개수

    ```java
    public static void main(String[] args){
        ArrayList<Object> sizeTest = new ArrayList<Object>();
        System.out.println( sizeTest.size() );  // 0
    }
    ```
*   capacity() - 들어갈 수 있는 항목의 최대 개수

    ```java
    public static void main(String[] args) {
        StringBuffer buff = new StringBuffer(20);
        buff.append("GwangJik");
        System.out.println("Capacity : " + buff.capacity());    // 20
    }
    ```
*   is\_empty()

    ```java
    String test = null;
    if(test != null && test.isEmpty()) {
        System.out.println(test);
    }
    ```
*   at(index) - 인덱스에 있는 항목을 돌려주고, 인덱스가 범위 밖이면 에러를 냄

    ```java
    int digitStr = "456";

    // 0번째에 있는 char 값을 리턴
    digitStr.charAt(0) // 4
    ```
*   push(item)

    ```java
    var fruit = ["사과", "배", "포도"];
    fruit.push("딸기");      // 배열 뒤쪽에 데이터 삽입 ["사과", "배", "포도", "딸기"]
    ```
*   insert(index, item) - index에 item을 삽입하고 기존 인덱스의 값부터 쭉 오른쪽으로 쉬프트

    ```java
    public class ArrayListDemo {
        public static void main(String[] args)
        {
            // create an empty list with an initial
            // capacity
            List<String> list = new ArrayList<String>(5);
     
            // use add() method to initially
            // add elements in the list
            list.add("Geeks");
            list.add("For");
            list.add("Geeks");
           
            // Add a new element at index 0
            list.add(0, "Hello");
           
            // prints all the elements available in list
            for (String str : list) {
                System.out.print(str + " ");
            }
        }
    }
    // Hello Geeks For Geeks
    ```
*   prepend(item) - 맨 앞에 원소를 삽입

    ```java
    int[] arr = { 10, 20, 30 };

    arr = ArrayUtils.add(arr, 40);
    ```
*   pop() - 마지막 원소를 삭제하고 값을 돌려준다

    ```java
    var fruit = ["사과", "배", "포도"];
    fruit.pop();             // 배열 뒤쪽의 데이터 제거 ["사과", "배"]
    ```
*   delete(index) - delete item at index, shifting all trailing elements left

    ```java
    import java.io.File;  // Import the File class

    public class DeleteFile {
      public static void main(String[] args) { 
        File myObj = new File("filename.txt"); 
        if (myObj.delete()) { 
          System.out.println("Deleted the file: " + myObj.getName());
        } else {
          System.out.println("Failed to delete the file.");
        } 
      } 
    }

    // Deleted the file: filename.txt
    ```
*   remove(item) - looks for value and removes index holding it (even if in multiple places)

    ```java
    String[] fruitsArray = {"apple", "banana", "kiwi", "mango"};
    ArrayList<String>  fruits = new ArrayList<>(Arrays.asList(fruitsArray));
    System.out.println("all: " + fruits.toString());

    String returned = fruits.remove(2);
    System.out.println("remove(2): " + fruits.toString());
    System.out.println("returned: " + returned);

    // all: [apple, banana, kiwi, mango]
    // remove(2): [apple, banana, mango]
    // returned: kiwi
    ```
*   find(item) - looks for value and returns first index with that value, -1 if not found

    ```java
    import java.util.regex.Matcher;  
    import java.util.regex.Pattern;  
      
    public class BooleanFindMethodExample1 {  
        public static void main(String[] args) {  
            // TODO Auto-generated method stub  
            Pattern p=Pattern.compile("java");  
            Matcher m=p.matcher("HellojavaHellojava");  
            int c=0;  
            // finding matching char   
            while(m.find())  
            {  
            c=c+1;  
            System.out.println("Start position of matching String "+m.start());  
            System.out.println("End position of Matching String (java) "+m.end());  
            }  
            System.out.println(" Number of matches : "+c);  
        }  
    }
    ```

    ```java
    Pattern pat = Pattern.compile("여기에 정규식 입력"); 
    패턴을 정의 한 후

    Matcher match = pat.matcher("여기에 조사할 문자열");
    정의된 패턴에 매치 되는 값을 저장한다.

    match.find()
    매치된 값이 있으면 true 없으면 false를 반환한다.

    match.group()
    매치된 값을 반환한다.
    ```
* resize(new\_capacity) // private 함수
  * 용량이 꽉 차면, 그 두배로 크기를 조정한다.
  * item을 하나 꺼낼 때, 용량이 1/4이라면, 용량을 절반으로 줄인다.
