FAQ
===

**What are all those OCOCOCO or ODODODO that appear on the screen?**

     These are the terminal sequences that MisTTY sends to a program
     to move the cursor left or right. If you see these printed on the
     terminal, it means that the program that's currently controlling
     the terminal doesn't support these.

     In such situation, you can:

     - Only type self-inserting characters and :kbd:`DEL`.

     - Press :kbd:`C-c C-q` or :kbd:`M-x mistty-send-key-sequence` to
       send what you type directly to the terminal until you turn it
       off with :kbd:`C-g`.

     - Write a regexp that identifies the situation and add it to
       :kbd:`M-x customize-option mistty-forbid-edit-regexps`.

     See the section :ref:`term-vs-scroll` for more details.

**Why is the cursor jumping around when I move it?**

    MisTTY jumps over spaces which just "aren't there", such as the
    spaces between the command and the right prompt, spaces added by
    :program:`fish` for indentation in multi-line prompts.

    If it doesn't work with your shell or setup, or if you find it
    confusing, type :kbd:`M-x customize-option
    mistty-skip-empty-spaces` to turn it off.
     
**What's with the purple line?**

    This line indicates the region of the buffer that works as a
    terminal, meaning that it is not fully editable and that some
    shortcuts, such as :kbd:`TAB` are sent directly to the program
    controlling the terminal.

    This is covered in depth in the section :ref:`term-vs-scroll`.

    If you just don't want to see that line, turn it off with
    :kbd:`M-x customize-option mistty-fring-enabled`
