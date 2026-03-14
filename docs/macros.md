---
eleventyNavigation:
    key: Macros
    order: 5
update: 2023-11-18
version: VisiData 3.0
---

# Macros

Macros allow you to bind a series of commands to a key and then replay those commands within a session by using that keystroke.

The basic usage is:
1. Press `m` (macro-record) to begin recording the macro.
2. Go through the commands you wish to record.
3. Then type `m` again to complete the recording, and prompt for the keystroke or longname to bind it to.

The macro will then be executed every time the provided keystroke is used. Note: the Alt+keys and the function keys are left unbound; overriding other keys may conflict with existing bindings, now or in the future.

Executing a macro will the series of commands starting on the current row and column on the current sheet.

## Keystroke Binding

When binding a macro to a longname (like `happy-time`), you will also be prompted for an optional keystroke shortcut.
Type a keystroke (like `Alt+s`) and press Enter to bind it, or just press Enter to skip.

The keystroke is shown on the Macros Sheet and can be edited there.

## Input Parameters

Macro command inputs can use `{param}` or `{param=default}` placeholders in the `input` or `col` fields.
When a parameterized macro is run, VisiData prompts for parameter values before executing.

For example, recording a macro that adds a column with `=name + " suffix"`, then editing the input to `{col} + " {text=suffix}"`, will prompt for `col` and `text` values each time the macro runs.

# The Macros Sheet

Use `gm` (`macro-sheet`) to open an index of existing macros.

Macros can be marked for deletion (with `d`). Changes can then be committed with `z Ctrl+S`.

The `helpstr` column can be edited to add a description for each macro. This description will show up in the command palette and the Commands Sheet. Save changes with `z Ctrl+S`.

The `keystroke` column can be edited to bind or change a keystroke shortcut for a macro.

`Enter` will open the macro in the current row, and you can view the series of commands composing it.

