# D8S.E0007.Server


## Log

* Experimented with changing the server App.razor file to use a layout for the majority of its work.

Worked!

Layouts are just stupid.


* Added TailwindCSS

Used example from R5T.W0004.


* Changed server project from "D8S.E0007" to "D8S.E0007.Server"

This includes renaming the server project directory, and changing the project reference in the solution file.

This was far, far, FAR harder than it needed to be:

1. An unhandled exception appeared in the Chrome window.
This was because the default CSS file produced by the server, and referenced in the server's App component.
Changing the App to use the right URL ("D8S.E0007.Server.styles.css") fixed this.

See "Server Project Name Change – An unhandled error has occurred" in the Blazor notes file.

2. The Razor editor in the *client* project went haywire. Like, none of the Razor components could be found! And then the server couldn't find the client DLL (since it wasn't compiling).
Unclear what the reason was, but to fix it:
Just restarting Visual Studio *without* deleting the \.vs, \obj, and \bin directories. Somehow, Visual Studio then decided to recognize the new files.

See "Server Project Name Change – Razor Editor in client project no longer functional" in the Blazor notes file.
