### thoughts on functional components
[See: javascript-inside](https://medium.com/javascript-inside/some-thoughts-on-function-components-in-react-cb2938686bc7)
* __Clear separation of logic and view.__ View functions should always be simple functions by default.
 * container - logic / presentation - view
* The absence of any methods or setState __enforces thinking about application state early on__.
 * lift state up
* __Functions should either be concerned with logic or presentation__. This helps to add focus.
* Testable: __view functions make it easier to test__, as there is no logic involved. The view only renders according to the passed in props, no need to recreate a certain state to be able to test the component.
* Focus on reusability but start out large if necessary. __Abstracting early on and hitting the wrong abstraction is harder to revert than the other way round__.
* Use Recompose, __Ramda__, lodash etc.
* Use __Higher Order Components__ for pure render optimization and local state handling when possible.
 * render props
* In an ideal setup we could even __use advanced testing techniques like property-based testing__ as we’re only working with stateless functions.
* __Use flowtype or propTypes__ whenever possible.
* __Documentation__ is easier when components are small.
