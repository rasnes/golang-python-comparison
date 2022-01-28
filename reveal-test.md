---
theme: "white"
highlightTheme: "monokai"
---

<style>
#left {
	margin: 10px 0 15px 20px;
	text-align: left;
	float: left;
	z-index:-10;
	width:48%;
	font-size: 0.75em;
	line-height: 1.2; 
}

#right {
	margin: 10px 0 15px 0;
	float: right;
	text-align: left;
	z-index:-10;
	width:48%;
	font-size: 0.75em;
	line-height: 1.2; 
}

#left-most {
	margin: 10px 0 15px 20px;
	text-align: left;
	float: left;
	z-index:-10;
	width:68%;
	font-size: 0.85em;
	line-height: 1.2; 
}

#right-less {
	margin: 10px 0 15px 0;
	float: right;
	text-align: left;
	z-index:-10;
	width:28%;
	font-size: 0.85em;
	line-height: 1.2; 
}

#left-less {
	margin: 10px 0 15px 20px;
	text-align: left;
	float: left;
	z-index:-10;
	width:43%;
	font-size: 0.85em;
	line-height: 1.2; 
}

#right-less {
	margin: 10px 0 15px 0;
	float: right;
	text-align: left;
	z-index:-10;
	width: 53%;
	font-size: 0.85em;
	line-height: 1.2; 
}



</style>

## Contents

- Go: concurrency, OOP (interface), strongly typed, speed, runtime, history, deliberately boring, few keywords, somewhat verbose (example no ternary operator, for loop), imperative but with first-class function support. Ambition: get developers unfamiliar with the language up to speed quickly, easy to read others code and easier to maintain large codebases, go fmt. fast compiler. Standard library: testing, net/http
- Python: GIL, age of language (compare to C, C++, Java, Rust), Zen of Python: There should be only way of doing it..
- Go controversial design decisions: error handling, no generics (until February!)
- Concurrency vs Parallelism
- Go arguments: embraced by CoopX, great backend language; Kubernetes, Docker
- Go Python interop, using C bindings.
- Go vs Rust - modern languages compared
- Go cons: Data Science tooling, no REPL
- References: Learning Go,

---

## Why learn `Go`?

<div id="left-most">

- Great for backend development
- Maintained by Google, great support in Google Cloud Platform
- `CoopX` preferred language <br> (together with `Python`)
- Powerful concurrency tools
- Relatively easy to learn

</div>

<div id="right-less">

![](images/gopher.png)

</div>

---

# `Go` selling points 

- speed (compare with Python)
- concurrency (compare with Python)
	- Concurrency vs Parallellism
- Ambition: get developers unfamiliar with the language up to speed quickly, easy to read others code and easier to maintain large codebases, go fmt. fast compiler.

--

## Ambitions / Design goals

- Onboard new developers quickly
	- Imperative (familiar to most)
	- Small language
	- Easy-to-read syntax
- 


--

## Static type checking

<div id="left">

`python` is duck-typed by nature, but `mypy` can help.

```python
class Logic:
		def process(self, data):
				# business logic

def program(logic):
	  # get data from somewhere
		logic.process(data)

lgc = Logic()
program(lgc)
```
</div>

<div id="right">

`go` uses `interface`s instead of `class`es. No inheritance.

```go
type Logic interface {
	Process(data string)
}
func program(l Logic) {
	// get data from somewhere
	l.process(data)
}
//Any type implementing a Process
//method complies with Logic interface
type lgc struct {}
// Implement method Process on lgc
func (lg log) Process(data string) {
		// business logic
}

// Compile time error if not `lgc`
// implements the Process method!
program(lgc)
```

</div>

--

## Compile time

<div id="left">

Blazingly fast compiler

Compared to "all" other compiled languages, like `Java`, `C`, `C++`, `Rust`

Enables rapid prototyping and development

</div>

<div id="right">

![](images/compiling.png)

</div>

--

## `Go` is fast

Comparable to `Java` and `C`.

No need for "glue code", to faster languages.

"Pure" `Python` is slow in comparison, but calling `C`/`C++` code with e.g. `numpy` or `pyTorch` gives comparable speeds.

---

## `Go` vs `Python`

Why and when would you consider using `Go` instead of `Python`?

--

## `Go` vs `Python` - concurrency



---

#### Example of two-column layout with syntax highlighting

Some text. Strange that bullets get "caught" in the divs.

<div id="left">

`python:`

```python
def bar(a, b):
    return a + b
```

- list
- yes

</div>

<div id="right">

`go:`

```go
func foo(a, b int) int {
  return a + b
}
```

1. ordered
2. indeed

</div>

---


## Themes

reveal.js comes with a few themes built in:
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/black.css'); return false;">Black (default)</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/white.css'); return false;">White</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/league.css'); return false;">League</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/sky.css'); return false;">Sky</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/beige.css'); return false;">Beige</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/simple.css'); return false;">Simple</a> <br>
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/serif.css'); return false;">Serif</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/blood.css'); return false;">Blood</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/night.css'); return false;">Night</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/moon.css'); return false;">Moon</a> -
<a href="#" onclick="document.getElementById('theme').setAttribute('href','libs/reveal.js/3.8.0/css/theme/solarized.css'); return false;">Solarized</a>


---

Is it gone now?

note: some hnotes here. How can I see them?

