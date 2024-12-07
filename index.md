---
layout: default
---

Text can be **bold**, _italic_, or ~~strikethrough~~.

[Link to another page](./another-page.html).

There should be whitespace between paragraphs.

There should be whitespace between paragraphs. We recommend including a README, or a file with information about your project.

# Header 1

This is a normal paragraph following a header. GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere.

## Header 2

> This is a blockquote following a header.
>
> When something is important enough, you do it even if the odds are not in your favor.

### Header 3

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```python
print("Welcome to Maciejs python calculator!")

while True:
    number1 = float(input("Enter the first number: "))
    number2 = float(input("Enter the second number: "))

    print("Choose your operation: ")
    print("1 = Addition")
    print("2 = Subtraction")
    print("3 = Multiplication")
    print("4 = Division")
    choice = int(input("Enter your choice! (1/2/3/4)"))

    if choice == 1:
        result = number1 + number2
        print(f"The result of the addition is: {result}")
    elif choice == 2:
        result = number1 - number2
        print(f"The result of the subtraction is: {result}")
    elif choice == 3:
        result = number1 * number2
        print(f"The result of the multiplication is: {result}")
    elif choice == 4:
        if number2 == 0:
            print("Division by zero is not possible!")
        else:
            result = number1 / number2
            print(f"The result of the division is: {result}")
    else:
        print("Invalid choice! Input 1, 2, 3 or 4")

    repeat = input("Do you want to perform another calculation? (Yes/No)").lower()
    if repeat != 'yes':
        print("Thank you for using Maciejs python calculator! Have a nice day/evening/night!")
        break
```

#### Header 4

*   This is an unordered list following a header.
*   This is an unordered list following a header.
*   This is an unordered list following a header.

##### Header 5

1.  This is an ordered list following a header.
2.  This is an ordered list following a header.
3.  This is an ordered list following a header.

###### Header 6

| head1        | head two          | three |
|:-------------|:------------------|:------|
| ok           | good swedish fish | nice  |
| out of stock | good and plenty   | nice  |
| ok           | good `oreos`      | hmm   |
| ok           | good `zoute` drop | yumm  |

### There's a horizontal rule below this.

* * *

### Here is an unordered list:

*   Item foo
*   Item bar
*   Item baz
*   Item zip

### And an ordered list:

1.  Item one
1.  Item two
1.  Item three
1.  Item four

### And a nested list:

- level 1 item
  - level 2 item
  - level 2 item
    - level 3 item
    - level 3 item
- level 1 item
  - level 2 item
  - level 2 item
  - level 2 item
- level 1 item
  - level 2 item
  - level 2 item
- level 1 item

### Small image

![Octocat](https://github.githubassets.com/images/icons/emoji/octocat.png)

### Large image

![Branching](https://guides.github.com/activities/hello-world/branching.png)


### Definition lists can be used with HTML syntax.

<dl>
<dt>Name</dt>
<dd>Godzilla</dd>
<dt>Born</dt>
<dd>1952</dd>
<dt>Birthplace</dt>
<dd>Japan</dd>
<dt>Color</dt>
<dd>Green</dd>
</dl>

```
Long, single-line code blocks should not wrap. They should horizontally scroll if they are too long. This line should be long enough to demonstrate this.
```

```
The final element.
```
