# protoPractice

- [ProtoType](#ProtoType)

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
