[Sandi Metz’ rules for developers](http://robots.thoughtbot.com/post/50655960596/sandi-metz-rules-for-developers)
- Classes can be no longer than one hundred lines of code.
- Methods can be no longer than five lines of code.
- Pass no more than four parameters into a method. Hash options are parameters.
- Controllers can instantiate only one object. Therefore, views can only know about one instance variable and views should only send messages to that object `@object.collaborator.value` is not allowed).
