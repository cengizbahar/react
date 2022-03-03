## Callback Function

```
    // 2 saniye sonra hello dünya yazar
setTimeout(() => {
    console.log('hello dünya');
}, 2000);


// Her periyetto çalışır durdurmazsanız sürekli çalışır.
setInterval(() => {
    console.log('Merhaba');
});

// Paremetre olarak çalıştırma
const sayhello = (cb) => {
    cb();
}

sayhello(() => {
    console.log('hello')
});

// fetch işlemlerinde sıraya koyarak çagırma işlemi yapabiliriz,
// dışarıdan ayrı ayrı çağırırsak sıralamayı js kendisi belirler, iç içe olarak düzgün çağırma işlemi yapabiliriz.
npm i node - fetch

import fetch from 'nonde-fetch'

fetch("https://jsonplaceholder.typicode.com/users") {
    .then((data) => data.json())
        .then((users) => {
            console.log("users Yuklendi", users);
});

// axios en iyi kullanılan

async function getData() {
        const users = await (
            await fetch("https://jsonplaceholder.typicode.com/users")
        ).json();

        const post1 = await (
            await fetch("https://jsonplaceholder.typicode.com/posts/1")
        ).json();

        console.log("users", users);
        console.log("post1", post1);
    }

    getData();



// axios npm i axios
import axios from "axios";

( async () => {
    const {data: users} = await axios("https://jsonplaceholder.typicode.com/users");

    console.log("users",users);
})();


```

## Promise 
```
// Promise konusu
// eger 1 e eşitse resolve dönecek degiselse reject olacak
// promise kullanımı bu şekilde


const getComments = (number) => {
    return new Promise((resolve, reject) => {
      if (number === 1 ) {
          resolve({text: "selam"});
      }
      reject ("bir problem oluştu!");
    }); 
};

getComments(1)
.then(() => console.log(data))
.catch((e) => console.log(e));


// try catch arasına alırsa hatayı loglayabiliriz.


```

## Array Function
```
// array function 
// push , map , find , filter , some, every //


const users = [
    { 
    name: "cengiz",
    age: 18,
},
{
    name: "sedat",
    age: 21,
}
];

// Push ekleme
users.push("ayşe")
console.log(users)

// map döngü
users.map((item) => {
    console.log(item.name);
});

// find
const result = users.find((item) => item.name === "mehmet" && item.age > 20);
console.log(users)

// filter filtreledigimiz alanları getirir && ve 
const filter = users.filter(({name, age}) => name === "mehmet" && age < 20 );
console.log(filter)

//some 1 şart sağlandıgında true döner
const some = users.some((item) => item.name === cengiz);
console.log(users)

// every tüm şartlar uygunsa true döner

const every = users.every((item) => item.age >20);
console.log(every);




// includes var mı yok mu diye kontrol ediyor 
const meyveler = ["armut","elma","kiraz"];

const inclued = meyveler.includes("portakal");
console.log(inclued);
```
 
## Koşullu Render ? = ise   : = else
```
const isLoggdIn = false;
const name = "cengiz";
const surname = "bahar";

function app(){
    return (
        <div> 
            {ìsLoggdIn ? `benim adım {name}, soyadım {surname}` :  `giriş yapmadınız` }
        </div>
    )
}

```
