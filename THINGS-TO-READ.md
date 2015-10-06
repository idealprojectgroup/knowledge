### [Sandi Metz’ rules for developers](http://robots.thoughtbot.com/post/50655960596/sandi-metz-rules-for-developers)
- Classes can be no longer than one hundred lines of code.
- Methods can be no longer than five lines of code.
- Pass no more than four parameters into a method. Hash options are parameters.
- Controllers can instantiate only one object. Therefore, views can only know about one instance variable and views should only send messages to that object `@object.collaborator.value` is not allowed).

### [What I Wish I Knew When Starting Out as a Software Developer](http://blog.salsitasoft.com/what-i-wish-i-knew-when-starting-out-as-a-software-developer-slow-the-fuck-down/)
- In response to this article: [What I Wish I Knew When I Started My Career as a Software Developer](http://lifehacker.com/what-i-wish-i-knew-when-i-started-my-career-as-a-softwa-1681002791)
- "timeframes that seem absurdly bloated beforehand tend to look reasonable, even respectable, at the end of a project"
- "projects fail far more often because the software never really works reliably than because they missed a tight market window"
- "with all the details and pitfalls and tangents in plain sight, you can see that that the initial estimate was hopelessly unrealistic"

### [How to be a great software developer](http://peternixey.com/post/83510597580/how-to-be-a-great-software-developer)
- "Your value as a developer is measured not in the height of your peaks, but the area under your line"
- "Go deep before you go wide - learn your chosen stack inside out"
- "Learn to detect the smell of bad code"
- "Check and re-check your code. Your problems are yours to fix"
- "Write up the things you’ve done and share them with the team"
- "Understand and appreciate the exquisite balance between too much testing and too little"
- "Make your team better"
- "Your contribution as a developer is defined not by the abstraction of how smart you are or how much you know. It’s not defined by the technology acronyms on your resume, the companies you’ve worked at or which college you went to. They hint at what you’re capable of but who you are is defined by what you do and how that changes the project and the people around you."

### The Great TDD Debate of 2014
- DHH: [TDD is dead. Long live testing.](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html)
- Uncle Bob: [Monogamous TDD](http://blog.8thlight.com/uncle-bob/2014/04/25/MonogamousTDD.html)
- DHH: [Test-induced design damage](http://david.heinemeierhansson.com/2014/test-induced-design-damage.html)
- Uncle Bob: [When TDD doesn't work.](http://blog.8thlight.com/uncle-bob/2014/04/30/When-tdd-does-not-work.html)
- DHH: [Slow database test fallacy](http://david.heinemeierhansson.com/2014/slow-database-test-fallacy.html)
- Gary Bernhardt: [TDD, Straw Men, and Rhetoric](https://www.destroyallsoftware.com/blog/2014/tdd-straw-men-and-rhetoric)
- Uncle Bob: [Test Induced Design Damage?](http://blog.8thlight.com/uncle-bob/2014/05/01/Design-Damage.html)
- Uncle Bob: [Professionalism and TDD (Reprise)](http://blog.8thlight.com/uncle-bob/2014/05/02/ProfessionalismAndTDD.html)

### [Remote-First Communication for Project Teams](http://spin.atomicobject.com/2015/01/30/remote-first-communication/)
- "remote-first communication means preferring written, searchable methods of communication that work even when the sender and receiver aren’t engaged at the same time"
- "Remote-first communication does not mean that your only communication should be written."

### [The economics of software correctness](http://www.drmaciver.com/2015/10/the-economics-of-software-correctness/)
- "Users have stated the price that they’re willing to pay, and that price does not include correctness, so they’re getting software that is not correct. I think we all feel bad about shipping buggy software, so let me emphasise this here: Buggy software is not a moral failing. The option to ship correct software is simply not on the table, so why on earth should we feel bad about not taking it?"
- "The result is long and frustrating conversations with users in which you try to determine whether what they’re seeing is actually a bug or a misunderstanding (although treating misunderstandings as bugs is a good idea too), trying to figure out what the actual bug is, etc. It’s a time consuming process which ends up annoying the user and taking up a lot of expensive time from developers and customer support."
- "At the same time, your users are a lot more effective at finding bugs than you are due to sheer numbers if nothing else, and as we’ve established it’s basically impossible to ship fully correct software, so we end up choosing some level of acceptable defect rate in the middle. This is generally determined by the point at which it is more expensive to find the next bug yourself than it is to let your users find it. Any higher or lower defect rate and you could just adjust your development process and make more money, and companies like making money so if they’re competently run will generally do the things that cause them to do so."
- "But one thing that won’t improve your ability to find bugs is feeling bad about yourself and trying really hard to write correct software then feeling guilty when you fail. This seems to be the current standard, and it’s deeply counter-productive. You can’t fix systemic issues with individual action, and the only way to ship better software is to change the economics to make it viable to do so."
