# JS_Alogrithms
Javascript Interview Alogrithms


//Check if Prime Number

function checkPrime(number){
	var isPrime = false;

for(var i =1; i < 10; i++){
	if(number%i == 0 && number != i && i != 1){
		isPrime = true;
		return isPrime;
	}
}
return isPrime;

}

// Get Prime Numbers

function getPrimeNumbers(number){
	var factors = [];
	var divisor = 2;

	while(number > 2){
		if(number%divisor == 0){
			factors.push(divisor);
			number = number/divisor;
		}
		else(){
			divisor ++;
		}
	}
	return factors;
}


//Add up preceding number

function addPrecedingValue(array){
	var fib = 0;
	for(var i = 0; i <array.length; i++){
		fib += array[i];
	}
	return fib;
}

//Get fibonacci number @ Fn



function getFibonacciFn(n){
	var fib = [0,1]
	if(n <=2){return 1;}

	for(var i = 2; i <=n; i++){
		fib[i] = fib[i-1] + fib[i-2];
	}
	return fib[n];

}

// Get greatest common divisor
function getGreatestCommonDivisor(x, y){

	var divisor = 2;
	var greatestCommon = 0;

	if(x <= 2 && y <= 2){
		return 1;
	}

	while(x >= divisor && y >= divisor){
		if(x%divisor == 0 && y%divisor ==0){
			greatestCommon = divisor;
		}
		divisor++;
	}

	return greatestCommon;
}

// Remove Duplicates from Array

function removeDupes(array){
	var obj = {};
	for(var i =0; i < array.length; i++){
		if(!obj[array[i]])
		{
			obj[array[i]] = i;
		}
		else {
			array.splice(i,1);
		}
	}
	return array;

}

//Merge two sorted arrays

function mergedSorted(a,b){
	var merged = [],
	i = 0,
	j = 0,
	bell = b[i],
	ace = a[j];

	if(b.length == 0){
		return a;
	}
	if(a.length == 0){
		return b;
	}
	

	while(bell || ace){
		if(ace < bell || (ace && !bell)){
			merged.push(ace);
			ace = a[i++];
		}
		else{
			merged.push(bell);
			bell = b[j++];
		}
}
	console.log(merged);

}


// Swap numbers without a temp variable

function swapGuys(a,b){
	b = b-a;
	a = a+b;
	b = a-b;

	console.log("a is now " + a + " b is now " + b);
}

// Reverse a string a.k.a. check if palindrome

function palindrome(string){
	return string.split('').reverse().join('');
}


// Reverse words in a sentence Ex. This guy fucks ---> fucks guy this

function reverseWords(string){
	return string.split(" ").reverse().join(" ");
}

// Reverse words in place Ex. This guy fucks --> sihT yug skuf

function thisGuy(string){
	var reversed = string.split(" ").forEach(function(value){value.split("").reverse().join("");});
	return reversed.join(" ");
}

// split string in place

function reverse(word){
	var arry = [];
	

	for(var i = string.length-1; i>-1; i--){
		arry.push(string[i]);
	}
	arry.join("word");
	


}