---
layout: post
title: Understanding Javascript variables - Var | let | const
cover: https://images.unsplash.com/photo-1503437313881-503a91226402?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1189&q=80
---

![Do what is great](https://images.unsplash.com/photo-1503437313881-503a91226402?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1189&q=80)


Welcome back super programmer, Today i will be touching very basic topic but yet will be way much useful to you if you are writing javascript for your stack.

Based on usage, scope and availablity, a programming language may offer various ways to declear variables, and using those variables randomly & without understanding fully might cause problem, headec while debugging code and sometimes just you might have to replace one type with another without knowing why you are doing that.

So lets clear these three ways of variable in your javascript today.


## var - Global as windows property & Mutable
Very Common type of variable we decleare and since its quite relatable with name, everyone used this and looks cool.

```
var base_url = 'http://thedijje.com';
```

Seems all right, yeah.. Let me tell you how far `var` is available in your client.

Open devtool/Browser console, and type 
```
window
```
& hit enter, you will see detail of window object which have all sorts of properties which a browser window might have.

and all these properties can be accessed using `window.pro_name`.

Okay so why i am here, because if you decleare `var`, this variable will become property of `window` object and will be available as `window.your-variable`.

For example
```
var base_url;
// http://thedijje.com
```

& 
```
window.base_url;
// http://thedijje.com
```

![var as window object]({{ site.baseurl }}/images/posts/2020/05/29/var-scope-javascript.png)

**Usecase** 
If you want to make your variable available globally, and you also open for any conflict/or any other process might replace value of that variable, or even you may want to update it later on, `var` is good choice.

If you want variable to be available globally but do not want to be changes, var is definately not good option.

Let's get to `const` for the same reason

## const - Global & Immutable
As name suggest, its constant, you can use this way of declearing variable when you want to keep your variable available globally but do not want any other code/process/method/function to alter this.

_For example_
```
const base_url = 'https://thedijje.com';
```
is something which i will be using in entire application as `base_url` and this will not be changed.

So declearing it as `var` will be very much risky as if any process assign any other value to `base_url`, it will affact entire usage of this variable after that.

but if i have initiated it as `const`, its value will stay as it is for entire scope of application and will be exactly what i want.

and imagine if you ever decleare it in any sort of loop 😄, on very next iteration its gona break. so whats for loop? 
`let`'s got ahead🤘

## let - available only in given block
So ever used local variables like i for incrementing purpose? Have you decleared  it as `var`, now do you understand, for very localised use of `i` say, we kept modifying windows object, not anymore.

We have `let`, a very short lived variable, it's scope is limited to its code block, either in if-statement or in loop or in function.

Its really good to use let in all sorts of such places where only local manipulation is required, rest memory gets free as soon as processing is completed.

## Bottom line & take away
* Use `var` only if you want your variable to be accessable globally in application, and can also be used using `window.var_name`.
* `var` is mutable, so its value can be altered by any other line of code.
* `const` is also global but immutable variable.
* `let` is very short lived variable, scope is limited to block level or function level only.


I hope i could made this clear to you, wish you better being coder, stay awesome, keep coding.
