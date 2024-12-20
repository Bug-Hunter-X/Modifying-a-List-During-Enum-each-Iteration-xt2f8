# Modifying a List During Enum.each Iteration in Elixir

This example demonstrates a common mistake in Elixir: attempting to modify a list while iterating over it using `Enum.each`.  Because Elixir lists are immutable, modifications within the `Enum.each` function do not affect the original list.

The `bug.ex` file contains code that attempts to remove the element `3` from a list. The issue is that `List.delete` creates a *new* list, leaving the original list unchanged. `IO.puts` shows that the list remains unaffected despite the attempt to delete an element.

The `bugSolution.ex` demonstrates the correct way to accomplish this using `Enum.filter` or list comprehensions.