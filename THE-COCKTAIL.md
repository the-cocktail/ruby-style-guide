# The Ruby Room Currently Choosed Options

The Cocktail's choosed options in the collaborative
  [Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide).

## Source Code Layout

* No spaces after `{` or before `}`
  ([link](https://github.com/bbatsov/ruby-style-guide#spaces-operators)):

    ```Ruby
    # not so good
    { one: 1, two: 2 }
    "string#{ expr }"

    # good
    {one: 1, two: 2}
    "string#{expr}"
    ```

* Multi-line method chaining using leading dot
  ([link](https://github.com/bbatsov/ruby-style-guide#consistent-multi-line-chains)):

  * **(Option A)** When continuing a chained method invocation on
    another line keep the `.` on the second line.

    ```Ruby
    # bad - need to consult first line to understand second line
    one.two.three.
      four

    # good - it's immediately clear what's going on the second line
    one.two.three
      .four
    ```

## Syntax

* Symbolic operators *&&/||* preferred, but english operarors *and/or* accepted
  for control flow ([link](https://github.com/bbatsov/ruby-style-guide#no-and-or-or)).

  ```Ruby
  # bad
  # boolean expression
  if some_condition and some_other_condition
    do_something
  end

  # control flow: no problem with english operators! :)
  document.saved? or document.save!

  # good
  # boolean expression
  if some_condition && some_other_condition
    do_something
  end

  # control flow
  document.saved? || document.save!
  ```

In complex boolean expressions parenthesis are free and always help. Thanks!
  ([Advi Grimm 5min. screencast about the subject](http://devblog.avdi.org/2014/08/26/how-to-use-rubys-english-andor-operators-without-going-nuts/)).


## Comments

* Internal projects' comments can be written in Spanish. However, they should
  be translated to English before becoming public.

## Naming

* If we need explicit access to the first object in a collection the name of
  its variable should begin with *first_* (for example, for the first *wadus*
  in the *wadus* collection we should use *first_wadus*).

* If for some reason we need to access more than the first element of a
  collection (to the second, for example), then their variable names should
  finish an underscore following by their position (in our previous example
  we'll have the *wadus_1* and *wadus_2* variables).

## Strings

* At The Cocktail we interpolate code **without** space after { and before }
  (like **#{this}** and not like **#{ this }**, which follows the style rule of
  not spaces after { and before }).

* String literal quoting with single-quoted when no interpolation is needed
  ([link](https://github.com/bbatsov/ruby-style-guide#consistent-string-literals)):

  * **(Option A)** Prefer single-quoted strings when you don't need
    string interpolation or special symbols such as `\t`, `\n`, `'`,
    etc.

    ```Ruby
    # bad
    name = "Bozhidar"

    # good
    name = 'Bozhidar'
    ```

* Percent literal if both interpolation and double-quotes are neeed:

    ```Ruby
    greeting = %(Hello "#{name}")
    ```

* Remember to use String#<< instead of String#+ when you need to construct
  large strings
  ([link](https://github.com/bbatsov/ruby-style-guide#concat-strings)).


## Regular Expressions

First of all let's repeat this section's Jamie Zawinski's quote:

> Some people, when confronted with a problem, think
> "I know, I'll use regular expressions." Now they have two problems.<br/>

That said...

* This (almost final) section about RegExps deserves to be read: 
  [link](https://github.com/bbatsov/ruby-style-guide#no-regexp-for-plaintext).

* If you don't understand something, please ask us!!!

* If you need them, the creator of this style guide (Bozhidar Batsov) also
  wrote [a nice post about how sub/gsub replacements can be used with a block](http://batsov.com/articles/2013/08/30/using-gsub-with-a-block).


## Misc

Favourite ones:

* Avoid methods longer than 10 LOC.

* Avoid parameter lists longer than three or four parameters.

* Use common sense. :)

