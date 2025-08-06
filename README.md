# js-homework
// 41. function vory kveradardzni true ete eranish tvi miavorneri tvanshany havasar lini
// tasnavorneri u haryuravorneri tvanshanneri gumarin, hakarak depqum false


function number(num) {
  if (num < 100 || num > 999) {
    return false; 
  }

  let units=num%10; 
  let tens=Math.floor((num%100)/ 10); 
  let hundreds=Math.floor(num /100);

  return units===(tens+hundreds);
}
console.log(number(235));
console.log(number(404));

//42. function vory kveradardzni true ete eranish tvi mej kan irar havasar tvanshanner
// hakarak depqum false
function number1(num) {
  if (num < 100 || num > 999) 
    return false;

  let units=num%10; 
  let tens=Math.floor((num % 100)/10); 
  let hundreds=Math.floor(num/100);

  return units === tens || units === hundreds || hundreds === tens;
}
console.log(number1(225));
console.log(number1(404))

//43. khashven ev ktpen eranish tvi ev ir tvanshanner gumari haraberutyany arjeqy
//  ete eranish tivy mets e trvats "k" tvic hakarak depqum miavorneri tvanshani ev eranish tvi haraberutyan arjeqy

function number2(num, k) {
  if (num < 100 || num > 999) {
    return;
  }

  let units=num % 10;
  let tens=Math.floor((num % 100) / 10);
    let hundreds=Math.floor(num/100);
    let sum=units+tens+hundreds

  if (num > k) {
    console.log(num/sum);
  } else {
    console.log(units/num);
  }
}
//44. khashven ev ktpen eranish tvi tvanshanneric amenametsy
function maxNumber(num) {
  let digits=num.toString().split("");
  let max=0;

  for (let i= 0; i <digits.length; i++) {
    let digit=parseInt(digits[i]);
    if (digit > max) {
      max=digit;
    }
  }

  return max;
}

console.log(maxNumber(472)); 

//45.khashven ev ktpen eranish tvi tvanshanneric amenapoqry
function minNumber(num) {
  let digits=num.toString().split("");
  let min=0;

  for (let i= 0; i<digits.length; i++) {
    let digit=parseInt(digits[i]);
    if (digit <min) {
      min=digit;
    }
  }

  return min;
}

console.log(minNumber(486)); 

//46. khashvi ev ktpi eranish tvi tvanshanneri haraberutyuny eranish tvin, ete
// miavorneri tvanshany mets e tasnavorneri tvanshanic hakarak depqum tpel eranish tivy


function number3(num) {
  if (num < 100 || num > 999) {
    return;
  }

  let units=num % 10;
  let tens=Math.floor((num % 100) / 10);
  let hundreds=Math.floor(num/100);
  let sum=units+tens+hundreds

  if (units>tens) {
    console.log(sum/num);
  } else {
    console.log(num);
  }
}


//47.  khashvi ev ktpi eranish tvi tvanshanneri ev miavorneri haraberutyuny, ete 
// ete eranish tivy > e 300ic, hakarak depqym haryursvornri ev miavorneri haraberutyan arjeqy
// (miavorneri arjeqy 0 che)


function number4(num) {
  if (num < 100 || num > 999) {
    return;
  }

  let units=num % 10;
  let tens=Math.floor((num % 100) / 10);
  let hundreds=Math.floor(num/100);

  if (units === 0) {
    return;
  }


  if (num>300) {
    console.log(tens/units);
  } else {
    console.log(hundreds/units);
  }
}


//48. f popoxakanin kveragrenq "a" arjeq, ete eranish tvi 
//tasnavorneri ev haryuravorneri gumary mets lini 5ic, hakarak depqum "b" arjeq

function number5(f) {
  if (f< 100 || f> 999) {
    return;
  }

  let tens=Math.floor((f % 100) / 10);
  let hundreds=Math.floor(f/100);


  if ((tens+hundreds)>5) {
    return "a";
  } else {
    return "b";
  }
}



// 49. ktpen eranish tvi tvanshannery dasavorvats achman kargov
function sort(num) {
  let sorted=num.toString().split('').sort().join('');      
  
  return parseInt(sorted);
}

console.log(sort(472)); 


// 50. ktpen eranish tvi tvanshannery dasavorvats nvazman kargov

// ---------------------------------


//51. t popoxakanin kvergrenq ture arjeqy ete qaranish tvi miavorneri ev tasnavorneri 
// tvanshanneri gumary =e haryuravorneri ev hazaravorneri tvanshanneri gumarin
// hakarak depqum ktpi false


function number5(num) {
  if (num < 1000 || num > 9999) {
    return;
  }

  let thousands=Math.floor(num/1000);
  let hundreds=Math.floor((num % 1000)/100);
  let tens=Math.floor((num % 100)/10);
  let units=num % 10;



  if (units+tens===hundreds+thousands) {
   return true
  } else {
   return false
  }
}


//52. khashven ev ktpen qaranish tvi haraberutyan arjeqy miavorneri ev haryuravorneri 
// tvanshanneri gumarin, ete qaranish tivy poqr e 5000ic, hakarak depqum tpel 
//  qaranish tvi haraberutyan arjeqy hazaravorneri ev haryuravorneri tvanshanneri gumarin
// (miavorner ev haryuravorner =che 0)

function number6(num) {
  if (num < 1000 || num > 9999) {
    return;
  }

  let thousands=Math.floor(num/1000);
  let hundreds=Math.floor((num % 1000)/100);
  let tens=Math.floor((num % 100)/10);
  let units=num % 10;
 if (units === 0) {
    return;
  }

 if (hundreds === 0) {
    return;
  }
let sum1=tens+units
let sum2=thousands+hundreds

  if (num<5000) {
   console.log(num/sum1)
  } else {
   console.log(num/sum2)
  }
}

//53. ktpi 1 ete qaranish tvi tvanshanneri mej ka "1" tvanshany, hakarak depqum 0

function number7(num) {
  if (num < 1000 || num > 9999) {
    return;
  }

  let thousands=Math.floor(num/1000);
  let hundreds=Math.floor((num % 1000)/100);
  let tens=Math.floor((num % 100)/10);
  let units=num % 10;
 if (units === 1 || tens === 1||hundreds === 1 ||thousands === 1) {
    console.log(1);
  }else{
    console.log(0)
  }

}

//54. y popoxakany kveradardzni "s" arjeq ete qaranish tvi miavorneri ev tasnaorneri tvanshanneri 
// gumary =e 5i hakarak depqum "d" arjeq

function number8(y) {
  if (y< 1000 || y> 9999) {
    return;
  }

  let tens=Math.floor((y% 100)/10);
  let units=y % 10;

let sum=tens+units


  if (sum===5) {
   return "s"
  } else {
  return "d"
  }
}


//55. ktpen y=12 ete qaranish tvi mej miavorneri u tasnavorineri artadryaly =e 12
// hakarak depqum y=0
function number9(y) {
  if (y< 1000 || y> 9999) {
    return;
  }

  let tens=Math.floor((y% 100)/10);
  let units=y % 10;

let product=tens*units


  if (product===12) {
   console.log(y=12);
   
  } else {
  console.log(y=0);
  }
}


//56. ktpi "YES" ete qaranish tvi arajin ev verjin tvanshani mej ka
// "4" tvanshany hakarak depqym "NO"

function number10(num) {
  if (num< 1000 || num> 9999) {
    return;
  }

  let thousands=Math.floor(num/1000);
  let units=num % 10;


  if (units===4 && thousands===4  ) {
   console.log("YES");
   
  } else {
  console.log("NO");
  }
}

//57. ktpi "YES" ete qaranish tivy = nra tvanshanneri gumari qarakusun
// hakarak depqum "NO"

function number11(num) {
  if (num< 1000 || num> 9999) {
    return;
  }

  let thousands=Math.floor(num/1000);
  let hundreds=Math.floor((num % 1000)/100);
  let tens=Math.floor((num % 100)/10);
  let units=num % 10; 
  
  let sum=(thousands+hundreds+tens+units)**2



  if (num===sum ) {
   console.log("YES");
   
  } else {
  console.log("NO");
  }
}


//58. khashven ev ktpen qaranish tvi miavorneri ev haryueavorneri artadryaly, ete
//miavorneri tvanshany mets e haryueavorneri tvanshanic, hakarak depqum ktpen "1"
function number11(num) {
  if (num< 1000 || num> 9999) {
    return;
  }

  
  let hundreds=Math.floor((num % 1000)/100);
  let units=num % 10; 
  
  if (units>hundreds) {
   console.log(units*hundreds);
   
  } else {
  console.log(1);
  }
}


//59.y popoxakany kveradardzni "1" arjeq ete qaranish tvi tvanshanneri  
// gumary >e 20ic hakarak depqum "0" arjeq

function number8(y) {
  if (y< 1000 || y> 9999) {
    return;
  }

  let thousands=Math.floor(num/1000);
  let hundreds=Math.floor((num % 1000)/100);
  let tens=Math.floor((num % 100)/10);
  let units=num % 10;

let sum=thousands+hundreds+tens+units


  if (sum>12) {
   console.log(1);
   
  } else {
  console.log(0)
  }
}


//60. y popoxakany kveradardzni "0" arjeq ete qaranish tvi tvanshanneri  
// artadryaly >e 200ic hakarak depqum "1" arjeq

function number8(y) {
  if (y< 1000 || y> 9999) {
    return;
  }

  let thousands=Math.floor(num/1000);
  let hundreds=Math.floor((num % 1000)/100);
  let tens=Math.floor((num % 100)/10);
  let units=num % 10;

let product=thousands*hundreds*tens*units


  if (product>200) {
   console.log(0);
   
  } else {
  console.log(1)
  }
}

//151. tpel bolor ayn bnakan tveri gumary voronc vra 
// aranc mnacord bajanvum e trvats "n" bnakan tivy  (?)

function divisible(n){
  let sum=0;

  for (let i=1; i<=100;i++) {
    if (i%n===0) {
      sum += i;
    }
  }

  return sum;
}

//152.  tpel bolor ayn bnakan tveri artadryaly voronc vra 
// aranc mnacord bajanvum e trvats "n" bnakan tivy  (?)
function divisible(n){
  let sum=0;

  for (let i=1; i<=100;i++) {
    if (i%n===0) {
      sum *= i;
    }
  }

  return sum;
}


//155. tpel bolor ayn bnakan erknish tveri gumary
// voronq bazmapatik en 3i

function divisible2(num){
  let sum=0;

  for (let i=10; i<=99;i++) {
    if (i%3===0) {
      sum += i;
    }
  }

  return sum;
}

//156. tpel bolor ayn bnakan erknish tveri artadryaly
// voronq bazmapatik en 3i ev 5i

function divisible(num){
  let product=1;

  for (let i=10; i<=99;i++) {
    if (i%3===0 && i%5===0 ) {
      product*= i;
    }
  }

  return product;
}


//157. tpel bolor ayn eranish tveri gumary
// voronq bazmapatik chen 5i

function divisible5(num){
  let sum=0;

  for (let i=100; i<=999;i++) {
    if (i%5!==0) {
      sum += i;
    }
  }

  return sum;
}

console.log(divisible5());


//158. tpel bolor ayn eranish tveri qanaky
// voronq bazmapatik chen 3i ev 2i

function divisible3(num){
   let count= 0

  for (let i=100; i<=999;i++) {
    if (i%2!==0 && i%3!==0) {
      count ++;
    }
  }

  return count;
}

console.log(divisible3());


//160. tpel ayn amenapoqr eranish tivy vory 16ov bazmapatkum es stacvum e bnakan tvi qarakusi
function find() {
  for (letx=100; x<=999; x++) {
    let product = x*16;
    let sqrt=Math.sqrt(product);

    if (Number.isInteger(sqrt)) {
      return x; 
    }
  }
}

console.log(find());



//161.tpel ayn amenapoqr qaranish tivy vory 26ov bazmapatkum es stacvum e bnakan tvi qarakusi

function find1() {
  for (let x=1000; x<=9999; x++) {
    let product = x*26;
    let sqrt=Math.sqrt(product);

    if (Number.isInteger(sqrt)) {
      return x; 
    }
  }
}

console.log(find1());

//162. tpel ayn amenamets qaranish tivy vory 14ov bazmapatkum es stacvum e bnakan tvi qarakusi

function findLargest() {
  for (let x=9999; x>=1000; x--) {
    let product=x*14;
    let sqrt=Math.sqrt(product);

    if (Number.isInteger(sqrt)) {
      return x;
    }
  }
}

console.log(findLargest());




//163. tpel ayn amenamets qaranish tivy vory 18ov bazmapatkum es stacvum e bnakan tvi qarakusi

function findLargest1() {
  for (let x=9999; x>=1000; x--) {
    let product=x*18;
    let sqrt=Math.sqrt(product);

    if (Number.isInteger(sqrt)) {
      return x;
    }
  }
}

console.log(findLargest1());



//165. t tramabanakan typi popoxakanin kveragri ture arjeq
// ete trvats n bnakan tivy 3i artichan e

function number(n) {
  if (n<1)
     return false;

  while (n%3===0) {
    n /= 3;
  }
  return n === 1;
}

function number4(n) {
  if (n<1)
     return false;

  while (n%4===0) {
    n /=4;
  }
  return n === 1;
}




//170. drakan tarreri mijin tvabanakany
function positive(arr) {
  let sum=0;
  let count=0;

  for (let i=0; i <arr.length; i++) {
    if (arr[i] > 0) {
      sum += arr[i];
      count++;
    }
  }
  if (count===0) {
    return 0; 
  }

  return sum/count;
}

//171. drakan tareri mijin erkrachapakan
function geometric(arr) {
  let product=1;
  let count=0;

  for (let i=0; i<arr.length; i++) {
    if (arr[i] > 0) { 
      product *= arr[i];
      count++;
    }
  }

  if (count===0)
     return 0; 

}


//175. zuyg index necox tareri gumar

function even(arr){
  let count=0;

  for (let i=0; i<arr.length; i++) {
    if (i%2===0) { 
      count++;
    }
  }
}


//176. zuyg index unecox tareri artadryaly
function even1(arr) {
  let product=1;
  let count=0;

  for (let i=0; i<arr.length; i++) {
    if (i%2===0) { 
      product *= arr[i];
      count++;
    }
  }

  if (count===0){
     return 0; 
  }
    
return product;
}

// 177. kent index unecox tareri qarakusineri artadryaly

function odd(arr) {
  let product=1;
  let count=0;

  for (let i=0; i<arr.length; i++) {
    if (i%2===1) { 
      product *= (arr[i]**2);
      count++;
    }
  }

  if (count===0){
     return 0; 
  }
    
return product;
}

//178. kent index unecox tareri bacardzak arjeqneri gumary
function sum(arr) {
  let sum=0;

  for (let i=1; i<arr.length; i+= 2) {
    sum += Math.abs(arr[i]);
  }

  return sum;
}

//180. trvats drakan ev bacasakan tarreri qanaky

function count(arr) {
  let positiveCount=0;
  let negativeCount=0;

  for (let i=0; i<arr.length; i++) {
    if (arr[i] > 0) {
      positiveCount++;
    } else if (arr[i] < 0) {
      negativeCount++;
    }
   
  }
}


//184.ayn tareri xoranardneri gumary voronq bacardzak arjeqov poqr en k tvic
function sum(arr, k) {
  let sum=0;

  for (let i=0; i< arr.length; i++) {
    if (arr[i] < 0 && arr[i] < k) {
      sum += (arr[i]**3) ;
    }
  }

  return sum;
}

//185 ayn tareri artadryaly voronq bacardzak arjeqov poqr en t tvic
function productNegative(arr, t) {
  let product=1;
  let count=0;

  for (let i = 0; i<arr.length; i++) {
    if (arr[i] < 0 && arr[i] < t) {
      product *= arr[i];
      count++;
    }
  }

}

//186. ayn tareri qanaky voronq bacardzak arjeqov poqr en k tvic
function countNeg(arr, k) {
  let count= 0;

  for (let i=0; i<arr.length; i++) {
    if (arr[i]<0 && arr[i]<k) {
      count++;
    }
  }

  
  return count;
}
