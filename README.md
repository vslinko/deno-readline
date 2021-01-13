# deno-readline

Readline implementation for https://deno.land/.

# Usage

```ts
import { readline } from "https://deno.land/x/readline@v1.1.0/mod.ts";

const f = await Deno.open("./example.ts");
for await (const line of readline(f)) {
  console.log(`line: ${new TextDecoder().decode(line)}`);
}
f.close();
```
