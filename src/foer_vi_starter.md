# Før vi starter

Jeg forventer du kan programmere i mindst et af følgende sprog: (C#, Python, Javascript). Dvs. du har forståelse for samtlige af følgende koncepter.

Hvis du ikke forstår hvad der foregår, spørg nogen eller [Google](https://duckduckgo.com) det.

## Værdier og variabler

```ts
let my_variable: number = 5;

my_variable = 2;

const myConstant = false;

const myString: string = "hello world";

const myArray1: number[] = [ 1, 2, 3 ];

const myArray2 = [ 1, "foo", true, "bar" ];

let myValue = myArray2[0];

my_value = myArray1[1];

const my_object = {
    foo: 1,
    "bar": true,
};
```

## If-statements

```ts
if (myVariable == 5) {
    console.log("five");    
} else {
    console.log("not five");    
}

if (myString != "hello world")
    return "wasn't \"hello world\"";
```

## Loops

```ts
const values = [1, 2, 3, 4]

for (const value of values)
    console.log(value);

for (let i = 0; i < values.length; i++) {
    const value = values[i];
    console.log(`values[${i}] == ${value}`);
}

while (we.areRunning()) {
    we.avoidFalling();
}
```

## Funktioner

```ts
function myFunctionThatReturns(): number {
    return 4;
}

function myFunctionThatTakes2Parameters(a: number, b: number): number {
    return a + b;
}

function myFunctionThatDoesntReturnAnything(): void {
    console.log("hello world");
}
```

## Klasser

```ts
class Counter {
    private counter = 0;
    
    public count() {
        this.counter += 1;
    }

    public result(): number {
        return this.counter;
    }
}

let myCounter = new Counter();
myCounter.count();
myCounter.count();
myCounter.count();
console.log(myCounter.result()) // maybe 5 idk
```

Alan, tryk.


