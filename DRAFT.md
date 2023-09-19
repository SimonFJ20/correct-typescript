
# Correct Typscript

**Very oppinionated.**

## Basics

### Naming

Type identifier are `UpperPascalCase`. Value identifier are `lowerCamelCase`.

Type identifiers include:
- Types aliases
- Classes
- Interfaces
- Enums
- Enum members (enum members are types)

Value identifiers include:
- Variables
- Constants
- Function parameters
- Object fields
- Static class fields
- Functions
- Methods

Do not use `SCREAMING_UPPER_SNAKE_CASE`.

Function names explain what the function does, or what values it returns, eg:
```ts
// this one may have side effects
function formatCode(codeText: string): string {}

// no side effects
function formattedCode(codeText: string): string {}
```

Class names are nouns, eg:
```ts
class CodeFormatter {}
```

Variable names explain the contained value, eg:
```ts
let indentWidth = 0;
indentWidth += amountOfSpaces;

let isIndented = false;
if (indentWith > 0) {
    isIndented = true;
}
```

### Formatting

Start braces `{` are on the same line.

Always use braces `{` and `}`, on single line `if`, `while` and `for`.

Always use semicolon `;`.

Function parameter-lists, arrays and objects are formatted like this:
```ts
[1, 2, 3]
[
    1,
    2,
    3,
]
```

Use tabs, 4-spaces or 2-spaces consistently.

Indent code properly.

### Comments

Not there, unless really really necessary.

Not valid:
```ts
// 5 is the starting number of students
let i = 5;

scanQueue.addScan(scanData);
// sends messages to server
scanQueue.flush();

// test intString is a valid integer string
if (!/^0|[1-9][0-9]*$/.test(intString)) {}
```

Valid:
```ts
const startingNumberOfStudents = 5;
let i = startingNumberOfStudents;

sendScansToServerAndFlush(scanQueue, scanData);

const validIntegerPattern = /^0|[1-9][0-9]*$/.test(intString);
function isValidInteger(text: string): boolean {
    return validIntegerPattern.test(text);
}

if (!isValidInteger(intString)) {}

function hypotheticallySpeedUpTheNextFewAllocations(): number {
    // the hack works by forcing a collection cycle,
    // which will make v8 mmap a new memory pace, which might speed up
    // the next few allocations, due to a caching techinality:
    // https://stackoverflow.com/questions/12345678/hypothetically-speed-up-allocations
    // it works by ...
    return new Array(1 << 31)
        .fill(Math.random())
        .map((_, i) => i)
        .reduce((acc, v) => acc * v % 5, 0);
}
```


