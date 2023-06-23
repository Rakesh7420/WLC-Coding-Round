# WLC-Coding-Round
WLC Coding Round Repo
<?php


Burgerking sells three items: 
VegBurger which needs 2 breads & 1 veg pattice
NonVegBurger which needs 2 breads & 1 non-veg pattice
TikkiBurger which needs 2 breads & 1 tikki pattice

Given bread quantity, veg pattice quantity, non-veg pattice quantity, tikki pattice quantity & price of all 3 items

Print the total maximum possible profit by making all possible items based on bread availability 

Also, test for all inputs, we would change all the values while testing, the quantity values as well as price

And program has to be optimal with respect to time & space complexity

*/

$breads = 15;
$vegPattice = 3;
$nonVegPattice = 2;
$TikkiPattice = 1;
$priceVegBurger = 100;
$priceNonVegBurger = 125;
$priceTikkiBurger = 112;

$maxProfit = 0;

/*   In this Question we have to find out the max profit made by selling th Burger.
     To make one Burger we need 2 breads and one pattice
     As we can see there are three types of burger  1) VegBurger
                                                    2) NonVegBurger
                                                    3) TikkiBurger
     and for making max profit we have to prefer to make high cost burger as maximum quantity
     The highest cost burger is NonVegBurger and second highest cost burger is TikkiBurger if still we have bread then we can make VegBurger
     
*/
     // first we divided bread into half by that we can know how many n0 of burger we can make
     $breads = $breads/2;
     
    // if we have breads then we are first going to make as many as non-veg Burger
     if($breads > 0){
         
       if($nonVegPattice > 0 && $nonVegPattice <= $breads){
         $breads = $breads - $nonVegPattice; 
         $maxProfit += $priceNonVegBurger * $nonVegPattice; 
       
       }
       // if we dont have sufficient bread then we can make equal no of breads
      else{
       
         $maxProfit += $priceNonVegBurger * $breads; 
        $breads = 0;
       
      }
    }
    
    // in this condition we are Counting 
    if($breads > 0){
      if($TikkiPattice > 0 && $TikkiPattice <= $breads){
        $breads = $breads - $TikkiPattice;
        $maxProfit += $priceTikkiBurger * $TikkiPattice; 
       
      }
       // if we dont have sufficient bread then we can make equal no of breads
      else{
   
        $maxProfit +=$priceNonVegBurger * $breads;
        $breads = 0;
       
      }

    }
    
    if($breads > 0){

      if($vegPattice > 0 && $vegPattice <= $breads){
        $breads = $breads - $vegPattice;
        $maxProfit += $priceVegBurger * $vegPattice; 
      
      }
       // if we dont have sufficient bread then we can make equal no of breads
      else{
       
         $maxProfit += $priceNonVegBurger * $breads; 
        $breads = 0;
     
      }
    }
    
    echo $maxProfit

?>


<?php
// Your code here!
/* 

Burgerking sells three items: 
VegBurger which needs 2 breads & 1 veg pattice
NonVegBurger which needs 2 breads & 1 non-veg pattice
TikkiBurger which needs 2 breads & 1 tikki pattice

Given bread quantity, veg pattice quantity, non-veg pattice quantity, tikki pattice quantity & price of all 3 items

Print the total maximum possible profit by making all possible items based on bread availability 

Also, test for all inputs, we would change all the values while testing, the quantity values as well as price

And program has to be optimal with respect to time & space complexity

*/

$breads = 15;
$vegPattice = 3;
$nonVegPattice = 2;
$TikkiPattice = 1;
$priceVegBurger = 100;
$priceNonVegBurger = 125;
$priceTikkiBurger = 112;

$maxProfit = 0;

/*   In this Question we have to find out the max profit made by selling th Burger.
     To make one Burger we need 2 breads and one pattice
     As we can see there are three types of burger  1) VegBurger
                                                    2) NonVegBurger
                                                    3) TikkiBurger
     and for making max profit we have to prefer to make high cost burger as maximum quantity
     The highest cost burger is NonVegBurger and second highest cost burger is TikkiBurger if still we have bread then we can make VegBurger
     
*/
     // first we divided bread into half by that we can know how many n0 of burger we can make
     $breads = $breads/2;
     
    // if we have breads then we are first going to make as many as non-veg Burger
     if($breads > 0){
         
       if($nonVegPattice > 0 && $nonVegPattice <= $breads){
         $breads = $breads - $nonVegPattice; 
         $maxProfit += $priceNonVegBurger * $nonVegPattice; 
       
       }
       // if we dont have sufficient bread then we can make equal no of breads
      else{
       
         $maxProfit += $priceNonVegBurger * $breads; 
        $breads = 0;
       
      }
    }
    
    // in this condition we are Counting 
    if($breads > 0){
      if($TikkiPattice > 0 && $TikkiPattice <= $breads){
        $breads = $breads - $TikkiPattice;
        $maxProfit += $priceTikkiBurger * $TikkiPattice; 
       
      }
       // if we dont have sufficient bread then we can make equal no of breads
      else{
   
        $maxProfit +=$priceNonVegBurger * $breads;
        $breads = 0;
       
      }

    }
    
    if($breads > 0){

      if($vegPattice > 0 && $vegPattice <= $breads){
        $breads = $breads - $vegPattice;
        $maxProfit += $priceVegBurger * $vegPattice; 
      
      }
       // if we dont have sufficient bread then we can make equal no of breads
      else{
       
         $maxProfit += $priceNonVegBurger * $breads; 
        $breads = 0;
     
      }
    }
    
    echo $maxProfit

?>


