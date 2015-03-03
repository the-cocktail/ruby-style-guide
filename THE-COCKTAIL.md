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

* Symbolic operators *&&/||* peferred, but english operarors *and/or* accepted for control flow.

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

In boolean expressions parenthesis are free and always help. Thanks!

