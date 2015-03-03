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

* Multi-line method chaining using trailing dot:

  * **(Option B)** When continuing a chained method invocation on another line,
    include the `.` on the first line to indicate that the
    expression continues.

    ```Ruby
    # bad - need to read ahead to the second line to know that the chain continues
    one.two.three
      .four

    # good - it's immediately clear that the expression continues beyond the first line
    one.two.three.
      four
    ```
