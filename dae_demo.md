---
marp: true
theme: dae
---
<!-- _class: title-slide-v2017   -->

# Title slide 2017

## WEEK 2

<!-- footer: Demo presentation -->

---
<!-- _class: title-slide   -->

# Title slide 2019

## WEEK 2

<!-- footer: Demo presentation -->

---
<!-- _class: title-slide-v2023   -->

# Title slide 2023

## WEEK 2

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