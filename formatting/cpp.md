# cpp formatting
### conventions
- variables `camelCase`
- func `camelCase`
- class `PascalCase`
- param `pPascalCase`
- template param `T, U, V`
- template param (named) `PascalCaseOneWord`
- template param (impl) `ImplT`
- namespace `PascalCase`
- namespace (apis) `nocaseoneword`
- constants `UPPER_SNAKE_CASE`
- macros `UPPER_SNAKE_CASE`
- private/protected member `m_camelCase`
- public member names `camelCase`

### special vars
- indexes `i, j, k`
- iterators `it`
- retaining `ret`


### scope on same line

```cpp
// ya
void uwu() {
    // ...
};
// no
void uwu() 
{
    // ...
};
```

### no one liners (other than return)

```cpp
// ya
if (true) {
    uwu();
}
// no
if (true) uwu();
```

other thing

```cpp
// ya
struct UwU {
    bool rawr;
};
// no
struct UwU { bool rawr; };
```

for empty structs its fine tho

```cpp
struct UwU {};
```

### ptrs/references

```cpp
// ya
int* uwu = nulllptr;
// no
int *uwu = nullptr;
```

### const

```cpp
// ya
const int uwu = 1;
// no
int const uwu = 1;
```

### 2 line constructors

```cpp
// ya
UwU()
    : rawr(true) {}
// no
UwU() : rawr(true) {}
```

even for defaults

```cpp
// ya
UwU()
    = default;
// no
UwU() = default;
```

also

```cpp
// ya
UwU()
    : rawr(true) 
{
    thing();
}
// no
UwU() 
    : rawr(true) {
    thing();
}
```

### format switch statements like this
```cpp
// ya
switch (true) {
    case 0: {
        uwu();

        thing();
    break; }
    case 1: [[__fallthrough__]];
    case 2: {
        uwu();

        otherThing();
    break; }
}
// no
switch (true) {
    case 0:
        uwu();
        thing();
        break;
    case 1:
    case 2: {
        uwu();

        otherThing();

        break; 
    }
}
```

if the switch cases r rly small u can js do this tho (only if the entire switch is like this tho js keep it consistent)

```cpp
switch (true) {
    case 0: uwu(); break;
    case 1: thing(); break;
    case 2: otherThing() break;
}
```

### seperate different "things" as much as possible

```cpp
// ya
SillyNode* create() {
    auto ret = new SillyNode;

    if (!ret->init()) {
        delete ret;

        return nullptr;
    }

    ret->autorelease();

    return ret;
}
// no
SillyNode* create() {
    auto ret = new SillyNode;
    if (!ret->init()) {
        delete ret;
        return nullptr;
    }
    ret->autorelease();
    return ret;
}
```

prolly better example

```cpp
// ya
void uwu() {
    auto node = CCNode::create();
    node->setPosition(CCPointZero);
    EditorUI::get()->addChild(node);

    if (true) {
        node->setScale(0.5f);

        reinterpret_cast<SillyEditorUI*>(EditorUI::get())->thing();
    }
}
// no
void uwu() {
    auto node = CCNode::create();
    node->setPosition(CCPointZero);
    EditorUI::get()->addChild(node);
    if (true) {
        node->setScale(0.5f);
        reinterpret_cast<SillyEditorUI*>(EditorUI::get())->thing();
    }
}

```

### variable initialization
for primitive types:

```cpp
// ya
constexpr float UWU = 1.0f;
// no
constexpr float UWU{1.0f};
```

default constructing

```cpp
// ya
constexpr float UWU = 0.0f;
// no
constexpr float UWU{};
```

for non-primitive types:

```cpp
// ya
constexpr std::string UWU{"rawr"};
// no
constexpr std::string UWU = "rawr";
```

### if args list is too long then wrap it like this

```cpp
// ya
uwu(
    REALLY_REALLY_REALLY_REALLY_REALLY_LONG_CONSTANT, 
    OTHER_REALLY_REALLY_REALLY_REALLY_REALLY_LONG_CONSTANT
);
// no
uwu(REALLY_REALLY_REALLY_REALLY_REALLY_LONG_CONSTANT, 
    OTHER_REALLY_REALLY_REALLY_REALLY_REALLY_LONG_CONSTANT);
```

### lambdas 

```cpp
// ya
auto uwu = [this] () {
    thing();
};
// no
auto uwu = [this](){
    thing();
};
```

### end float literals with .0f

```cpp
// ya
constexpr float UWU = 1.0f
// no
constexpr float UWU = 1.f
// no
constexpr float UWU = 1.10f
```

### specify constants types (anything else can be auto idrc)

```cpp
// ya
constexpr float UWU = 1.0f
// no
constexpr auto UWU = 1.0f
```

### generally dont use magic numbers but if you do and its in arithmetic just let them be promoted to float no literal necessary

```cpp
float rawr();

// ya
rawr() / 2;
// no
rawr() / 2.0f;
```

### dont do the dumb thing ai does and align stuff in maps

```cpp
// ya
constexpr std::array<float, 6> uwu{
    1.0f, 1.0f
    1.1111f, 1.0f
    1.11f, 1.0f
}
// no 
constexpr std::array<float, 6> uwu{
    1.0f,    1.0f
    1.1111f, 1.0f
    1.11f,   1.0f
}
```