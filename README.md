# Tech Records

> A Technology's Records for Tech Lead to research


## Tech Vision

### Explain


#### Explain（Chinese）

| 关键因素 | 描述 |
| --- | --- |
| 对于 |  xxx |
| 我们的 | xxx |
| 是一个 | xxx |
| 它可以 | xxx |
| 但它不同于 | xxx |
| 它的优势是 | xxx |

示例

| 关键因素 | 描述 |
| --- | --- |
| 对于 | 想拆解单体前端应用的团队 |
| 我们的架构 | 微应用化 |
| 是一个 | 类微前端架构 |
| 它可以 | 在开发环境将应用拆分成一个个的模块化应用，在构建时以单体的形式构建 |
| 但他不同于 | 微前端架构 |
| 它的优势是 | 实施成本低、技术难度小、维护成本低 |

## Tech Debt Records


### Explain


#### Explain(English)

> Technical debt (also known as design debt[1] or code debt) is a concept in software development that reflects the implied cost of additional rework caused by choosing an easy solution now instead of using a better approach that would take longer.


|  Title | Description |
|--------|-------------|
| Tech Debt ID | Records ID |
| Date | date |
| Reporter | reporter |
| Title | Name to identified tech debt |
| Description | description detail of tech debt |
| Alternatives | possible alternative solutions |
| Rationale  | reason to fix tech debt |


<caption>Technical debt quadrants</caption>

|   | Reckless | Prudent |
|---|----------|---------|
| Deliberate | "We don't have time for design" | "We must ship now and deal with consequences (later)" |
| Inadvertent | "What's Layering?" | "Now we know how we should have done it" |

from: [https://en.wikipedia.org/wiki/Technical_debt](https://en.wikipedia.org/wiki/Technical_debt)

#### Explain（Chinese）

> 技术负债（英语：Technical debt），又译技术债，也称为设计负债（design debt）、代码负债（code debt），是编程及软件工程中的一个比喻。指开发人员为了加速软件开发，在应该采用最佳方案时进行了妥协，改用了短期内能加速软件开发的方案，从而在未来给自己带来的额外开发负担。

<caption>技术债务的四象限分类</caption>

|   | 鲁莽Reckless | 谨慎Prudent |
|---|-------------|-------------|
| 故意Deliberate | 我们没有时间做设计"We don't have time for design" | 我们必须马上交付，后果以后再说"We must ship now and deal with consequences (later)" |
| 疏忽Inadvertent | 什么是分层（设计）？"What's Layering?" | 现在我们才知道该如何做了"Now we know how we should have done it" |

from: [https://zh.wikipedia.org/wiki/%E6%8A%80%E6%9C%AF%E8%B4%9F%E5%80%BA](https://zh.wikipedia.org/wiki/%E6%8A%80%E6%9C%AF%E8%B4%9F%E5%80%BA)


### usecases

## Architeture Decision Records

### Explain

#### Explain

| Title | Description | 
|-------|-------------|
| Title | These documents have names that are short noun phrases. For example, "ADR 1: Deployment on Ruby on Rails 3.0.10" or "ADR 9: LDAP for Multitenant Integration" |
| Context | This section describes the forces at play, including technological, political, social, and project local. These forces are probably in tension, and should be called out as such. The language in this section is value-neutral. It is simply describing facts. |
| Status | A decision may be "proposed" if the project stakeholders haven't agreed with it yet, or "accepted" once it is agreed. If a later ADR changes or reverses a decision, it may be marked as "deprecated" or "superseded" with a reference to its replacement. |
| Decision |  This section describes our response to these forces. It is stated in full sentences, with active voice. "We will ..." |
| Consequences | This section describes the resulting context, after applying the decision. All consequences should be listed here, not just the "positive" ones. A particular decision may have positive, negative, and neutral consequences, but all of them affect the team and project in the future. | 

#### Explain（Chinese）

| 标题 | 说明  |
|-----|-------|
| 标题 | 这些文件的名称是短名词短语。例如，“ADR 1: Deployment on Ruby on Rails 3.0.10” 或 “ADR 9: LDAP for Multitenant Integration |
| 上下文 | 这一节描述了当前的技术、政治、社会和项目。这些力量可能处于紧张状态，应该这样说。本节中的语言是价值中立的，只用于描述事实。 |
| 决策 | 这一节描述我们对这些力量的回应。这是充分的句子，以及积极的声音。 “我们会...” |
| 状态 | 如果项目利益相关方尚未同意，或者一旦达成一致，则 “决定” 可能被 “提议”。如果以后的 ADR （架构决策记录）更改或撤消决定，则可能会将其标记为 “已弃用” 或 “已取代”，并参考其替换。 |
| 后果 | 这部分描述了应用决策后产生的上下文。所有的后果应该列在这里，而不仅仅是 “积极的”。一个特定的决策可能会产生积极的、消极的和中性的后果，但是它们都会影响未来的团队和项目。 |

## Clean Architeture Usecases Records


### Example

Source: [https://fullstackmark.com/post/11/better-software-design-with-clean-architecture](https://fullstackmark.com/post/11/better-software-design-with-clean-architecture)

| Title | Register for courses |
|-------|----------------------|
| Description | Student accesses the system and views the courses currently available for him to register. Then he selects the courses and registers for them. |
| Primary Actor | Student |
| Preconditions | - Student is logged into system <br> - Student has not previously enrolled or registered <br> - Student cannot register within 5 days of course start date |
| Postconditions | Student is registered for courses |
| Main Success Scenario | 1.  Student selects "Register New Courses" from the menu. <br> 2.  System displays list of courses available for registering.  <br> 3.  Student selects one or more courses he wants to register for.  <br> 4.  Student clicks "Submit" button.  <br> 5.  System registers student for the selected courses and displays a confirmation message. |
| Extensions |  (2a) No courses are available for this student.  <br> 1.  System displays error message saying no courses are available, and provides the reason & how to rectify if possible.  <br> 2.  Student either backs out of this use case, or tries again after rectifying the cause.  <br> (5a) Some courses could not be registered.  <br> 1.  System displays message showing which courses were registered, and which courses were not registered along with a reason for each failure.  <br> (5b) None of the courses could be registered.  <br> 1.  System displays message saying none of the courses could be registered, along with a reason for each failure. | 
