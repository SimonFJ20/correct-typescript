# Lidt om types

I Typescript skal du bruge typer ('types' formelt), såsom `number`, `string`, `boolean`, osv.

## Funktioner

Når du skal skrive funktioner, skal du fortælle hvilke typer du forventer at modtage gennem parametrene (dem i parenteserne), og hvad du forventer at returnere.

```ts
function add(left: number, right: number): number {
    return left + right;
}
```

