---
marp: true
theme: dae_black
class: invert
---
<!-- _class: title-slide -->

# Beyond execution

## WEEK 01

<!-- footer: "Game Development / Software Engineering / 2024-2025" -->

---

<!-- header: Beyond execution -->
<!-- paginate: true -->

# In this lecture

<center>

Understanding how **programming languages** differ beyond just syntax

Exploring the (c++) **build process** from source code to executable

Comparing **platforms** and their (default) **compilers**

</center>

---

# Programming languages

There are many programming/scripting languages beyond C++, each with their specific syntax, strengths and common use cases

A Programming/Scripting Language is defined by a Syntax

- Set of **valid instructions**
- Set of **keywords**
- Set of **valid identifiers**: variable names, class names, namespace names
- **Punctuations**: braces, brackets, semi columns, ...
Code written in a programming language is readable by humans

A <scope style="color: #70ad47">Programming Language</scope> is typically compiled (C++, C#, Java, ...)
A <scope style="color: #70ad47">Scripting Language</scope> can be directly executed typically by an interpreter (Python, Lua, Basic, ...)

---

# Programming languages

<center>

There are many programming/scripting languages beyond C++, 
each with their specific syntax, strengths and common use cases

<table style="font-size: 21px;">
  <tr>
    <th>Language</th>
    <th>Managed/Unmanaged</th>
    <th>Compiled/Interpreted</th>
    <th>Typing</th>
    <th>Common Use Cases</th>
  </tr>
  <tr>
    <td style="color: #ffc000;"> C++</td>
    <td>Unmanaged</td>
    <td>Compiled</td>
    <td>Strong</td>
    <td>Game development, systems programming, embedded systems, high-performance application</td>
  </tr>
  <tr>
    <td style="color: #ffc000;">Python</td>
    <td>Managed</td>
    <td>Interpreted</td>
    <td>Dynamic</td>
    <td>Scripting, Data science, web development, automation, machine learning</td>
  </tr>
  <tr>
    <td style="color: #ffc000;">C#</td>
    <td>Managed</td>
    <td>Compiled to MSIL, JIT (Just-In-Time)</td>
    <td>Strong</td>
    <td>Windows applications, game development (Unity), web applications (ASP.NET)</td>
  </tr>
  <tr>
    <td style="color: #ffc000;">Java</td>
    <td>Managed</td>
    <td>Compiled to Bytecode, JIT</td>
    <td>Strong</td>
    <td>Enterprise applications, Android development, large-scale web services</td>
  </tr>
  <tr>
    <td style="color: #ffc000;">Rust</td>
    <td>Unmanaged</td>
    <td>Compiled</td>
    <td>Strong</td>
    <td>Systems programming, embedded systems, performance-critical applications</td>
  </tr>
  <tr>
    <td style="color: #ffc000;">Lua</td>
    <td>Managed</td>
    <td>Interpreted</td>
    <td>Dynamic</td>
    <td>Game scripting, embedded applications, lightweight scripting</td>
  </tr>
  <tr>
    <td style="color: #ffc000;">Go</td>
    <td>Hybrid</td>
    <td>Compiled</td>
    <td>Strong</td>
    <td>Cloud infrastructure, web servers, concurrency-heavy application</td>
  </tr>
  <tr>
    <td style="color: #ffc000;">...</td>
    <td>...</td>
    <td>...</td>
    <td>...</td>
    <td>...</td>
  </tr>
</table>
</center>

---

# Managed or Unmanaged?

<style scoped>section{font-size:22px;}</style>

**Managed** Languages:
- **Memory management is handled automatically** by a runtime environment (e.g., garbage collection)
Examples: C#, Java, Python
- <scope style="color: #70ad47">Advantages</scope>
  - Easier development since memory is managed for you
  - Lower risk of memory leaks and pointer-related bugs
- <scope style="color: #c00000">Disadvantages</scope>
  - Slower in some cases due to garbage collection overhead
  - Less control over memory usage and performance optimization

**Unmanaged** Languages:
- Developers **manually manage memory** (e.g., using malloc/free in C/C++)
Examples: C++, Rust
- <scope style="color: #70ad47">Advantages</scope>
  - Greater control over memory, which can lead to more optimized and high-performance code
  - No garbage collection overhead, making it ideal for performance-critical applications
- <scope style="color: #c00000">Disadvantages</scope>
  - Higher risk of memory leaks and bugs (e.g., dangling pointers, buffer overflows)
  - More complex and error-prone due to manual memory management

**Hybrid**
- Combines automatic memory management with low-level control, allowing for some flexibility between the two approaches
Examples: Go


---

# A title

Lorem ipsum dolor sit amet, **consectetur adipiscing elit**, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

- bullet
- bullet

A centered image :

![center drop-shadow:0,0,10px,#000](https://gameprogrammingpatterns.com/images/data-locality-cache-line.png)

<sub>https://baptiste-wicht.com/posts/2017/09/cpp11-performance-tip-when-to-use-std-pow.html</sub>


<!-- Some comments, these will be present in the pptx too if you export this. -->
---
![bg right:50% width:70% drop-shadow:0,0,10px,#000](https://en.wikichip.org/w/images/thumb/8/86/haswell_%28octa-core%29_die_shot.png/650px-haswell_%28octa-core%29_die_shot.png)

# Slide **with** an image
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

---
# <!--fit --> Two column layout and a title that is so long it exceeds the width of the slide

<div class="columns"><div>

Some code blocks

<style scoped> code { font-size: 35px; } </style>

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

---
# SVG Test

![center drop-shadow:0,0,10px,#000](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/Bananas.svg/1024px-Bananas.svg.png)

--- 

# Class test

On what objects do we call this Update method?

```cpp
namespace dae
{
  class Texture2D;
  class GameObject 
  {
    Transform m_transform{};
    std::string m_name{};
    std::shared_ptr<Texture2D> m_texture{};
  public:
    virtual void Update();
    virtual void Render() const;

    void SetTexture(const std::string& filename);
    void SetPosition(float x, float y);

    GameObject() = default;
    virtual ~GameObject();
    GameObject(const GameObject& other) = delete;
    GameObject(GameObject&& other) = delete;
    GameObject& operator=(const GameObject& other) = delete;
    GameObject& operator=(GameObject&& other) = delete;
  };
}
```