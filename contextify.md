[clypd/Xandr](https://www.xandr.com/) is using Go since 2013. At that time `context` package was not readily available in stdlib even if it was getting used inside Google. But as Go ecosystem matured `context` came in stdlib and many libraries started supporting it too. We also wanted to update all of our old code that was not using `context`. Changing whole code manually was tedious and not fun. So we decided to use Go's code parsing and code generation capabilities to write a tool to make our code context aware.

Code of `contextify` is not in a public domain, but it is easy enough to build if someone needs it. Putting this small post here with the [presentation](blog/contextify.pdf) that I gave in local Go meetup so that I don't loose it.