# JavaScript Practice

- [ProtoType](#ProtoType)
- [Window](#Window)

  ### ProtoType
  ```js
    const bercelona = {
      jerseyNumber: '',
      name: '',
      country: '',
      position: '',
  
      __proto__: {
          bercelonaPlayer: false,
  
          playerRegistration(jerseyNumber, name, country, position){
              this.jerseyNumber = jerseyNumber;
              this.name = name;
              this.country = country;
              this.position = position;
  
              console.log(`You are succesfully signup for FC Barcelona`);
          },
  
          playerIdentify(jerseyNumber, name){
              if(this.jerseyNumber !== jerseyNumber || this.name !== name ) return;
              this.bercelonaPlayer =  true;
          }
      }
  };
  
  bercelona.playerRegistration(10, 'Lionel Messi', 'Argentina', 'Forward');
  // bercelona.playerIdentify(10, 'Lionel Messi');
  bercelona.playerIdentify(30, 'Lionel Messi');
  
  if (bercelona.bercelonaPlayer) {
      console.log(`Welcome to Mr. ${bercelona.name} not the Barcelona's world`);
  } else {
      console.log(`Sorry, You are not Bercelona player!`);
  }
  
  console.log(bercelona);
  ```


### Window
## In JavaScript, a "window" refers to the global object that represents the web browser's window or tab in which your JavaScript code is running. The window object provides access to various properties and methods that allow you to interact with and control the browser environment. Here are some key aspects of the window object:

### Global Scope
## Variables and functions declared in the global scope are attached to the window object. For example, if you declare a variable like var x = 10; at the top level of your JavaScript code, you can access it as window.x or simply x.
```js
var x = 10;
console.log(window.x) // the result will be same
console.log(x) // the result will be same
```


