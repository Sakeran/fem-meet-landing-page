# fem-meet-landing-page

This is a solution to the [Meet landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/meet-landing-page-rbTDS6OUR). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Notes

(October 18th, 2021)

With this project, I think I'm starting to get the hang of developing in Astro (and of component-based development in general). The implementation of this design was mostly straightforward, with one exception: the numbered headings preceding each of the two major sections.

When it came time to implement the numbered headings, I first designed them as standalone components that were completely agnostic to their sibling elements, assuming I could use properties like `gap` and `margin` to control the spacing. I did this using the first instance in the mockup as my template...but if I'd paid attention to the second instance, I'd have noticed that it overlaps its associated content, a scenario in which those properties are useless to me.

It wasn't hard to solve: I simply changed my `Divider` to a `WithDivider` component that accepts the associated content as its children. Implementing the overlap became a simple matter once the presence of associated content could be assumed. The resulting markup did *look* a little weird to me at first, but it's been a while since I've developed in this way, so I might just need to get used to it. Lesson learned.

[The live version of my solution may be found here.](https://grumpy-pail.surge.sh/)