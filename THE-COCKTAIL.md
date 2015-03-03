# The Ruby Room Currently Choosed Options

The Cocktail's choosed options in the collaborative [Ruby Style Guide](https://github.com/bbatsov/ruby-style-guide).

## Source Code Layout

* No spaces after `{` or before `}`:

    ```Ruby
    # not so good
    { one: 1, two: 2 }
    "string#{ expr }"

    # good
    {one: 1, two: 2}
    "string#{expr}"
    ```

* Multi-line method chaining using leading dot:

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

* Symbolic operators *&&/||* preferred, but english operarors *and/or* accepted for control flow.

  ```Ruby
  # bad
  # boolean expression
  if some_condition and some_other_condition
    do_something
  end

  # control flow, no problem with english! :)
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


## Comments

* Internal projects' comments can be written in Spanish. However, they should be translated to English before becoming public.

## Naming

* If we need explicit access to the first object in a collection the name of its variable should begin with *first_* (for example, for the first *wadus* in the *wadus* collection we should use *first_wadus*).

* If for some reason we need to access more than the first element of a collection (to the second, for example), then their variable names should finish an underscore following by their position (in our previous example we'll have the *wadus_1* and *wadus_2* variables).

## Strings

* At The Cocktail we interpolate code **without** space after { and before } (like **#{this}** and not like **#{ this }**).

* String literal quoting with single-quoted when no interpolation is needed:

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

