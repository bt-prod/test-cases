
# Undo / Redo - Test Cases

#### **Known Issues**

* Undoing the insertion of characters can result in the cursor being misplaced. [#303](https://github.com/wordpress-mobile/gutenberg-mobile/issues/303)

#### **Precondition**

Start on a new empty post.

##### TC001

**Undo/redo block actions**

- From the example app, remove a few blocks.
- Press the Undo button to see them reappear.
- Press Redo to remove the blocks again.


##### TC002

**Undo/redo text**

- Write some text on a text based block .
- Press Undo until all new text has disappeared.
- Press Redo to see the text appear again.


##### TC003

**Undo/redo text format**

- On a rich-text based component, add some format (bold, links, etc…).
- Undo all changes and Redo them to arrive to the same state.



