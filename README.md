# homework10
//point 1
function randomInRange() {
    return Math.floor(Math.random() * 101); 
 }
  
  // Example usage:
 console.log(randomInRange())

//point 2
function generateRandomString(length) {
    var result = '';
    var characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+-=[]{}|;:,.<>?';
    
    for ( var i = 0; i < length; i++ ) {
    result += characters.charAt(Math.floor(Math.random() * characters.length));
    }   
    return result;
    }  
    // Contoh penggunaan:
    var randomString = generateRandomString(10);
    console.log(randomString); // Output: ?Wo6-[N!bJ

//point 3
function splitString(str) {
    let arr = str.split(' '); // membagi string dengan spasi sebagai pemisah
    return arr;
  }
  
  let string = 'Halo semuanya, semoga sehat selalu';
  let result = splitString(string);
  
  console.log(result); // Output: ['Halo', 'semuanya,', 'semoga', 'sehat', 'selalu']

// point 4
function isLeapYear(year) {
    // tahun kabisat jika habis dibagi 4 dan bukan habis dibagi 100 atau habis dibagi 400
    return (year % 4 == 0 && year % 100 != 0) || year % 400 == 0;
    }
    
    // contoh penggunaan
    console.log(isLeapYear(2020)); // true
    console.log(isLeapYear(2021)); // false
    console.log(isLeapYear(2000)); // true
    console.log(isLeapYear(1900)); // false

//point 5 
function printData(data) {
    data.forEach(function(item) {
    console.log("Name: " + item.name + ", Age: " + item.age);
    })
    }
    
    var input = [
    {
    name: "ilhamsar",
    age: 21
    },
    {
    name: "fadli",
    age: 18
    },
    {
    name: "yusuf",
    age: 20
    }
    ];
    
    printData(input); 

//point 6
function filterPeopleByStatus(people, jobStatus) {
  const filteredPeople = people.filter(person => person.social === jobStatus);
  const groupedPeople = {};

  filteredPeople.forEach(person => {
    const key = `${person.sex}_${person.age}_${person.marital}`;
    if (!groupedPeople[key]) {
      groupedPeople[key] = [];
    }
    groupedPeople[key].push(person);
  });

  return groupedPeople;
}

const people = [
  {
    name: "udin",
    sex: "male",
    age: 10,
    marital: "single",
    social: "student"
  },
  {
    name: "ujang",
    sex: "male",
    age: 25,
    marital: "married",
    social: "employee"
  },
  {
    name: "icih",
    sex: "female",
    age: 10,
    marital: "single",
    social: "student"
  },
  {
    name: "eneng",
    sex: "female",
    age: 100,
    marital: "married",
    social: "employee"
  },
  {
      name: "asep",
      sex: "male",
      age: 20,
      marital: "single",
      social: "employee"
  },
];

const jobStatus = "employee";
const groupedPeople = filterPeopleByStatus(people, jobStatus);
console.log(groupedPeople);

// point 7
function countA(word, noOfLoop) {
    let count = 0;
    for (let i = 0; i < word.length * noOfLoop; i+= noOfLoop) {
    if (word[i % word.length] === "a") {
    count++;
    }
    }
    return count;
    }
    
    console.log(countA("ahhahgafahaskdhagafshaha", 3)); // Output: 3
