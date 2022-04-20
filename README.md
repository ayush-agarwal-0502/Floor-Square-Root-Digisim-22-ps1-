# Floor-Square-Root-Digisim-22-ps1-
Digital Electronics Circuit for returning the floor of the square root of the inputted number . Digisim 22 PS1 Udyam .

## Introduction :

* Team Name - Technites 
* Team members - Ayush Agarwal (me) , Bhavna Chavan 
* Project Skills - Digital Electronics 
* Project Tools - Proteus 
* Event - DIGISIM 22 PS1 UDYAM 

## The PS :

## The PS but in short :

Design a digital electronics circuit which takes in a 10 bit number and returns the floor of the square root of the number . 

## Approaches :

* Approach 1 - The time efficient approach - O(1) Complexity - ( we didnt use this as cost was more important in ps than time ) 

In this , we compare the number with all possible solutions , and then return the answer . For eg , if the input was 4 bit , and we were given some input value say 11 , then we compare it with 1 , 4 , 9 , 16 and then pass the outputs of the compartors to the priority encoder , which would retur 3 for 11 (... and so on , hope you get the idea ) 

* Approach 2 - The cost effective approach - O(n) Complexity - ( We used this ) 

In this , we run a counter starting from 0 , square the number ( using a multiplier ofc) , and then compared to the input number . If it is exactly equal then we return the number in the counter , and if the square is more then we return one less than the value in the counter .

int n ; // n is the input value 

int x ; // x is the output value 

for(x=0; x<n ; x++){

if(n==(x*x)){

return x;

}

else if( n>(x*x) ) {

return (x-1) ;

}

}
