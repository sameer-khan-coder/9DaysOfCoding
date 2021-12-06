# 9DaysOfCoding
CODING COMPETITION
//program-3
#include<iostream>
int squareSum(int);
using namespace std;
int main()
{
    cout<< squareSum(8);
    return 0;
} 
int squareSum(int n)
{
    int sum = 0;
    for (int i = 1; i <=  n; i++)
        sum += (2*i - 1) * (2*i - 1);
    return sum;
}

//program-5
#include <iostream>
#include <stdio.h>

using namespace std;

int main()
{
    cout << "\n\nWelcome to Studytonight :-)\n\n\n";
    cout << "Program to Reverse the String without using System defined function\n\n";

    //Variable Declaration
    char s1[100], c = 'a';
    int n = 0, i = 0;

    cout << "\n\nEnter the String you want to reverse: ";
    cin >> s1;

  

    //Declaring another char array to store the reverse of the string
    char s2[i];

    i = 0;
    //Logic to store the reverse of a string in another char array
    while (i != n + 1)
    {
        s2[i] = s1[n - i - 1];
        i++;
    }

    cout << "\n\nReverse of the entered string \"" << s1 << "\" is : \"" << s2 << "\"\n\n\n";

    return 0;
}
  
  
//program-9
  
  #include <iostream>  
using namespace std;  
int main()  
{  
long int n,sum=0,r;    
cout<<"Enter the Number= ";    
cin>>n;    
while(n>0)    
{    
r=n%10;    
sum=sum*10+r;    
n=n/10;    
}    
n=sum;    
while(n>0)    
{    
r=n%10;    
switch(r)    
{    
case 1:    
cout<<"one ";    
break;    
case 2:    
cout<<"two ";    
break;    
case 3:    
cout<<"three ";  
break;    
case 4:    
cout<<"four ";  
break;    
case 5:    
cout<<"five ";  
break;    
case 6:    
cout<<"six ";   
break;    
case 7:  
cout<<"seven ";  
break;  
case 8:    
cout<<"eight ";    
break;    
case 9:    
cout<<"nine ";  
break;    
case 0:    
cout<<"zero ";  
break;    
default:    
cout<<"tttt ";    
break;    
}    
n=n/10;    
}    
}  
  
//program-10
#include<iostream>
using namespace std;
int main()
{
    int arr[50], i, elem, pos, tot;
    cout<<"Enter the Size for Array: ";
    cin>>tot;
    cout<<"Enter "<<tot<<" Array Elements: ";
    for(i=0; i<tot; i++)
        cin>>arr[i];
    cout<<"\nEnter Element to Insert: ";
    cin>>elem;
    cout<<"At What Position ? ";
    cin>>pos;
    for(i=tot; i>=pos; i--)
        arr[i] = arr[i-1];
    arr[i] = elem;
    tot++;
    cout<<"\nThe New Array is:\n";
    for(i=0; i<tot; i++)
        cout<<arr[i]<<"  ";
    cout<<endl;
    return 0;
}
               
//program-8
               
#include<iostream>
using namespace std;
 
// Function to count uppercase, lowercase,
// special characters and numbers
void Count(string str)
{
    int upper = 0, lower = 0, number = 0, special = 0;
    for (int i = 0; i < str.length(); i++)
    {
        if (str[i] >= 'A' && str[i] <= 'Z')
            upper++;
        else if (str[i] >= 'a' && str[i] <= 'z')
            lower++;
        else if (str[i]>= '0' && str[i]<= '9')
            number++;
        else
            special++;
    }
    cout << "Upper case letters: " << upper << endl;
    cout << "Lower case letters : " << lower << endl;
    cout << "Number : " << number << endl;
    cout << "Special characters : " << special << endl;
}
 
// Driver function
int main()
{
    string str = "%#vhrdbvsdFSGDH990";
    Count(str);
    return 0;
}
                                                      
//program-11
               
#include <iostream>
using namespace std;
   
int main(){
    int input[100], count, i, num;
       
    cout << "Enter Number of Elements in Array\n";
    cin >> count;
     
    cout << "Enter " << count << " numbers \n";
      
    // Read array elements
    for(i = 0; i < count; i++){
        cin >> input[i];
    }
      
    cout << "Enter a number to serach in Array\n";
    cin >> num;
      
    // search num in inputArray from index 0 to elementCount-1 
    for(i = 0; i < count; i++){
        if(input[i] == num){
            cout << "Element found at index " << i;
            break;
        }
    }
      
    if(i == count){
        cout  << "Element Not Present in Input Array\n";
    }
 
    return 0;
}
                 
//program-2
                 
using namespace std;
class gfg {
public:
    int sumDigits(int no)
    {
        if(no == 0){
          return 0 ;
        }
       
        return (no % 10) + sumDigits(no / 10) ;
    }
};
 
// Driver code
int main(void)
{
    gfg g;
    cout << g.sumDigits(687);
    return 0;
}
         
//program-6
                            
 using namespace std;
 
// Function to convert binary to decimal
int binaryToDecimal(string n)
{
    string num = n;
    int dec_value = 0;
 
    // Initializing base value to 1, i.e 2^0
    int base = 1;
 
    int len = num.length();
    for (int i = len - 1; i >= 0; i--) {
        if (num[i] == '1')
            dec_value += base;
        base = base * 2;
    }
 
    return dec_value;
}
 
// Driver program to test above function
int main()
{
    string num = "10101001";
    cout << binaryToDecimal(num) << endl;
}                           
  
//program-13
  
#include <iostream>
#include <string.h>
#include <conio.h>
#include <cstring>
using namespace std;
int vowelChk(char);
int main(){
   char s[50], t[50];
   int c, d = 0;
   cout<<"Enter a string to delete vowels\n";
   cin>>s;
   for(c = 0; s[c] != '\0'; c++) {
      // check for If not a vowel
      if(vowelChk(s[c]) == 0){
         t[d] = s[c];
         d++;
      }
   }
   t[d] = '\0';
   strcpy(s, t);
   cout<<"String after delete vowels:"<<s;
   return 0;
}
int vowelChk(char ch){
   if (ch == 'a' || ch == 'A' || ch == 'e' || ch == 'E' || ch == 'i' || ch == 'I' || ch =='o' || ch=='O' || ch == 'u' || ch == 'U')
      return 1;
   else
      return 0;
}
  
//program-14
  
#include <iostream>
using namespace std;
 
// Function which pushes all zeros to end of an array.
void pushZerosToEnd(int arr[], int n)
{
    int count = 0;  // Count of non-zero elements
 
    // Traverse the array. If element encountered is non-
    // zero, then replace the element at index 'count'
    // with this element
    for (int i = 0; i < n; i++)
        if (arr[i] != 0)
            arr[count++] = arr[i]; // here count is
                                   // incremented
 
    // Now all non-zero elements have been shifted to
    // front and  'count' is set as index of first 0.
    // Make all elements 0 from count to end.
    while (count < n)
        arr[count++] = 0;
}
 
// Driver program to test above function
int main()
{
    int arr[] = {1, 9, 8, 4, 0, 0, 2, 7, 0, 6, 0, 9};
    int n = sizeof(arr) / sizeof(arr[0]);
    pushZerosToEnd(arr, n);
    cout << "Array after pushing all zeros to end of array :\n";
    for (int i = 0; i < n; i++)
        cout << arr[i] << " ";
    return 0;
}  
