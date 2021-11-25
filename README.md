# Csharp
 c# practise
 
 
 Create and load a matrix of 4 rows by 4 columns of decimal numbers.
(a) Program must print the main diagonal in binary code (format must be 8 bits).
x - - - 
- x - - 
- - x –
- - - x 
(b) Program must calculate for the diagonal showed character representation for each 
number on the diagonal (ascii code) if it is possible and manage possible exemptions and 
errors. 
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Text; 
using System.Threading.Tasks; 
namespace Ques2 
{ 
 class matrice 
 { 
 public struct Matrix4x4 
 { 
 public static void Main() 
 { 
 int i, j; 
 int[,] arr1 = new int[4,4]; 
 Console.Write("\n\nRead a 3D array of size 4x4 and print the matrix :\n"); 
 Console.Write("------------------------------------------------------\n"); 
Confidentiality Class
Ericsson Internal
External Confidentiality Label
Commercial in Confidence
Document Type
Check List
Page
4 (8) 
Prepared By (Subject Responsible)
EGONSAL Salvador Gonzalez Perez 
Approved By (Document Responsible)
BNEWNBBAD
Checked Document Number TLL-RPTD-100/CT0002 Uen Revision Date B 2021-02-12 Reference 
 /* Stored values into the array*/ 
 Console.Write("Input elements in the matrix :\n"); 
 for (i = 0; i < 4; i++) 
 { 
 for (j = 0; j < 4; j++) 
 { 
 Console.Write("element - [{0},{1}] : ", i, j); 
 
 arr1[i, j] = Convert.ToInt32(Console.ReadLine()); 
 } 
 } 
 Console.Write("\nThe matrix is : \n"); 
 for (i = 0; i < 4; i++) 
 { 
 Console.Write("\n"); 
 for (j = 0; j < 4; j++) 
 Console.Write("{0}\t", arr1[i, j]); 
 } 
 Console.Write("\n\n"); 
 b ) Console.Write("\nThe matrix in the value with binary on the diagnol : \n"); 
 for (i = 0; i < 4; i++) 
 { 
 Console.Write("\n"); 
 for (j = 0; j < 4; j++) 
 { 
 if (i == j) 
 { 
 string binary = Convert.ToString(arr1[i, j], 2).PadLeft(8, '0'); 
 Console.Write("{0}\t", binary); 
 } 
 else 
 { 
 Console.Write("{0}\t", arr1[i, j]); 
 } 
 } 
 } 
 Console.Write("\n\n"); 
 Console.ReadLine(); 
 } 
 } 
 } 
}

