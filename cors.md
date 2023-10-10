# CORS in ExpressJS


**Step 1 :** *To install cors dependency*
```
npm i cors
```
**Step 2 :** *Cors snippets*

```js

const whitelist  = ['https://www.google.com','http://127.0.0.1:5500','http://localhost:5000/'];

const corsOptions = {
    origin: (origin, callback) => {
        if(whitelist.indexOf(origin) !== -1){
            callback(null, true);
        }
        else{
            callback(new Error('Not allowed by Cors'));
        }
    },
    optionSuccessStatus:200
}

// Third-party middleware

app.use(cors(corsOptions));
```