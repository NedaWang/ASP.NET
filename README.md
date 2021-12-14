# ASP.NET
ASP: Active Server Pages, predecessor of ASP.NET
.NET framework: foundation that ASP>NET is built on. It provides consistent development experience.
ASP.NET Core: Support other OS like Mac OS and Linux.
ASP.NET Web Api: RESTful HTTP services built by ASP.NET framework. It can serialize a model into formats like JSON and XML, and then it outputs it into the HTTP response.

NuGet packages have consume reusable code, we need to use NuGet package restore to restore them: right click solution file -> restore NuGet Packages.

### Web forms: Event-Driven development, stateless execution
Web Forms provide a suite of web server controls to build your applications. This includes controls that are similar to HTML elements like text inputs and buttons. There are also some more complicated controls that connect to data sources and handle data access. You don't have to worry about creating HTML or dealing with the interaction between the browser and the server. You can then set UI properties and events for the controls. You can then set UI properties and events for the controls. View State preserves state over roundtrips to server, when the page posts back to the server, the contents of Viewstate are also sent along. To disablt it we can set "ViewSateMode" to asp elements in aspx, or set in page directive <%@ %> to disable it for emtire page. Remember that the purpose of Viewstate is to store page specific values.
We can store the application specific values in global storage called application state. This is used for data that's shared by multiple user sessions and doesn't change that often.

- Default.aspx: first UI
- Defult.aspx.cs (code behind): This is where you'd write programming logic for the page, like event handlers and other server-side code.
- Site.Master: This is an ASP.NET master page. It's where you define a consistent appearance for all the pages in your application, such as navigation.
- Global.asax: This is where you'd find code to handle application and session-level events raised by ASP.NET

- Content folder: Bootstrap is a layout and theme-ing framework from Twitter. It provides responsive design capabilities, which means the layout can adapt to different browser window sizes. You can build one application that can dynamically adjust to display on desktop, tablet, and mobile devices.
- Scripts folder:  Jquery is a Javascript library that allows you to traverse HTML documents and handle client-side events.
- Web.config: Settings like database connection strings and authentication modes are typically managed here.
- runat="server"attribute on both head and form elements, when we add this to an HTML tag, it becaomes an HTML server control. We can then easily access and modify it's properties on the server side.
- load event: part of page lifecycle. It's raised every time a request is made to the page and when the page is posted back to the server like when the Submit button's clicked.
- page_load method:  event handler for the load event.

### Web pages:add dynamic code to HTML pages
That code is written in C# or VB.NET using a markup syntax called Razor. Razor pages written in C# end in .cshtml, and VB.NET pages have the extension .vbhtml. You can do anything you'd normally be able to do in an HTML page, like add JavaScript or jQuery.
-  @{...}, @variable, so they can be displayed without being interpreted as HTML. Even though we're inside a code block, we can go right back to writing HTML markup.
-  set start up project, set start up page.
-  Layout pages(_SiteLayout): place common content that's shared across the site. In its head include third party library, like JQuery, so we don't need to include it in all other single pages. In its body, we can put logo in hearder and design footer, also we can check authentication, and base on that, display different menu items.
-  Render Section Method: is how you render a named section that's defined in a content page. The second parameter, Required, is set to false. That means the section can be ignored if it's not defined in the content page.

### MVC
- model: data, handle business logic.
- view: UI, take info from model and show to user.
- controller: get user input from view and pass result back to the view with the help of model.
- action: The public methods that are defined within the controllers are called actions, like the index action.
- by default, if the view method is called with no parameters, the view name would be the same as the action name.

### Web Api
ASP.NET Web API can serialize a model into formats like JSON and XML, and then it outputs it into the HTTP response.
- App_Start -> WebApiConfig.cs routeTemplate
- find url from app property, then add /api/{controller_name}
