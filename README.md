
Just some fun in inventing some crazy language.

Glitch: a programming language with symbols. Because C wasn't cryptic enough.
It's basically C with simple reserved keyword substitution.
Maybe more to come, for now just replacing reserved keywords and some functions.

Samples, of course you need to be able to see UTF-8!

Switch / If / Goto
```
∑ <stdio.h>

⁑ ⚐() {
  ⁑ v = 3;
  ◉ (v) {
    ◔ 1:
      → end;
    ◔ 2:
      ← 5;
    ◔ 3:
      ⇉("It's a three!!\n");
      ↕;
    ◕:
      ⇉("No idea??\n");
  }
end:
  △(v*4 == 8)
    ⇉("It's two.\n");
  ▽ △(v == -1)
    ⇉("It's -1.\n");
  ▽
    ⇉("It's any.\n");
  ← 0;
}
```

Finding a prime
```
∑ <stdio.h>

♢ ♧ ⚟ ⁑ two = 2;

⁑ ⚐() {
  ⁑ n, c;

  ⇉("Enter a number\n");
  ⇇("%d", &n);

  △(n == two) {
    ⇉("Prime number.\n");
  }▽{

    ☍(c = two; c <= n - 1; c++)
      △(n % c == 0) ↕;

    △(c != n)
      ⇉("Not prime.\n");
    ▽
      ⇉("Prime number.\n");
  }

  ← 0;
}
```

Struct / str / functions
```
∑ <stdio.h>
∑ <string.h>

☁ ⚘ {ONE, TWO} nums;

☁ ☀ {
  ☆ name[50];
  ♤ ⁑ num;
} stru;

⁑ ⚐() {
  stru g;

  ✄(g.name, "This is a string");
  ⁑ cmp = ⚇(g.name, "no?");
  g.num = 11;

  ⇉("Name: %s\n", g.name);
  ⇉("Number: %d\n", g.num);
  fn();

  ← 0;
}

◇ fn() {
  ‡ c = 1;
  ∞(c <= 10) {
    △(c <= 3) ↔;
    ⇉("%d ", c);
    c++;
  }
}

```

File functions
```
∑ <stdio.h>
∑ <stdlib.h>

⁑ ⚐() {
  FILE * fp;
  fp = ♪("file.txt", "w+");
  ⇝(fp, "%s %s %s %d", "We", "are", "in", 2012);

  ♫(fp);

  ← 0;
}
```

Why stopping there, reach to assembler...
```
⁑ ⚐() { ⁝(
  _main:
    mov esi, 1
    mov edi, 31
    end
) }
```

DEC / HEX / SYMBOL / keyword

types

  * 9671 25C7 ◇ void
  * 8224 2020 † float
  * 8225 2021 ‡ double
  * 8270 204E ⁎ short
  * 8273 2051 ⁑ int
  * 8277 2055 ⁕ long
  * 9734 2606 ☆ char
  * 9729 2601 ☁ typedef
  * 9728 2600 ☀ struct
  * 9880 2698 ⚘ enum

type modifiers

  * 9826 2662 ♢ static
  * 9831 2667 ♧ const
  * 9825 2661 ♡ signed
  * 9828 2664 ♤ unsigned
  * 9887 269F ⚟ volatile
  * 8623 21AF ↯ sizeof
  * 9633 25A1 □ auto
  * 9675 25CB ○ register
  * 9696 25E0 ◠ extern
  * 9697 25E1 ◡ union

control

  * 9651 25B3 △ if
  * 9661 25BD ▽ else
  * 9741 260D ☍ for
  * 8734 221E ∞ while
  * 8733 221D ∝ do
  * 9673 25C9 ◉ switch
  * 9684 25D4 ◔ case
  * 9685 25D5 ◕ default
  * 8594 2192 → goto
  * 8592 2190 ← return
  * 8596 2194 ↔ continue
  * 8597 2195 ↕ break
  * 9872 2690 ⚐ "main" used for the main function

some function replacement

  * 8647 21C7 ⇇ scanf
  * 8649 21C9 ⇉ printf
  * 8721 2211 ∑ #include ?
  * 9988 2704 ✄ strcpy
  * 9863 2687 ⚇ strcmp
  * 9834 266A ♪ fopen
  * 9835 266B ♫ fclose
  * 8668 21DC ⇜ fscanf
  * 8669 21DD ⇝ fprintf
  * 8285 205D ⁝ asm

Left to use:

  * 9960 26E8 ⛨ maybe new? not in C
  * 9904 26B0 ⚰ maybe delete? not in C
