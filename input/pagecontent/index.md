

Show a Mermaid diagrams.

### Mermaid Diagrams

#### Simple Mermaid Diagram

```mermaid
graph TD
    A[Observation] -->|profiles| B[Blood Pressure]
    A[Observation] -->|profiles| C[Height]
    A[Observation] -->|profiles| D[Weight]
```

#### Sequence Diagram

```mermaid
sequenceDiagram
    participant A as Alice
    participant B as Bob
    A->>B: Hello Bob, how are you?
    B-->>A: I am good, thanks!
```

#### Flowchart

```mermaid
flowchart LR
    A[Start] --> B{Is it working?}
    B -- Yes --> C[Great!]
    B -- No --> D[Check the code]
    D --> E{Is the code correct?}
    E -- Yes --> F[Check dependencies]
    E -- No --> G[Fix the code]
    F -- Yes --> C
    F -- No --> H[Update dependencies]
    H --> C
```

#### Gantt Chart

```mermaid
gantt
    title Project Timeline
    dateFormat  YYYY-MM-DD
    section Development
    Task A       :a1, 2024-01-01, 30d
    Task B       :a2, after a1, 20d
    Task C       :a3, after a2, 10d
```

#### Class Diagram

```mermaid
classDiagram
    class Person {
        +String name
        +int age
        +void greet()
    }
    class Student {
        +String studentId
        +void study()
    }
    Person <|-- Student
```

#### State Diagram

```mermaid
stateDiagram
    [*] --> Idle
    Idle --> Processing : start
    Processing --> Idle : stop
    Processing --> Error : error
    Error --> Idle : reset
```

#### Pie Chart

```mermaid
pie
    title Distribution of Tasks
    "Task A" : 40
    "Task B" : 30
    "Task C" : 20
    "Task D" : 10
```

##### Entity Relationship Diagram

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE_ITEM : contains
    CUSTOMER }|..|{ DELIVERY_ADDRESS : uses
```

#### User Journey Diagram

```mermaid
journey
    title User Journey
    section Login
      User: 5: Click login button
      System: 4: Display login form
      User: 3: Enter credentials
      System: 2: Validate credentials
      System: 1: Grant access
```


#### Mind Map

```mermaid
mindmap
    root((Root))
        sub1((Subtopic 1))
            sub1a((Subtopic 1a))
            sub1b((Subtopic 1b))
        sub2((Subtopic 2))
            sub2a((Subtopic 2a))
            sub2b((Subtopic 2b))
```

### Plantuml Diagrams

#### Simple Plantuml Diagram

<div>
{% include observation-profiles.svg %}
</div>

#### Plantuml Sequence Diagram

<div>
{% include sequence-diagram.svg %}
</div>

#### Plantuml Flowchart

<div>
{% include flowchart-debugging.svg %}
</div>

#### Plantuml Gantt Chart

not supported by Plantuml, but can be created using Mermaid as shown above.

#### Plantuml Class Diagram

<div>
{% include class-person-student.svg %}
</div>

#### Plantuml State Diagram

<div>
{% include state-processing.svg %}
</div>

#### Plantuml Pie Chart

<div>
{% include pie-task-distribution.svg %}
</div>

#### Plantuml Entity Relationship Diagram

<div>
{% include erd-customer-order.svg %}
</div>

#### Plantuml User Journey Diagram

<div>
{% include user-journey-login.svg %}
</div>

#### Plantuml Mind Map

<div>
{% include mindmap-topics.svg %}
</div>

### Source

The source code for this Implementation Guide can be found on [GitHub](https://github.com/JohnMoehrke/testMermaid)

#### Cross Version Analysis

{% include cross-version-analysis.xhtml %}

#### Dependency Table

{% include dependency-table.xhtml %}

#### Globals Table

{% include globals-table.xhtml %}

#### IP Statements

{% include ip-statements.xhtml %}
