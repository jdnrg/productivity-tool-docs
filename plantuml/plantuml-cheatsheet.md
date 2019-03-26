# PlantUML Quick lookup table

## Diagram

### Behavior

### Structure

## UML

### Use Case

### Activity

### State

### Timing（Sequence）

KeyWord | Usage | Image
------ | ---- | ----
`->` | | ![](images/cheatsheet/sequence/image-arrow-1.png)
`<--` | | ![](images/cheatsheet/sequence/image-arrow-2.png)
`->>` | | ![](images/cheatsheet/sequence/image-arrow-3.png)
`<<--` | | ![](images/cheatsheet/sequence/image-arrow-4.png)

```
@startuml

actor Entrant

Entrant -> Ticket : Attend Event Request

activate Ticket
Ticket -> Member : Create Member Request

activate Member
Member -> Member : Create Member
Ticket <-- Member : Create Member Response
deactivate Member

Ticket -> Ticket : Create Ticket
Entrant <-- Ticket : Attend Event Response
deactivate Ticket

@enduml
```

![](images/cheatsheet/sequence/sequence-diagram.png)

### class

Keyword | Usage | Pictures
------ | ---- | ----
`class` | class | ![](images/cheatsheet/class-diagram/image-class.png)
`+` | Public | ![](images/cheatsheet/class-diagram/image-public.png)
`-` | Private | ![](images/cheatsheet/class-diagram/image-private.png)
`#` | Protected | ![](images/cheatsheet/class-diagram/image-protected.png)
`~` | Package | ![](images/cheatsheet/class-diagram/image-package.png)
<code><&#124;--</code> | extension | ![](images/cheatsheet/class-diagram/image-extension.png)
<code><&#124;..</code> | implements | 
`o--` | aggregation| ![](images/cheatsheet/class-diagram/image-aggregation.png)
`*--` | composition | ![](images/cheatsheet/class-diagram/image-composition.png)

```
@startuml
class User {
  username
  password
  +sign_in()
}

class Group {
  name
}

class Member {
  roles
}

User .. Member
Group .. Member
@enduml
```

![](images/cheatsheet/class-diagram/class-diagram.png)

### Object

### Component

## Common

###  Title、Note、Comment
Keyword | usage
------- | -----
`title` | Set a title. Use `\n` to indicate a line break in the title description. You can use some skinparam settings to specify the border of the title.
`title`, `end title` | Define multiple line headings. You can use the creole format in the title.
`note top`, `note top of` | Add a comment above.
`note bottom`, `note bottom of` | Add a comment below.
`note left`, `note left of`| Add a comment on the left.
`note right`, `note right of` | Add a comment on the right.
`note` | Add a note (do not specify a location).
`'` | All lines beginning with single quotes `'` are comment lines.
`/'`,`'/` | Multi-line comments begin with `/'` and end with `'/`.

```
@startuml
' You can use some skinparam settings to specify the border of the title.
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor red

' Set a title.
Title title, notes, and comments\nexamples

Object <|--- ArrayList
note top of Object : In java , every class\nextends this one.

/'
	Define a note with the note keyword alone.
You can then use the .. symbol to make a dashed line connecting it to other objects.
'/
note "This is a floating note" as N1
note "This note is connected\nto several objects." as N2
Object .. N2
N2 .. ArrayList

class Foo
note left: On last defined class
@enduml
```
![](images/cheatsheet/common/title-note-comment.png)

### Element

### Package

### Arrow

## Salt

### Basic widgets

### Tree widgets

## Tips

### Example

#### Component

#### Sequence
