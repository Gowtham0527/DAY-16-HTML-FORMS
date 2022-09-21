
//to autopopulate countries and states in dropdown-passing the id of country and state select element
populateCountries("country","state");

populateStates("country","state");

let form= document.getElementById("form");

form.addEventListener("submit",formHandler)

function formHandler(event){
    event.preventDefault();

    let selectedFood=[];
    let foodError = false;

    for(let option of document.getElementById("food").options)
    {
        if(option.selected){
            selectedFood.push(option.value);
        }
    }
//display error message if user selects lessthan 2 food
   if(selectedFood.length < 2){
    document.getElementById('food-error').innerText = "Select atleast 2 options from food";
    document.getElementById('food-error').display = "block";
    foodError = true;
   }
   else{
    document.getElementById('food-error').innerText = "";
    document.getElementById('food-error').display = "none";
   }

   let firstName= document.getElementById("first-name").value;

   let lastName= document.getElementById("last-name").value;

   let address= document.getElementById("address").value;

   let pincode= document.getElementById("pincode").value;

   let selectedGender = ""
   let gender = document.getElementsByName('gender');
   for(let i=0;i<gender.length;i++){
    if(gender[i].checked){
        selectedGender = gender[i].value;
    }
   }


let tempCountry = document.getElementById("country");
let selectedCountry = tempCountry.options[tempCountry.selectedIndex].value; 

let tempState = document.getElementById("state");
let selectedState = tempState.options[tempState.selectedIndex].value; 

//create object and pass the values to populate table
let obj ={
    firstName:firstName,
    lastName:lastName,
    address:address,
    pincode:pincode,
    gender:selectedGender,
    food:selectedFood,
    state:selectedState,
    country:selectedCountry
}

//call function to populate table values only when there is no food error
if(!foodError){
    populateTable(obj);
}

}

function populateTable(obj){
    //create row element
    let trEle = document.createElement("tr");
    let tdEle;

    let entries = Object.entries(obj);

    entries.map(([key,val],index) => {
        //create td element
        tdEle = document.createElement("td");
        //set value to td
        tdEle.innerHTML = val;
        //append td to tr
        trEle.appendChild(tdEle);
    })
    
    //append tr to table body
    let tableBody= document.getElementById("tableBody");
    tableBody.appendChild(trEle);
}