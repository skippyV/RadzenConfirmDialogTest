This project was made with Visual Studio (2026) Blazor Web App template.
Target: .NET 10.0

Radzen.Blazor NuGet version: 9.0.5

Setup was done via https://blazor.radzen.com/get-started

Added following to _Imports.razor
	@using Radzen
	@using Radzen.Blazor
	
And the changes to App.razor	
  <RadzenTheme Theme="material" />
  <script src="_content/Radzen.Blazor/Radzen.Blazor.js?v=@(typeof(Radzen.Colors).Assembly.GetName().Version)"></script>
  
And Program.c
  builder.Services.AddRadzenComponents();
  
On the Home page I added the code for Radzen Dialog - Alert Dialog section
  https://blazor.radzen.com/dialog#alert-dialog
  
But the issue is that no Dialog ever appears. The Radzen buttons are all there but nothing happens.

And I also added this to top of Home page. 
   @rendermode InteractiveServer
   