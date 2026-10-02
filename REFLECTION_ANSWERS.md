# Reflection answers

1. **Why does the form need both HTML constraints and JavaScript?**
   HTML attributes (required, type, min/max, minlength, pattern) give quick built-in checks for most
   rules. JavaScript is needed for rules HTML cannot express, such as checking that the confirmation
   password matches, trimming the name, and deciding what message to show. Because the form uses
   `novalidate`, JavaScript also controls when validation runs.

2. **How do the array and loop work together to create the dropdown?**
   The `workshops` array stores the names. The `for...of` loop visits each name once; on each visit it
   creates a new `<option>`, sets its value and text, and appends it to the select. Adding a name to the
   array adds a dropdown choice automatically.

3. **Why use valueAsNumber rather than value when comparing seats?**
   `value` is always a string (e.g. "1"), while `valueAsNumber` is a real number. With a number,
   `seatCount === 1` works correctly with strict comparison and the seat count can be used reliably in
   calculations; a string would never be strictly equal to the number 1.

4. **Why must a custom validity message be cleared after a correction?**
   A non-empty `setCustomValidity` message keeps the field invalid. If it is not reset to an empty
   string, the field stays invalid even after the user fixes it, so the form could never be submitted.
