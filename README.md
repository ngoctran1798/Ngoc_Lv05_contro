#Trần Thị Ngọc
##**Báo cáo học Con trỏ**    
[Khái niệm](#Khái_niệm)    
[Con trỏ với mảng một chiều](#Mảng_một_chiều)    
[Con trỏ với mảng nhiều chiều](#Mảng_nhiều_chiều)   
[Phép toán trên con trỏ](#Phép_toán)   
[Con trỏ mảng](#Con_trỏ_mảng)  

<a name = Khái_niệm><a\>    
###1. Khái niệm:  
**Con trỏ được dùng để trỏ tới tới địa chỉ trên bộ nhớ nơi được dùng để lưu trữ giá trị của biến.**  
*Một biến sau khi khai báo nó sẽ có 4 đặc tính như sau:*  
-Tên biến  
-Giá trị hiện tại của biến  
-Địa chỉ trên bộ nhớ nơi lưu trữ giá trị của biến  
-Kiểu dữ liệu  
Khai báo:    
`<kiểu_DL> * <tên_biến_con_trỏ>;`  
VD:`int x = 45;`   

<a name = Mảng_một_chiều><a\>  
###2. Con trỏ và mảng 1 chiều    
*Các phần tử của mảng có thể được xác định thông qua con trỏ.*    
VD: Nhập từ bàn phím các phần tử của mảng và tính tổng các phần tử đó  
`   float a[5], s ; int i;      
    for(i=0;i<5;i++)      
    {      
        printf(“\na[%d]= ”,i);       
        scanf(“%f”,&a[i]);    
    }    
    s=0;    
    for (i=0;i<5;i++) s+=a[i];      
    printf(“\n Tong =%8.2f”,s);      
}`    

<a name = Mảng_nhiều_chiều><a\>    
###3. Con trỏ với mảng nhiều chiều    
*Ðể tính toán địa chỉ của thành phần a[i][j] chúng ta sử dụng công thức sau : (float *)a+i*n+j.  
a là một hằng con trỏ trỏ đến các dòng của một ma trân hai chiều, vì vậy:    
a trỏ đến dòng thứ nhất  
a+1 trỏ đến dòng thứ hai  
a+2 trỏ đến dòng thứ ba*  

VD: nhập giá trị của ma trận hai chiều:  
`   float a[10][20];      
    int i,j,n;  
    printf("Nhap vao kich thuoc ma tran n=");      
    scanf("%n",&n);    
    for(i=0;i<n;i++)    
        for(j=0;j<n;j++)    
        {     
            printf("a[%d][%d] = ",i,j);    
            scanf("%f",(float *)a+i*20+j);    
        }     
}`    
<a name = Phép_toán><a\>
###4. Phép toán trên con trỏ  
*1. Phép gán*  
Chỉ nên thực hiện trên các con trỏ có cùng kiểu, khi thực hiện trên con trỏ phải thực hiện phép ép kiểu:  
*2. Phép tăng giảm địa chỉ*  
*3. Phép so sánh*    

<a name = Mảng_con_trỏ><a\>  
###5. Mảng con trỏ  
*Mảng con trỏ là một mảng mà mỗi phẩn tử của nó có thể chứa một địa chỉ nào đó. Mảng con trỏ có nhiều kiểu, mỗi phẩn tử của mảng kiểu nào thì sẽ chứa địa chỉ kiểu tương ứng với nó. Mảng con trỏ được khai báo theo mẫu sau: <kiểu Dl> *<tênmảng>[N]*  
*Khi gặp khai báo mảng con trỏ thì máy sẽ cấp phát N khoảng nhớ liên tiếp cho N phần tử tương ứng trong mảng.*  
