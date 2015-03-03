# The Ruby Room Currently Choosed Options

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
