---
layout: post
title:  "Is it too early to use framework agnostic Web Components?"
date:   2017-10-17 14:33:37 -0500
description: We all understand why creating components, web or otherwise, is easier when using an existing framework. You know what the framework does...
---
We all understand why creating components, web or otherwise, is easier when using an existing framework. You know what the framework does, and you usually have ideas about how to extend it for the purpose at hand, without having to write the code from scratch. Frameworks are designed to be universal, reusable and adaptable for a reasonable range of uses.

However, not all is rosy with this picture. By adopting a framework, you automatically introduce a dependency on it. Porting the app to another framework can be complex and lengthy, especially if your components started life inside jQuery, Backbone, Angular, Ember or any of the other relatively complex but popular frameworks. Transitive dependencies can add up fast. As well, sticking within the framework you started with will mean you reach a point where one requested change means having to alter all occurrences of the same code. Maintaining templates of controllers and components would also require resources, although many IDEs are making it easier to propagate changes throughout your environment.

Other difficulties arise when your preferred framework puts out a major new release. The transition of AngularJS to Angular is a good example of this, as it showed that such a migration requires additional time and effort to make sure that all your components will work in the new environment. Finally, if you were looking for a new component for a specific task, and found one that would do exactly what you need, unless it was created in the same framework, you may be better off creating your own rather than trying to port it over.

What strategy would work better? Building components that have no knowledge of which Document Object Model (DOM) builder they’re using is one possible solution. The DOM interface for application programming is cross-platform and language-independent, making it possible to bundle all easily abstracted functionality into a single object. No real dependencies are created, and the single object can be easily changed at any time.

Ensuring a separation of component behaviour and the framework implementation is similar in many ways to the practice of domain-driven design. And if we take this argument a step further by separating behaviour and state, we would be able to write components in a purely functional way. Examples of this are Mithril.js, Mercury, Hyperscript and Vue.js.

While all of this sounds obvious in theory, implementation might be too costly at any particular time in the project lifecycle. For one thing, long-term support would be difficult if lax rules allow developers to mix frameworks within a project. And, depending on your framework’s complexity, you might have to bear an initial cost for developing a facade for the framework.

Adoption of framework agnostic components has been slow. There’s still a lot to learn, and it’s hard to find good articles about it. For example, although using Redux will definitely helps in the separation of state, developers are still coding in such a way as to make Angular appear as a first-class citizen. If your component logic is just a JavaScript object that Angular uses, the bindings and infrastructure are still in Angular. Another hurdle to overcome is that different frameworks handle data flow differently, depending on whether they’re using events, two-way bindings, or one-way data flow with actions back up.

There has been progress. One example is web components that are now part of the platform. If you start using a platform that comes with built-in components, you can expect that the components will work, reducing your testing requirements and allowing you to move on to more specialized work. Having platform components also reduces the need for frameworks, at least as far as simple components go.

Overall, we hope that framework agnostic components become more popular and that a greater user community gets behind them with support and examples. It would be great to reduce our attachment to specific frameworks, but that day might be further ahead than we think. In the meantime, it may be worth investigating and considering concepts from domain-driven design when developing web components to reduce the long-term maintenance cost:

Separate the core domain/business logic into a separate JavaScript class/package
Create web component classes following the W3C specification that encapsulates the behaviour and lifecycle of the component
When using a framework, create components that wrap the native W3C web component interface linking the appropriate lifecycle and behaviours
By considering these ideas, it will allow the web components to eventually shed the framework and allow for a lower overhead by leveraging the native browser functionality. As an added bonus, it would allow for the creation of a framework agnostic component catalogue that could be reused across projects. The interfaces between the desired framework and the native web component could also be potentially reusable. In this manner of development, one can achieve maintainability, readability, and flexibility.
