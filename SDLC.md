# SDLC - Software Development Life Cycle

 - [SDLC Phases](#sdlc-phases)
   - [1. Planning](#1-planning)
   - [2. Requirement gathering / Feasibility](#2-requirement-gathering--feasibility)
   - [3. Designing (Optional in case considering 5 phases)](#3-designing-optional-in-case-considering-5-phases)
   - [4. Building/Development/Implementation ](#4-buildingdevelopmentimplementation)
   - [5. Testing](#5-testing)
   - [6. Deploy ](#6-deploy)
   - [7. Documenting (Optional in case considering 7 phases)](#7-documenting-optional-in-case-considering-7-phases)
   - [8. Operations and Maintainance ](#8-operations-and-maintainance)
 - [SDLC Methodologies](#sdlc-methodologies)
   - [1. Waterfall](#1-waterfall)
   - [2. Agile](#2-agile)
     - [Agile Estimation Techniques](#21-agile-estimation-techniques)
   - [3. Iterative](#3-iterative)
   - [4. Spiral](#4-spiral)
   - [5. DevOps](#5-devops)
   - [6. Others](#6-others)
     - [6.1 Lean (originally used in manufacturing by Toyota)](#61-lean)
     - [6.2 SAFe (uses both agile and lean principles)](#62-safe-uses-both-agile-and-lean-principles)
 - [Choose right model for your project](#choose-right-model-for-your-project)
   - [1. Know them all](#1-know-them-all)
   - [2. Assess needs of stakeholders](#2-assess-needs-of-stakeholders)
   - [3. Define the criteria](#3-define-the-criteria)
   - [4. Decide](#4-decide)
   - [5. Optimize](#5-optimize)
   - [6. Summary](#6-summary)


# SDLC Phases
There are 5, 7 or 8 phases of standard software development, depending upon how you divide the task. We will consider it as an 8 step process.  
As per wiki "In software engineering, a software development process is the process of dividing software development work into distinct phases to improve design and product management"

SDLC shows you what’s happening, and exactly where your development process can improve.
Like many business processes, SDLC aims to analyze and improve the process of creating software. It creates a scalable view of the project, from day-to-day coding to managing production dates.

## 1. Planning
 - Outputs include project plans, cost estimations, and procurement requirements.
 - When you are finished, your plan should be something the entire team can understand.
## 2. Requirement gathering / Feasibility
  - Ensure that the project requirements help the end-user of the system.
  - Consider the users and how workable the feature is by gathering requirements from stakeholders and looking at as much relevant data as possible
  - Regardless of whether your team is working with a formal requirements document or a list of tickets, everyone has to understand each need
## 3. Designing (Optional in case considering 5 phases)
  - developers and designers prototype a feature or map out a solution
  - Prototyping is useful for getting early feedback and informing technical decisions. 
  - Without prototypes, there’s a risk that the team will waste time on production-ready solutions that don’t meet user needs.
  - In web development teams, a prototype often serves to show that the functionality works, although it will still need polishing.
## 4. Building/Development/Implementation 
  - turns your project’s requirements and prototypes into working code
  - phase in which you start to see something that resembles the final product
  - By the end of this stage, you will have a working feature to share with customers
  - Developers are the most involved during this phase. They will often need to confirm things with the product owner and the testers.
## 5. Testing
  - testers check for
      - Code quality
      - Code meets the stated requirements
      - Code is performant
      - Evidence of secure coding principles
## 6. Deploy 
  - Deploy your code
## 7. Documenting (Optional in case considering 7 phases)
  - This is an optional step where you document the learnings and details about the feature
## 8. Operations and Maintainance 
  - Developers watch software for bugs or defects
  - It is important to consider opportunities for when the development cycle starts over again.
  - Support specialists will report issues, product owners will help prioritize them, and developers will work with testers to make improvements.

# SDLC Methodologies

## 1. Waterfall
**Overview:**
 - Classic or most established method of development.
 - Goal is to finish each stage before moving on to the next one
 - Each phase relies on the information gathered from earlier stages and there is no going back

**Use when:**  
 - Project is small and has clearly defined requirements

**Pros:**  
 - Easy to understand and Simple to manage
 - Can only move on to the next step when the previous one is completed.

**Cons:**  
 - This model doesn’t work well if flexibility is needed or if the project is long term and ongoing.
 - lack of flexibility in changing scope during the development process
 - limited in speed

## 2. Agile

**Overview:**  
 - Agile is best described from 4 values and 12 principles that are specified in https://agilemanifesto.org/  
 - prioritizes shorter planning phases, staged delivery, and regular customer interaction.
 - It puts customer needs first
 - focuses strongly on user experience and input.
 - It focuses on getting something workable in front of users as soon as possible and then working on improvements.  
 - Focus is on the interactions between the users and developers, and developers work closely together to reduce feedback loops.

**Values:**  
 - `Individuals and interactions` over processes and tools
 - `Working software` over comprehensive documentation
 - `Customer collaboration` over contract negotiation
 - `Responding to change` over following a plan

**Principles behind Manifesto:**  
 - Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.
 - Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage.
 - Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.
 - Business people and developers must work together daily throughout the project.
 - Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.
 - The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.
 - Working software is the primary measure of progress. 
 - Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.
 - Continuous attention to technical excellence and good design enhances agility.
 - Simplicity--the art of maximizing the amount of work not done--is essential.
 - The best architectures, requirements, and designs emerge from self-organizing teams.
 - At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly.

**Implementing frameworks:**  
It is a set of guidlines, can be implemented via below frameworks  
 - Scrum
 - Kanban
 - Extreme Programming (XP)

**Use when:**  
 - best choice for customers with uncertain requirements and creative projects.

**Pros:**  
 - Seeks to release software cycles quickly, to respond to a changing market.
 - Due to continous feedback in every iteration, users get to see quick improvements and feels ownership
 - Gained lots of momentum in recent years. Using Agile methodology is often a selling point when hiring staff.

**Cons:**  
 - Produces what the client wants quickly, but if the client doesn’t know what they need, developers waste time.
 - Can also lead to a project going off-track by relying too heavily on customer feedback.

### 2.1 Agile Estimation Techniques:  

 > Estimation is one of the simplest, yet most frightening activities that software professionals face. So much business value depends on it. So much of our reputations ride on it. So much of our angst and failure are caused by it. It is the primary wedge that has been driven between business people and developers. It is the source of nearly all the distrust that rules that relationship.    - Robert C Martin (Uncle Bob)

 - **Planning Poker** 
   - All participants use numbered playing cards and estimate the items. 
   - There are free online tools as well that can be leveraged. 
   - Voting is done anonymous and discussion is raised when there are large differences. 
   - Voting is repeated till the whole team reached consensus about the accurate estimation. 
   - Planning poker works well when you have to estimate a relative small number of items (max 10) in a small team (5-8 people). 
   - Tip: try to keep the voting between affordable numbers.  Maximize the highest card to 13 points in case of 3 week sprint and to 8 in case of 2 weeks sprint.
 - **T-shirt Sizes**
   - This is a perfect technique for estimating a large backlog of relative large items i.e Features
   - Especially when you have several concurrent scrum teams working on the same product. 
   - Items are estimated into t-shirt sizes: XS, S, M, L, XL. 
   - The decision about the size is based on an open and mutual collaborative discussion. 
   - This method is an informal and quick way to get an rough feeling about the total size of your backlog.
 - **Dot Voting**
   - When you are faced with a relative small set of items and in need of a super simple and effective technique to estimate you can use Dot Voting. 
   - This method has originated form decision making and you can use it for estimating. 
   - Each person gets a small number of small stickers and can choose to vote for the individual items. 
   - The more dots is an indicator of a bigger size. 
   - Works well in both small and large group. 
   - You have to limit the number of estimated items
 - **The Bucket System**
   - Much faster than planning poker is the Bucket System. 
   - This system is a good alternative when estimating a large number of items with a large group of participants. 
   - Create several buckets in the sequence of planning poker. 
   - The group estimates the items by placing them in these “buckets”. 
   - Buckets are usually different sheets of brown paper where you can place the sticky note with the item. 
   - But you can also use actual baskets to limit discussion about already processed items.
 - **Large/Uncertain/Small**
   - A very fast method of rough estimating is the Large/Uncertain/Small method. 
   - The team is being asked to place the items in one of these categories. 
   - The first step is to categorize the obvious items in the two extreme categories. 
   - Next the group can discuss the more complex items. 
   - This is actually a simplification of the bucket system. 
   - The system is especially good to use in smaller groups with comparable items. 
   - Next you can assign sizes to these 3 categories
 - **Affinity Mapping**
   - This method is based on finding similarities in the estimated items. 
   - The team is asked to group them together. 
   - Best way is to execute this is a visual way and order them form small groups to large. 
   - It works best with a small group of people and a relative small number of items. 
   - You can assign estimation numbers to the different groups.
 - **Ordering Method**
   - This is an exercise where you get an accurate image on the relative size of items
   - This works best in a small group of expert
   - All items are placed in random order on a scale label ranging from low to high.
   - Every participant is being asked to move one item on the scale. 
   - Each move is just one spot lower or one spot higher or pass the turn. 
   - This continues till no team member want to move items and passes their turn. 
   - The ordering protocol is a method of getting fine grained size estimates.
   - Works best with a relative small group of people and a large number of items.

### 2.4 Scrum vs Kanban

|Sr. no| Scrum                                              | Kanban                                            |
|-----:| -------------                                      |:-------------:                                    |
|  1   | well defined work; takes limited work              | its dynamic, can take extra work                  |
|  2   | immutable                                          | mutable                                           |
|  3   | time over burden                                   | focuses on continuous delivery                    |
|  4   | Structured and clear with goal                     | not structured but clear with goal                |
|  5   | Good number of meeting (planning, standup are must)| not a lot meeting (stand-up is not required)      |
|  6   | intervals ; sprint time                            | no intervals, work can be chosen on a daily basis.|
|  7   | more process, more overhead                        | less process and less overhead                    |
|  8   | good for new team and new project                  | for mature team                                   |

## 2.5 Scrum vs Kanban vs XP

| Type | Scrum                                              | Kanban                                            |  XP (Xtreme Programming)  |
| -----:| ------------- |:-------------:|:-------------:|
| Basic | Scrum is more suitable for teams who can devote their collective time to a project or product. It brings much more in the way of structure to help teams make major productivity gains through frequent communication and planning while still providing the freedom to decide among themselves how to engineer solutions.| Kanban is a really useful way for teams with a continually changing backlog of items to increase efficiency by limiting the amount of work-in-progress, whilst respecting existing roles and responsibilities.| XP is more towards Engineering process taken into account and incorporated in our process. XP adds another level of sophistication, bringing a strong focus on quality by insisting on a set of core engineering practices which keeps code clean and software stable. |
| Goal  | Use of cross-functional, self-organized, and empowered teams who divide their work into short, concentrated work cycles called Sprints. |  To alleviate impediments that cause us to take longer to deliver, not remove necessary pieces of the process. | To organize people to produce higher-quality software more productively. |
| Inception | In the mid 80’s, Hirotaka Takeuchi and Ikujiro Nonaka defined a flexible and all-inclusive product development strategy where the development team works as a unit to reach a common goal. Scrum has increased in popularity and is now the preferred project development methodology for many organizations globally. |  Kanban developed in the 1940s as a sub-component of the Toyota Production System and has its origins in these Lean and Just In Time (JIT) manufacturing processes. | XP has been created in 1996 by Kent Beck during his work on the Chrysler Comprehensive Compensation System (C3) payroll project. |
| Usage | The Scrum framework can only be used for small projects. However, it can easily be scaled for effective use in large projects. | One of the reasons many groups implement Kanban is to figure out how to deliver more consistently. Kanban, as well as many other methods/processes, is often chosen and implemented by the management or leadership layer and the values and goals are communicated down to developers or other individual contributors. | One of the reasons many groups implement Kanban is to figure out how to deliver more consistently. Kanban, as well as many other methods/processes, is often chosen and implemented by the management or leadership layer and the values and goals are communicated down to developers or other individual contributors.
| Speciality |  A key strength of Scrum lies in its use of cross-functional, self-organized, and empowered teams who divide their work into short, concentrated work cycles called Sprints. Scrum is one of the most popular Agile methodologies. It is an adaptive, iterative, fast, flexible, and effective methodology designed to deliver significant value quickly and throughout a project. Scrum ensures transparency in communication and creates an environment of collective accountability and continuous progress. | In Kanban the workflow is visualized: work is broken down into small, discrete items and written on a card which is stuck to a board; the board has different columns and as the work progresses through different stages (e.g. ready, in progress, ready for review etc) the card is moved accordingly. In Kanban the number of items that can be in progress at any one time is strictly limited. |  Extreme Programming is successful because it stresses customer satisfaction. Instead of delivering everything you could possibly want on some date far in the future this process delivers the software you need as you need it. Extreme Programming empowers your developers to confidently respond to changing customer requirements, even late in the life cycle.Extreme Programming emphasizes teamwork. Managers, customers, and developers are all equal partners in a collaborative team. |
| Values | `1. Focus`<br/>`2. Courage`<br/>`3. Openness`<br/>`4. Commitment`<br/>`5. Respect` | `1. Transparency`<br/>`2. Agreement`<br/>`3. Balance`<br/>`4. Respect`<br/>`5. Understanding`<br/>`6. Leadership`<br/>`7. Collaboration`<br/>`8. Customer focus`<br/>`9. Flow` | `1. Communication`<br/>`2. Simplicity`<br/>`3. Feedback`<br/>`4. Courage`<br/>`5. Respect`<br/> |
| key metrics | Sprint Velocity (2 weeks) | Cycle time. | Iteration time (2 weeks) |
| Activities | `1. Initiate`<br/>`2. Plan and Estimate`<br/>`3. Implement`<br/>`4. Review and Retrospect`<br/>`5. Release` | `1. To Do`<br/>`2. Development`<br/>`3. Test`<br/>`4. Release`<br/>`5. Done`<br/> | `1. Planning`<br/>`2. Managing`<br/>`3. Designing`<br/>`4. Coding`<br/>`5. Testing` |
| Accepting Change | Teams should strive to not make changes to the sprint forecast during the sprint. Doing so compromises leanings around estimation. | Change can happen at any time |  A high degree of developer discipline along with continuous customer involvement for the duration of the project.
| Flow | Regular fixed length sprints. | Continuous flow. | Iteration. |
| Release | At the end of each sprint if approved by the product owner. | Continuous delivery or at the team's discretion. | At the end of iteration.
| Practices | 1. Planning<br/>2. Daily Scrum<br/>3. Review and retrospective: Sprint Review and Sprint Retrospective<br/>4. Extension: Backlog refinement and Scrum of Scrums<br/>5. Artifacts: Product Backlog, Management, Sprint Backlog, Product Increment, Extensions (Sprint burn-down chart, Release burn-up chart) | 1. Visualize<br/>2. Limit Work-in-progress<br/>3. Manage Flow<br/>4. Make management policies explicit<br/>5.Improve collaboratively (using models and the scientific method) | **Fine scale feedback:** <br/> 1. Pair Programming <br/> 2. Planning Game <br/> 3. Test Driven Development <br/> **Continuous process:** <br/> 1. Continuous Integration <br/> 2. Design Improvement <br/> 3. Small Releases <br/> 4. Whole Team <br/> **Shared understanding:** <br/> 1. Coding Standards <br/> 2. Collective Code Ownership <br/> 3. Simple Design <br/> 4. System Metaphor <br/> **Programmer welfare:** <br/> 1. Sustainable Pace 

## 3. Iterative
**Overview:**  
 - Was introduced as the alternative to Waterfall
 - first step here is a planning step, the last one is deployment, with cyclical processes of design, implementation, testing, and evaluation in between.
 - This approach is also known as an incremental process because the final product is developed by working on smaller portions during each iteration.
 - Follows all the steps of the traditional Waterfall but in repetitive cycles called iterations. developers create an initial basic version of the software quickly.
 - Then they review and improve on the application in iterations
 - In Summary, Work towards the first specified need begins immediately, and new requirements lead to new iterations.

**Use when:**  
 - end goal is only very loosely defined.
 - very large applications.

**Pros:**
 - Get an application up and functional quickly to meet a business need
 - The team feels empowered to make changes and improve things as they go.
 -  gives software developers the opportunity to identify errors and fix them. 
 - It guarantees high-quality software as the end product.

**Cons:**  
 - Can exceed its scope quickly and risks using unplanned resources.
 - It’s hard to plan how long something will take.
 - You only know the number of iterations you’ll need to complete the project once it’s closer to being done.

## 4. Spiral
**Overview:**  
 - combination of the Iterative and Waterfall models
 - Every stage begins with a design goal and ends with the customer review. 
 - Developers start with a small set of requirements and move through each stage to fulfill them.
 - The Spiral methodology applies rigor to the Iterative approach.
 - Similar to the Iterative methodology, work happens in a cycle. Unlike Iterative, there is a specified method to follow.
 - In this methodology, developer teams:
   - Consider what stakeholders need
   - Identify and test approaches for satisfying the requirements
   - Find and mitigate risks that stem from the selected approaches
   - Get approval from stakeholders and commitment to pursue the next cycle

**Use when:**  
 - your project goals are unknown but you need to consider the risks before the development team starts working.
 - for expensive and complicated projects as it gives development teams a chance to generate a highly customized product and incorporate user feedback early on in the project.

**Pros:**  
 - The Spiral methodology allows for early feedback since the first iteration is quick to produce.
 - Unlike other methodologies which overlook feasibility analysis, Spiral looks for risks at each development iteration.
 - The approach ensures high-quality risk management as every single iteration starts by looking ahead to potential risks.

**Cons:**  
 - Working this way has the same drawbacks as working with Iterative development. It’s hard to see an end to the work.
 - You can mitigate this by getting stakeholder approval, but this can lead to bottlenecks.
 - Spiral requires special skills to evaluate risks and assumptions as well as high costs and time to reach the final product.

## 5. DevOps
**Overview:**  
 - In the DevOps model, developers and operations teams collaborate closely or work together, often as a combined team.
 - With the teams working together, updates to the software can happen more often than with other methodologies.
 - Your team might benefit from a DevOps model if a robust system from the outset of the project is what it needs.

**Use when:**  
 - 

**Pros:**  
 - Robust testing and stability from the outset are the main advantages of working with DevOps.
 - Within the DevOps methodology, deployed software is production-ready, secure and scalable.

**Cons:**
 - Merging two teams into one requires a large-scale mindset and culture change in a company.
 - Considering operations early on in the project often delays the first iteration.

## 6. Others

### 6.1 Lean 
**Overview:**  
  - founding in lean manufacturing principles
  - The Lean methodology prioritizes moving fast and cutting waste when possible.
  - To accomplish this, the development team focuses on one task at a time and achieves one milestone before working on the next

**Use when:**  
 - developer efficiency is a core team goal.

**Pros:**  
 - Taking a Lean approach allows teams to incorporate lessons learned from past inefficiencies.
 - This drive to be efficient leads to well-functioning teams in the long run.
 - Once the team is working efficiently, it produces a lot of value for stakeholders in a short time.

**Cons:**  
 - Onboarding new people into a Lean process can be a cultural shock. 
 - Therefore, team managers need to plan onboarding more carefully than they would if they were working with other methodologies.
 - Also, the team can only work on one feature at a time, which in the short term can cause conflicts with stakeholders.

The seven Lean principles are:  

 - `Eliminate waste`: Any step or feature that does not add value for the user is considered wasteful and should be eliminated.
 - `Optimize the whole`: Always focus on the entire development process and not just sub-steps.
 - `Amplify learning`: The software development process should be structured such that it enables learning for all the involved members.
 - `Empower the team`: Show respect to your project team and allow them the freedom to make decisions and take ownership of the development process.
 - `Decide as late as possible`: Instead of making rash decisions, take your time to evaluate every possible option, gather information and then make an informed decision.
 - `Deliver as fast as possible`: To make the delivery of software products swift, the software team should meet deadlines to deliver each component on the right time.
 - `Build quality in`: To develop quality software products, quality assurance should be done at every step throughout the process and every aspect of the process should be made efficient.

### 6.2 SAFe (uses both agile and lean principles)

[Wiki](https://en.wikipedia.org/wiki/Scaled_agile_framework): The Scaled Agile Framework (SAFe) is a set of organization and workflow patterns intended to guide enterprises in scaling lean and agile practi
ces.  
SAFe promotes alignment, collaboration, and delivery across large numbers of agile teams. It was developed by and for practitioners, by leveraging three primary bodies of knowledge: agile software development, lean product development, and systems thinking.  
Starting at its first release in 2011 already five major versions have been released[10] while the latest edition, version 5.0, was released in January 2020

Also, In case you do not understand anything while doing any of the ceremonies, you could quickly search that in below URL and you will get the
detailed answer  

Ask me anything URL: https://www.scaledagileframework.com/glossary/


**Underlying principles of SAFe**  
According to its authors, SAFe is based upon ten underlying concepts, which are derived from existing lean and agile principles, as well as observation:[25]

 - Take an economic view
 - Apply systems thinking
 - Assume variability; preserve options
 - Build incrementally with fast integrated learning cycles
 - Base milestones on objective evaluation of working systems
 - Visualize and limit work-in-progress, reduce batch sizes, and manage queue lengths
 - Apply cadence (timing), synchronize with cross-domain planning
 - Unlock the intrinsic motivation of knowledge workers
 - Decentralize decision-making
 - Organize around value

![Ceremonies](https://github.com/girirajvyas/101-series/blob/master/resources/images/sdlc/SAFe_Ceremonies.PNG "SAFe ceremonies")

**Ceremonies**  
 - https://www.scaledagileframework.com/program-increment/
 - https://www.scaledagileframework.com/pi-planning/
 - https://www.scaledagileframework.com/pi-objectives/
 - https://www.scaledagileframework.com/iterations/
 - https://www.scaledagileframework.com/iteration-planning/
 - https://www.scaledagileframework.com/iteration-retrospective/

**Key Stakeholders**  
 - https://www.scaledagileframework.com/agile-teams/
 - https://www.scaledagileframework.com/product-owner/
 - https://www.scaledagileframework.com/scrum-master/

**Key work items(Epic -> feature -> Story -> Task):**  
 - https://www.scaledagileframework.com/epic/
   - https://www.scaledagileframework.com/features-and-capabilities/
     - https://www.scaledagileframework.com/story/

**Note:**  "Epic has multiple features" and "Features has multiple stories" and "Story has Multiple tasks"

**Rally Status and Responsible for Action**  

|Sr. no| Status        | Responsible for Action                            |
|-----:| ------------- |:-------------:                                    |
|  1   | Unelaborated  | Product Owner writes the first draft                  |
|  1   | Defined       | After Sprint planning and after each team member agrees it is defined. i.e it can be worked upon                  |
|  1   | In Progress   | Create tasks on the first day and move to In Progress                  |
|  1   | Completed     | Mark complete once all tasks are completed and deployed                |
|  1   | Accepted      | After demo marked as Accepted by the Product owner                  |
|  1   | Ready to ship | Once feature is released                  |

**Feature Sizing**  

|Sr. no| Size (Tee shirt sizing)   | Story Points (Fibonacci series)     |
|-----:| -------------             |:-------------:    |
|  1   | XS                        |    15             |
|  1   | S                         |    30             |
|  1   | M                         |    45  (30 + 15)  |
|  1   | L                         |    75  (45 + 30)  |
|  1   | XL                        |    120 (75 + 45)  |
|  1   | 2XL                       |    195 (120 + 75) |

**Resources**  
 - https://www.scaledagileframework.com/safe-lean-agile-principles/
 - https://www.guru99.com/scaled-agile-framework.html


# Choose right model for your project

## 1. Know them all
In order to make a selection, it is very important that you have experience with them or atleast have knowledge about each one of them

## 2. Assess needs of stakeholders
We must study the business domain, stakeholders concerns and requirements, business priorities, our technical capability and ability, and technology constraints to be able to choose the right SDLC against their selection criteria.

## 3. Define the criteria
Some of the selection criteria or arguments that you may use to select an SDLC are:

 - Is the SDLC suitable for the size of our team and their skills?
 - Is the SDLC suitable for the selected technology we use for implementing the solution?
 - Is the SDLC suitable for client and stakeholders concerns and priorities?
 - Is the SDLC suitable for the geographical situation (distributed team)?
 - Is the SDLC suitable for the size and complexity of our software?
 - Is the SDLC suitable for the type of projects we do?
 - Is the SDLC suitable for our software engineering capability?
 - Is the SDLC suitable for the project risk and quality insurance?

## 4. Decide
When you define the criteria and the arguments you need to discuss with the team, you will need to have a decision matrix and give each criterion a defined weight and score for each option. After analyzing the results, you should document this decision in the project artifacts and share it with the related stakeholders.

## 5. Optimize
You can always optimize the SDLC during the project execution, you may notice upcoming changes do not fit with the selected SDLC, it is okay to align and cope with the changes. You can even make your own SDLC model which optimum for your organization or the type of projects you are involved in.

## 6. Summary
 - The methodology you pick for a particular project will depend on the constraints of the projects and the people involved
 - The methodologies we’ve talked about today are frameworks for doing excellent work. They are only as good as their implementation. If an implementation isn’t working for you, change it.
 - The best teams adopt the spirit of a methodology and implement it in a way that works for them.
 - should have enough experience and familiarity with the SDLCs that will be chosen and understand them correctly

Developing high performing teams with Devops Culture  

 - Version control everything: source code, documents, scripts, tasks
 - Continous integration and deployments
 - Automate everything (*Almost) - Builds, Testing, Releases, Configurations
 - Bring the pain forward (move left)
 - Built-in quality: Shorter feedback loops, code quality and security
 - Definition of done: Requirement is 'done' only when its in production 
 - Everyone is responsible: No to - 'it works in our local env'
 - Repeatable reliable process: process to release same in all environemnts
 - Continous improvement: Review, revisit and brainstorm
 - Adapt cloud services: IAAS, PAAS
 - Team environments, Integration Environments
 - Branching Strategies
 - Customer centric actions
 - Cross functional teams

# References:
SDLC:  
 - https://textexpander.com/blog/7-stages-of-the-system-development-life-cycle/
 - https://textexpander.com/blog/sdlc-methodologies/
 - https://phoenixnap.com/blog/software-development-life-cycle

Estimation:  
 - https://technology.amis.nl/2016/03/23/8-agile-estimation-techniques-beyond-planning-poker/

Choose SDLC:  
 - https://melsatar.blog/2012/03/21/choosing-the-right-software-development-life-cycle-model/
 - https://hygger.io/blog/choosing-sdlc-methodology-for-projects/
 - https://melsatar.blog/2012/03/21/choosing-the-right-software-development-life-cycle-model/

Comparison:  
 - https://www.visual-paradigm.com/scrum/scrum-vs-waterfall-vs-agile-vs-lean-vs-kanban/
 - https://community.simplilearn.com/threads/agile-scrum-vs-kanban-vs-xp-in-a-nutshell-%E2%80%93-paradise-in-worldwide-portfolio-management.22136/
 - https://www.planview.com/resources/guide/lean-principles-101/agile-and-lean

KPIs:  
 - https://phoenixnap.com/blog/devops-metrics-kpis
 - https://www.intellectsoft.net/blog/agile-metrics/ 
 - https://www.sealights.io/code-quality/code-quality-metrics-is-your-code-any-good/