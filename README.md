# ASP.NET
ASP: Active Server Pages, predecessor of ASP.NET
.NET framework: foundation that ASP>NET is built on. It provides consistent development experience.
ASP.NET Core: Support other OS like Mac OS and Linux.
ASP.NET Web Api: RESTful HTTP services built by ASP.NET framework. It can serialize a model into formats like JSON and XML, and then it outputs it into the HTTP response.

NuGet packages have consume reusable code, we need to use NuGet package restore to restore them: right click solution file -> restore NuGet Packages.

Web forms: Event-Driven development, stateless execution
Web Forms provide a suite of web server controls to build your applications. This includes controls that are similar to HTML elements like text inputs and buttons. There are also some more complicated controls that connect to data sources and handle data access. You don't have to worry about creating HTML or dealing with the interaction between the browser and the server. You can then set UI properties and events for the controls. You can then set UI properties and events for the controls. View State preserves state over roundtrips to server.
- Default.aspx: first UI
- Defult.aspx.cs (code behind): This is where you'd write programming logic for the page, like event handlers and other server-side code.
- Site.Master: This is an ASP.NET master page. It's where you define a consistent appearance for all the pages in your application, such as navigation.
- Global.asax: This is where you'd find code to handle application and session-level events raised by ASP.NET

- Content folder: Bootstrap is a layout and theme-ing framework from Twitter. It provides responsive design capabilities, which means the layout can adapt to different browser window sizes. You can build one application that can dynamically adjust to display on desktop, tablet, and mobile devices.
- Scripts folder:  Jquery is a Javascript library that allows you to traverse HTML documents and handle client-side events.
- Web.config: Settings like database connection strings and authentication modes are typically managed here.
