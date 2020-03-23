# js-verk2
### 2.1 Spurningar
#### 1. Afhverju er `getElementById()` fljótleglegasta aðferðin?
```Því að það er beint kall í javascript.```
#### 2. Hver er munurinn á static og live NodeList?
``` Static Nodelist hafa enga áhrif á kóðan safnið eftir breytingum á DOM. Live Nodelist lætur kóðan automatically updata kóða safnið.```
#### 3. Hver er munurinn á true og false í AddEventListener?

```True: er Capture og fer frá top elementinu og niður.
   False: er bubbling og fer frá neðsta elementinu og upp.
  ```
#### 4. this vísar í Event listener á html element en ekki á object. Þú getur notað `bind()` til að breyta því. Leystu eftirfarandi kóðadæmi með notkun á `bind()` til að birta í console “My name is Sam“ en ekki undefined.
```javascript
let Person = {
  name: 'Sam', 
  sayName: function(){
    console.log('My name is '+ this.name);
  }
};
buttonEl.addEventListener('click', Person.sayName.bind(Person));
```

### 2.1 DOM
#### 1. Notaðu `querySelector()` til að velja málsgrein nr 1. og litaðu textann rauðan.
```javascript
  document.querySelector("p").style.color = "red";
```
#### 2. Veldu allar málgreinar og breyttu textanum í ensku með textContent aðferðinni.
``` javascript
let x = 0;
const parag = document.querySelectorAll("p");
parag.forEach(element => {
  x++;
  element.textContent = "paragraph "+ x;
});
```
#### 3. Bættu við efst með `InnerHTML` `<h1>` með textanum Verkefni 2.2.

```javascript
  document.body.innerHTML = "<h1>Verkefni 2.2</h1>" + document.body.innerHTML; 
```
#### 4. Bættu við neðst með `createElement()` og `append()` málsgrein með nafninu þínu.
```javascript
  let me = document.createElement("p");
  me.innerHTML = "Lorraine";
  document.body.appendChild(me); 
  ```
