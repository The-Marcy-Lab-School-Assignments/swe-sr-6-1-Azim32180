# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

Arrays, Linked Lists and Doubly Linked Lists all allow programmers to organize data in a sequence. So, how would you choose to use one over the other?

In your response, make sure to compare the time complexities for insertion, removal, and random access (grabbing a particular known element by index/position) for each data structure as well as memory usage and ease of traversal.

## Response 1

### Choosing Between Arrays, Linked Lists, and Doubly Linked Lists

This question is asking how to choose the best way to store and organize a list of items in programming, based on how you need to access, add, or remove items. The three main options—arrays, linked lists, and doubly linked lists—each have different strengths and weaknesses, especially when it comes to speed and memory use.

### Arrays

An **array** is like a row of numbered boxes, where each box holds an item. Since the positions are fixed, finding an item is very fast (**O(1)**), meaning it takes the same amount of time no matter how big the array is. However, inserting or removing an item in the middle is slow (**O(n)**) because everything after the changed item must be shifted to keep the order. Arrays use the least memory since they only store the items themselves, but their fixed structure can make frequent changes inefficient.

### Linked Lists

A **linked list** is like a chain, where each item holds a link (or pointer) to the next one instead of being stored in a fixed position. Because you must start at the beginning and follow the links one by one, finding an item takes **O(n)** time, which means the more items you have, the longer it takes. However, inserting or removing an item is much faster (**O(1)**) because you only need to update the nearby links without shifting everything. The downside is that linked lists use more memory than arrays since each item stores extra data for its link.

### Doubly Linked Lists

A **doubly linked list** works like a linked list but has two links per item—one pointing forward and one pointing backward. This makes it easier to move both directions in the list. Finding an item still takes **O(n)** time because you have to follow links, but inserting or removing items remains fast at **O(1)**. The tradeoff is even higher memory use since each item needs two links instead of one.

### Choosing the Right Data Structure

- **Arrays**: Best for fast lookups when the list doesn’t change much.
- **Linked Lists**: Better when you need frequent insertions and removals.
- **Doubly Linked Lists**: Useful when you need to move forward and backward easily but can afford extra memory use.

## Prompt 2

Imagine you are developing a web browser's "back" button functionality. When a user clicks "back," the browser should navigate to the previously visited webpage.

Would you use a stack or a queue to implement this functionality?

In your response, explain what a Stack/Queue is and why it would be best for this use case. Make sure that your response includes the terms LIFO or FIFO.

## Response 2

## The Stack: LIFO (Last In, First Out)

A **stack** follows the **LIFO** (Last In, First Out) rule. This means that the last item added to the stack is the first one to be removed.

When you visit a new webpage, it gets **pushed** onto the stack. Each time you visit a new page, the previous page gets added to the stack. When you click the "back" button, the most recent page is **popped** off the stack, bringing you back to the previous page.

## Example:

- You visit Page A.
- You visit Page B.
- You visit Page C.
- Clicking "back" takes you to Page B (the last page you visited).
- Clicking "back" again takes you to Page A.

This works because the stack keeps track of your browsing history in the right order.

## Why Not Use a Queue?

A **queue**, on the other hand, follows the **FIFO** (First In, First Out) rule. This means that the first item added to the queue is the first one to be removed.

If you used a queue for a browser's "back" button, the first page you visited would be removed first, which isn’t what you want when navigating back through your history.

## Example:

- You visit Page A.
- You visit Page B.
- You visit Page C.
- Clicking "back" would take you to Page A (the oldest page), which isn't the desired behavior.

## Conclusion

A **stack** works best for implementing the "back" button in a web browser because it maintains the correct order of pages based on the LIFO principle, allowing you to go back to the most recent page.

## Prompt 3

What is an Abstract Data Type and why are they worth learning about?

### Response 3

## Prompt 4

A few classic problems involving a stack are the `isBalanced` and `isPalindrome` functions. Choose one of these functions and provide a solution to it along with a brief lesson explaining how it works.

### Response 4
