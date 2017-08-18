# KCDC 2017 Notes

## Machine Learning

David Body

* Linear regression
  * Gradient descent
* Binary classification
  * sigmoid/logistic function
  * confusion matrix
* Neural networks
  * perceptron: like linear regression, returns binary value
  * combine perceptrons into layers to make network
  * soft max
* MNIST database of handwritten digits
  * neural network with sigmoid activation functions
  * TensorFlow & Keras (Python) (https://keras.io/)
  * Training data (55,000), validation set (5,000), and test set (10,000)
  * categorical cross-entropy loss function
  * RMSprop optimizer (learning rate is adapted for each param)
  * train with 512 sample
  * evaluate model accuracy on the test data

## Don't Refactor, Rebuild

@wouterla
lagerweij.com

* strangler pattern
  * proxy layer to the legacy system
  * intercept requests and send to the new system
  * feature toggles
* CD
* BDD
  * scrap features that aren't actually needed anymore
* goals
  * 100% coverage
  * full automation
  * multiple releases per day
  * confidence

## Product + Architecture

@joeltosi

* story maps
* decision points
  * isolated vs dependent
  * known vs unknown
* coupling: "what if" a microservice was gone?
* use demos & feedback to validate your architecture
* Try
  * Document product assumptions
  * Document technical assumptions
  * Think of 3 ways you might be wrong. For each error, what would you do differently?

## ES Futures

@jeffreystrauss

* ES2017
  * object static methods: Object.values(), Object.entries()
  * async/await. wraps result in a promise.
    * await must be inside async func

## Settlers of Catan

qedcode.com

* DoF (independent vars) = number of unknowns minus number of equations
* number of mutable fields
* event sourcing pattern

## Jenkins

github.com/wellcorp examples

* pipeline plugin
* multibranch plugin
* Github Organization plugin
* write your own Groovy DSL (reference common tasks)

## Redux

@mlwigdahl
github.com/mlwigdahl

* react-redux
* middleware
  * redux-thunk -- action creators have dispatch/getState callbacks (lightweight but powerful)
  * redux-saga -- "Watcher" & "worker" generator functions (async, testable, good community/docs)
  * redux-observable -- RxJS-based observables
  * redux-logic -- RxJS-based, but delcarative model (can handle complex cases)

## Reusable Components

* Audience (project, team, public, business) -- start small with a specific project to consume
* Rigid vs flexible (style, layout, logic) -- start rigid, add flexibility as needed
  * say no to adding more config options
  * create a new component maybe
  * fight for consistency & simplicity
* link (to 3rd party docs), wrap, or fork? -- start with link
  * Amount of customization varies
* wrapping HTML primitives
* when to add component to the lib -- try in 3 projects before putting it in lib
* documentation strategy
  * generate docs from JSDoc comments, or the code directly
  * example code to copy & paste
  * inline demo
  * list props
  * Bootstrap-like UI
  * REPL in the UI ideally
  * searching. component groups.
* atomic design (atoms, molecule, organism) -- component composition & modular design
* closed, inner, open source
  * inner source -- open up for PRs from other business units. team is benevolent dictators.
* package hosting

## console.log

* @glimpse/glimpse
* node --inspect && chrome canary
* vscode debugger

## Stakeholder

@anngaff

* books
  * Good to Great
  * How to Have a Good Day
  * How Remarkable Women Lead
  * 5 Dysfunctions of a Team
  * Drop the Ball. Tiffany Dufu.

## Yak Shaving

@jessitron

medium.com/the-composition series

* Attack yaks
  * Be careful about summoning them (for others)
  * Track problems in CI process. (yak emoji)
* Yak stack -- stacks of errors (rabbit hole)
  * Urgent? Go around it. Minimum: create an issue.
  * Track it (Slack personal channel)
  * generativity -- value of team productivity
* Abstract yak
  * working on problems you don't have (e.g. premature optimization)
* Trim yaks
  * broadly improving productivity (personal automation, documentation, refactoring)
  * (see Banno 10% time)
  * timebox
  * learning
    * spend an extra 15-20mins to go beyond what you need
    * understand the system
    * learn about rest of the business
  * help others: post notes in Slack. update README. automated scripts. blog post.
* Yakkity yaks -- talking to others. Communication.
  * Who knows what
  * What do we each need to know?
  * psychological safety -- team respect and want contributions
* Golden yak
  * change behavior, or eliminates a tradeoff, or opens entirely new options
  * e.g. CI/CD, automated tests, log aggregation, Elm
  * great play to play and find truth
* takeaways
  * Pairing
  * Proven usefulness (timeboxed)
  * Play
