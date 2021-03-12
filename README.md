# json-credentials

Node.js module for storing/reading credentials data in/from JSON file

## How it works

In the example below the module will check if the json file exists.
If it does, the module will return the file data as an object.

If the file does not exist, the user will be prompted to specify the required fields(listed in array).
Then the provided data will be saved to a json file and returned to programm

## Installing

```
npm i json-credentials
```

## Usage

```
const { getCreds } = require('json-credentials');
(async () =>{
  const credsData = await getCreds(['login', 'password', 'secret']);
  console.log(`Login - ${credsData.login}, Password - ${credsData.password}, Secret - ${credsData.secret}`)
})();

```

optionally you can provide second argument wich a represents json file name

```
...
  const credsData = await getCreds(['login', 'password', 'secret'],'my-file-name.json');
...
```

by default, the name of the file that the module uses is credentials.json
