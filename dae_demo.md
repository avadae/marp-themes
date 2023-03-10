---
marp: true
theme: dae
---
<!-- _class: title-slide   -->

# Title slide 2019

<!-- footer: Demo presentation -->

---
<!-- _class: title-slide-v2023   -->

# Title slide 2023

<!-- footer: Demo presentation -->

---
<!-- header: A nice header for your slide -->
<!-- paginate: true -->

# A title

Lorem ipsum dolor sit amet, **consectetur adipiscing elit**, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

- bullet
- bullet

A centered image :

![center drop-shadow:0,0,10px,#000](https://gameprogrammingpatterns.com/images/data-locality-cache-line.png)

<!-- Some comments, these will be present in the pptx too if you export this. -->
---
![bg right:50% width:70% drop-shadow:0,0,10px,#000](https://en.wikichip.org/w/images/thumb/8/86/haswell_%28octa-core%29_die_shot.png/650px-haswell_%28octa-core%29_die_shot.png)

# Slide with an image
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

---
# Two column layout

<div class="columns"><div>

Some code blocks

```cpp
int main()
{
    int total = 0;
    for(int i = 0; i < 10; ++i)
    {
        total += i;
    }
    return 0;
}
```

</div><div>

```
main:
  push rbp
  mov rbp, rsp
  mov DWORD PTR [rbp-4], 0
  mov DWORD PTR [rbp-8], 0
  jmp .L2
.L3:
  mov eax, DWORD PTR [rbp-8]
  add DWORD PTR [rbp-4], eax
  add DWORD PTR [rbp-8], 1
.L2:
  cmp DWORD PTR [rbp-8], 9
  jle .L3
  mov eax, 0
  pop rbp
  ret
```

</div></div>

<!--
rpb = framepointer
eax = register
-->
