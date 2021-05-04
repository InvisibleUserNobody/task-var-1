let arr = [];
let localMaxArr = [];
let localMaxNum = 0;
for(let i = 1; i>0; i++){
    let x = +prompt("Введите число");
    if (x == '' || isNaN(x)==true) break;         
    arr.push(x);
}
console.log(arr.join(" "));
    
for(let i = 0; i<=arr.length; i++){

    if(localMaxNum<arr[i]){
    localMaxNum = arr[i];
    }

    else if(localMaxNum>arr[i]){
    i=i-1;

    if(localMaxNum<=arr[i]){
        localMaxArr.push(localMaxNum);
        localMaxNum = arr[i];   
    }

    i=i+1;    
    }
}

let divs1 = document.createElement("div");
document.body.append(divs1);
divs1.innerHTML = "Изначальный массив  =>  "+arr.join(", ")+"</br>"+"Максимальные числа     => "+localMaxArr.join(", ");

let polyStr = prompt("Ведите слово");
let polyCheck = "";
polyCheck = polyStr;
polyCheck = polyCheck.split("").reverse().join("");

let divs2 = document.createElement("div");
document.body.append(divs2);

if(polyStr===polyCheck){
    divs2.innerHTML = "Слово "+polyStr+" является полиморфом."
}
else{
    divs2.innerHTML = "Слово "+polyStr+" не является полиморфом."
}
