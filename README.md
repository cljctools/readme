# cljctools

cljctools is a namespace for solving problems freely, for the purpose of value only.    
So it is and will be non-commercial, non-monetized by design.   
Open source.  
It's just tools. But hoping to be the f-ing best ones, made with heart.
Stuff should be made only if is needed for some living system. Needed - as in pain, fury, I-cant-take-it-anymore, it-must-be-done.

## rationale

#### disclaimer

  - cljctools project is in no relation to official clojure ecosystem, these are "fan-made" tools
  - the goal of this project is to contibute value-wise via creating fresh, even experimental tools, used for end-user systems (make stuff only if is needed)
  - this project hopes to grow to the level of clojure community and tooling, evolve from *reaping the fruit of others* to hopefully bringing value as well

#### why cljctools and why use clojure

- cljc stands for clojure common, meaning it is runtime-less (can run on jvm, browser, nodejs ...)
- when buidlding a system for users, you end up having abstractions(libraries, spec, protocols,data generation), that need to be run both on the server and on the client
- and even having javascript, typescript - with their catastrophic flaw of having no namespaces - you still appreciate how easy it is to create a pacakge(dependency) to be used both on nodejs and in browser
- but this is nothing compared to the reach and brilliant simplicity, human-being-nature of clojure: as of 2020, the most (it is not even close to be honest) powerful tool for programming
- besides giving you everything any other remotely-sane language has, clpjure also allows you to right runtime-less code for both server, nodejs and the browser
- clojure has **the most reach** of them all - as far as java and js combined
- and gifts us things other languages cannot dream of
  - it is a Lisp, but insanely more advanced
  - it is built from data, data everywhere, no parsing by means of edn (extensible data notation -> you can add stuff) and transit - the way to send data efficienly across network and runtimes
  - is functional, has immutability
  - is itself built in terms of abstractions (Sequential, Associative ... ), which can be implemented and extended
  - fully-qualified auto-resolved keywords (which is the key for designing you project and data - when everything is fully-qualified, no need to hold stuff in your head or for cheats/tricks )
  - protocols, ability to reify, giving you the most able "constructor" in the world - because it's just a function with lexical (scoped) closure 
  - macros and macroexpansion, giving you the most powerful tool to validate/transform anything at compile time - a function call and the whole damn language inside it
  - .cljc extension and reader conditionals, allowing you to have conditional runtime-specific code in the same file #?(:clj (do this) :cljs (do that))
  - clojure.spec - the most elegant and simple, yet powerful way to programmatically describe/generate/validate and understand your data once
  - transducers - no words can be found for what an ahievement that is - a correct way to process a value through steps without creating intermidiate collections, and it's built right into the language  already
  - atoms (watchable atomic state), has transients (to do stuff manually for efficiency), has deps.edn to load deps from local dir ot github commit hash and on and on ..
- and the most important superpower - core.async
  - notice golang, which has become the go-to tool for cloud native and server-side world without having any code base java ecosystem provides
  - golang had to start from sratch, and it delivered kubernetes and docker - the defacto operating systems of the cloud world
  - why? because it has channels built into the language, they are *the* design goal
  - by handling asynchrony via process and channels (queues), passing channels around, systems can be built sanely
  - good news: clojure has exaclty that and quite a bit more, alongside all other features
  - core.async allows us to design your system as processes and queues (channels), and unbelievably core.async is a runtime-less abstraction, runs on both jvm, nodejs and in the browser 
  - as the creator of clojure says in his talk on core.async "function chains are poor machines", "good programs should be made out of processes and queues"

#### with that in mind

  - cljctools by design build abstractions as processes, with core.async being part of the language (as it is with golang)
  - not every abstraction needs to implemented for every runtime, but it should be defined in terms of protocols and api, with the ability to add another runtime implementation later
  - that is why cljctools libraries will have a meta package, dependecy-less .cljc code (spec, protocols, channel api) so that implementations could share the same abstraction definition

#### bigger aspirations
  - mult: a VSCode extension for clojure(script) https://github.com/cljctools/mult/blob/master/docs/design.md#rationale
  - sol: creating a better (simpler) building tool for clojurescript (the name will be "sol" - as in solution, or a day on Mars)
  - nrepl: implementing nrepl anew, with the same protocol at the core, but with the ability to run on nodejs (for self-hosting cljs inside VSCode editor, for full cljs REPL support right in the editor )
  - editor: creating and editor in clojure(script), but only if it can be done better than VSCode
  - origin cluster: an automated volunteer self-forming cloud  https://github.com/DeathStarGame/docs/blob/master/origin-cluster/origin-cluster.md#origin-a-volunteer-automated-cluster
  - opensource database: would it be possible to make a db like dgraph, but with clojure language itself as a query language?
  - ...

#### who should benefit from cljctools
  - users and user facing systems
  - any tool should be made only if it is needed - needed - for an end-user system or creation of such system

## why not monetize this project or monetize that ? you're an idiot, money is a blood system... bla bla

Go buck yourself. This is a children's playgorund. A money free zone, fun zone.

As Jesus says:

> <b>19 “Do not store up for yourselves treasures on earth, where moths and vermin destroy, and where thieves break in and steal. 20 But store up for yourselves treasures in heaven, where moths and vermin do not destroy, and where thieves do not break in and steal. 21 For where your treasure is, there your heart will be also.</b>

> <b>22 “The eye is the lamp of the body. If your eyes are healthy,[c] your whole body will be full of light. 23 But if your eyes are unhealthy,[d] your whole body will be full of darkness. If then the light within you is darkness, how great is that darkness!</b>

> <b>24 “No one can serve two masters. Either you will hate the one and love the other, or you will be devoted to the one and despise the other. You cannot serve both God and money.</b>

source: [NIV Bible, Matthew:6](https://www.biblica.com/bible/niv/matthew/6/)


## links
- mailing list
  - https://groups.google.com/g/cljctools
  - cljctools@googlegroups.com
