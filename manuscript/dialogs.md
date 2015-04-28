#Dialogs

##What is a dialog in regards to MahApps.Metro?

A dialog in MahApps.Metro is _almost_ synonymous to the old windows forms version of a dialog.  It allows the prompting the user for an input from a modal window, blocking further input on the screen.

The difference with MahApps Metro is that you get two styles:

###Metro Style

The Metro Style dialog window is an embedded control within your `<MetroWindow />` window.  Before being displayed, the `<MetroWindow />` applies a layer over the rest of the controls, at the `<MetroWindow />` level, so that you cannot interact with any of the window's controls until after you have performed the task within the dialog, and committed that work.

###Windows Forms Style

In the windows forms style, there is a new physical window that is created and is floated above the main `<MetroWindow />`.  All functionality you would expect from the Win32 dialog remains constant here.

##Other Considerations

Keep in mind, within the WPF infrastructure, whether you develop your front-end application in an MVP, M-V-VM, or code-behind pattern, the whole user interface is async, so you will be awaiting a command to come back from the Dialog before reacting to its result.

Without using an M-V-VM Framework, the code-behind \*.cs will look something like this:

```

```

###M-V-VM Implementations for a Dialog

####MVVMLight

####Caliburn Micro

####Prism
