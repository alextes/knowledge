# Simple
Thoughts on simplicity in software development. Mostly inspired by Simple Made Easy by Rich Hickey.

Simple is the converse of complex. Complexity in dev is :[ .
 _define 'complex', define 'simple'._

Explain in terms of near and distant or easy and difficult. 

The common pitfalls (three notions of nearness or difficulty):
* Is it easy to obtain? Near in the sense of accessibility.
* Is it easy to understand, familiar? If you don't know arithmetic: 1 + 1 = 2. Or if you're not japanese, japanese. Does that make it unreadable? i.e. extremely complex?
* Is it easy to use? Capability. Playing the violin. Climbing a mountain. Writing Java. For concepts hubris and insecurity kick in.

## Easy

### Easy is not simple
Easy does not mean simple. Conversely hard does not equal complex. Easy can be thought of as nearness. How far away is the thing you want to get, lets call this destinational far-ness, or conversely how close are you to the thing you're trying to obtain, origin close-ness. A good example to clarify these concepts with is basic arithmetic. Lets define our knowledge origin as low. Say the knowledge of a 5 or 6 year old. Arithmetic might be very hard to read to a 6 year old but is regardless, very simple to understand. Even the symbolism is simple and that's why it's easy to explain. In other words, basic arithmetic is very near, conceptually no matter what your current knowledge, your origin. The concepts within are simple and immediately obvious. Placing two single apples together makes for a collection of two apples. 1 + 1 = 2.

### Easy is relative
Things can be _near_ because of your familiarity or skill with them. Playing the violin for example. Your knowledge origin is close to your knowledge destination. Skill and Knowledge can make hard things easy. Capibility and Understanding can make hard things easy. Easy is relative.

### Easy to obtain (near)
It is near in the sense it is easy to obtain. Through tooling, internet. Can you run it within five seconds.
#### Speed

### Easy to read (near)
Near what we know. Familiarity.

### Easy to read, use, (simplicity?) through familiarity (near)
It is near in the sense we can easily get to the state we want to be in. If you want everything to be familiar you will never learn anything new.

### Easy to comprehend
* Simplicity. (Arithmetic)
* Immediate apparentness of meaning. (Arithmetic / German)

### Easy, Fast, Effective?
Only works short term if you ignore complexity. Development does not work in sprints. It's the same codebase every week. Eventually, going the easy route whilst making things more complex slows you down more than it speeds you up.

## Simplicity and Complexity
Ease of understanding, ease of change, ease of debugging, 

### Cardinality
Few is not automatically simple. Conversely many is not automatically hard. Addition does not become more complex when one expression features many terms. It might become harder to compute correctly just because humans make errors when making calculations but addition does not become any more complex.

### Simplicity is objective
Whether something is interleaved or not is often very possible to simply see from reading a piece of code. Does it do one thing? Is it twisting with something else?

### Simplicity of understanding vs. obtaining
Simple to understand is not always simple to obtain.

### Simplicity is crucial for right direction
Tests can tell you what not to do. Guardrails can tell drivers they are going somewhere they shouldn't. Test can help but also be completely useless in telling you where to go. For this you need to be able to reason about your program. In order to effectively reason about your program it needs to be simple.

### Incidental complexity
Code that doesn't change anything for the user but has more complexity than an alternative is incidental complexity. Latin for: your fault. Good examples are tools that make something easier but also add a lot of code, thus behavior, thus increasing complexity.

### Inherent complexity
Evironmental. Example is the systems we run our programs on. They differ. That makes it complex. This is why we use something like docker. We can't solve this inside our program. Not using too much memory in a program still blows up when enough programs are added to the system. You need more information / control to deal with this. That's why you have a docker agent that refuses to start containers that don't fit.

### Complecting and Composing
Intertwining, and placing together. Place four straight strings together and their structure is obvious. Braid them, literally 'complect them' and the structure becomes incredibly complex.

## How to we design simple things
Abstract for simplicity. Draw away complexity. Works by breaking up without complecting. How? Ask and don't complect what, who, how, when, where, why. 

There is really too much to be said here. WIP. I'll have to revisit. So many great ideas. I'm x_x .

When you have an orderable, of course you don't explain how to order it. Duh. Now you're complecting what with how. You explain what the order of something is. Alphabetical by ASCII charcode. Not how to sort it. 

## Conclusions

### Limiting complexity through choice
We look mostly at value, rarely at cost.

### Hard because difficult to obtain or unobtainable
Think cost of moving things near.
* How much do you pay for a library? 
* What licenses can you use? 
How many things are available in the ecosystem i.e. surroundings?

### Hard because unfamiliar
Great, now it is your problem, and you can solve it. If simple things are hard because you're unfamiliar with them, you can just learn them. Complexity knows no such luxury. You'll be forced to find or create a simpler solution if you still want to have an easy time reasoning about your program.

### Hard because complex
Incidental? Change it. Inherent to the problem? Sucks. You won't get smarter but you can try to simplify.

### Don't mix what with how
Polymorphism. Define what the order of something is not how to do ordering. Think Ord in Haskell. Traits in Rust. Interfaces. You do this wrong by supplying a function that sorts a list of x. Make how somebody else's problem.

## Things to consider
### So what about Golang?
Go is king of complecting what with how. It has no generics. You have to define how for every what. Want to map a list with elements of type x? Use a loop that complects what and how. So why are Go programmers so happy with their language regardless?