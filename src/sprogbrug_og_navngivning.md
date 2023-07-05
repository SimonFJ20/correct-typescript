# Sprogbrug og navngivning

## Sprog

Du skal skrive din kode på engelsk. Det gælder navne på variaber, filer, funktioner med mere. **Dette gælder også kommentarer**.

### Eksempler

```ts
// this is incorrect, 'minVariabel' is a name consisting of danish words, danish != english
let minVariabel = "123";

// this is incorrect, the comment should be in english
// dette er korrekt, da strengen '"hej verden"' er en værdi og ikke et navn
let myVariable = "hej værden";

// guess whether this is correct or not
class MinKlasse {}
``` 

## Ungarsk notation

Du skal bruge Typescript, dvs. du skal adskille variablers navne fra deres typer.

```ts
// i don't care that this is a number, i care that it's a count of some sort.
let countNumber: number = 0;

// i can see perfectly fine that EventClass is a class
class EventClass {}
```

Prefix-typer på variabel- og typenavne er ligegyldig og redundant information. Fraværet er bedre.


## -Handler, -Manager, -State, -Controller

Du skal skrive kode der representere din problem, dvs. hvis du har en klasse der representere dine brugere, så skal den hedde `Users` og ikke `UserHandler`. Dette er gældende fordi du skal skrive objekt orenteret kode, dvs. du skal modellere din problem-space i din kode, istedet for at lave kode der *håndterer* din problem-space.

```ts
type User = {
    username: string,
    password: string,
}

class Users {
    
    public async createUser(
        username: string,
        password: string,
    ): Promise<Result<User, UsersError>> {
        /* ... */
    }

}
```

Postfix-titler på klassenavne misrepresenterer klassens rolle. Fraværet er bedre.

## Hvad er et godt navn

### 

