# Svelte iUX - Component Library

WORK IN PROGRESS - no useful code here yet!

**Svelte incremental UX (iUX)** is a library of experimental web components being used to explore ideas for improving the UX of a complex application: [Visualisation Lab](https://github.com/theWebalyst/visualisation-lab).

iUX components are created for use with the Svelte web framework and in a specific application, but the will I hope be transferrable, hence putting them in a library from the start.

#### Join The Discussion
I welcome discussion of the vision (below) and any collaboration on ideas, testing and code. So feel free to open an issue with questions or contributions of any kind.

#### Svelte and Svench
This component library uses **Svench**, an experimental workbench for building **Svelte** components, and was made by taking a copy of the [svench/example](https://github.com/rixo/svench/tree/master/example) directory and modifying that.

# Svelte iUX Vision

None of this is code yet, it has literally just emerged from my head. I haven't even drawn any pictures except in my head (sorry!).

## Revealer Controls

**Svelte incremental UX (iUX)** provides a set of 'revealer controls' as Svelte
components. The idea is that by co-ordinating these controls you can build a UI
which 'unfolds' the story or workflow of an application incrementally for the
novice user, without impeding the expert.

### iUX Aims and Approach

For the new user, the approach is to reduce complexity and introduce 
features gradually, avoid overwhelm, increase retention and ease learning. The approach explored by iUX is to:

- Minimise the amount of information presented at any stage, keeping to what is
necessary for the current stage or to move onto a new stage or a different task.

- Reveal features in a way which guides and tutors, by showing controls and
optional follow on stages relevant to the current context and workflow stage.

- Unfold the application UI incrementally according to typical workflows,
re-enforcing the stories of different use cases, their relation to
application features and to the corresponding areas in UI.

- Give the user control over the process so they can move forward, back and
  around at their own pace, or dig deeper into the complexity of any stage.

- Ensure a knowledgable user can get directly to any feature and navigate
around the UI just as easily as if all the complexity were presented
at once in a user interface they know very well. 

Trying to cater for the novice and expert is particularly ambitious as if the former wasn't enough. So to make life a little easier the focus will be on helping the novice, while keeping catering for the expert in mind as an important longer term goal.

### Related UI Techniques

The above ideas aren't new, but I think are more ambitious in my conception than
the existing techniques that I'm aware of. I am though not up-to-date with state
of the art in this area, so only offer a couple of examples of current practice
and invite you to point out others to help inform or improve.

Two examples of current practiceare the 'Advanced' button which reveals
additional UI, and the 'Wizard' to guide through a procedure. These help, but
can't satisfy the ambtions of iUX as explained below!

#### Advanced`>` / `<`Hide
Some UIs reduce complexity and overload by showing only a subset of UI for
controlling a feature, and revealing more UI controls when the user clicks a
button such as 'Advanced'. This reveals additional UI, which can be hidden again
if desired. 

It is this simple idea which iUX builds on, and attempts to bring to an entire
application. The principle appears in other areas such as toolbars or menus which can be configured for simple or advanced users and so on. But ironically this can add to complexity at the same time, and create problems when an option is hidden from the novice rather than offered at just the point they might be ready to learn about it.

In iUX, the idea is to do this in a way which is intuitive for a new user and
facilitates learning the application's capabilities, workflows, and UI
structures. And to do so without getting in the way once this has been fully
understood.

#### Wizard Dialog
Another technique which I think has been around even longer than Advanced/Hide
is the Wizard Dialog: a sequence of pages with 'Next' and 'Back' buttons. 

A Wizard is useful for configuring a feature or initiating a task with complex
starting conditions. But a Wizard is also limiting and restrictive so only
useful for subsets of a complex application. This doesn't work well in
applications with multiple features which are intended to be used in
combination, which is an example of the extra yard that iUX is going for.

## Techniques:
Some embrionic ideas for techniques that I think will help support the aims of iUX:

- Use transitions when expanding or contracting, revealing or hiding, which
minimise disruption to the rest of the UI, and so to the user's mental
model of the system. For example, by not re-arranging existing controls or areas except for specific purposes, see next.

- Rearranging is necessary at certain points in a dynamic, unfolding UI, but it can also be useful. For example as a signal that a new stage in the story is being revealed rather then a step made within the current stage. It may be a signal of completion, and for a well earned pause with an implied pat on the back. And still a rearrange must be done with minimum disruption to the status quo. There's a whiff of gamification here, but for now I don't plan to use that approach overtly because iUX philosophy is to enable choice rather than impose a direction.

- Provide subtle, consistent visual clues which reflect the stages, such as
shades or boundaries separating areas of incremental change, rather than
simply adding to a homogenous controls area.

I welcome discussion and comment on any aspect of iUX, so feel free to open an issue for that, or to ask a question etc.

## Using Svench

Svench is at this time still a proof of concept and so subject to change, but
some basics on using it are included below. For latest information on Svench or
more details on the configuration files see the [Svench
github](https://github.com/rixo/svench/).

### Prerequisites
- `node` v12

This project has a `.nvmrc` file for use with `nvm` to select `node` version which can be used as below:

### Setup
```bash
git clone https://github.com/theWebalyst/svelte-iux.git
cd svelte-iux
nvm use
yarn
```

### Start Svench

```bash
yarn svench
```

Open http://localhost:4242. Edit / add things in `./src`.

### Using Svench

Each component has a '.svench' file next to the '.svelte' component file, and this file is used by Svench to create its menu, and provide the context for
displaying and interacting with the component.

For more on these, see the [Svench README](https://github.com/rixo/svench/).

## LICENSE
See LICENSE. 

TL;DR:
- **Svelte iUX** Compnents are under GPLv3
