🎯 Overview

ToastBlazor is a modern toast notification system for Blazor Web Apps.
It is built entirely in C# + Razor, with zero JavaScript, and provides a clean, customizable, theme‑ready UI.

✔ Light & Dark themes

✔ Minimal & Outline themes

✔ Custom SVG icons

✔ Infinite toasts

✔ Progress bar

✔ Smooth animations

✔ Configurable positions

✔ No dependencies

📦 Installation

Install via NuGet:
```bash

dotnet add package ToastBlazor
```
Or via Visual Studio → Manage NuGet Packages.

⚙️ Setup
1. Register the service

In Program.cs
```csharp
  builder.Services.AddToastBlazor();
```
2. Add the container
In MainLayout.razor
```csharp
  <ToastContainer />
  @Body
```
3. Inject the service where needed
```csharp
  @inject IToastService Toast
```
🎨 Stylesheet

Add the ToastBlazor CSS file:
```html
<link rel="stylesheet" href="_content/ToastBlazor/Styles/toastblazor.css" />
```
🔥 Usage Examples

Success toast
```csharp
  Toast.Success("Profile updated successfully!");
```
Error toast
csharp

Toast.Error("Something went wrong.");

Custom duration
```csharp
  Toast.Show("Saved with delay", ToastLevel.Info, 5000);
```
Infinite toast
```csharp
  Toast.ShowInfinite("Waiting for server...", ToastLevel.Warning);
```
Custom icon (SVG)
```csharp
  Toast.Show("Custom icon", ToastLevel.Success, "<svg>...</svg>");
```
Full custom toast
```csharp
  Toast.Show(new ToastMessage
  {
      Message = "Fully custom toast",
      Level = ToastLevel.Info,
      Duration = 8000,
      Theme = ToastTheme.MinimalOutline,
      Animation = ToastAnimation.Zoom,
      CustomIcon = "<svg>...</svg>"
  });
```
🎨 Theming
Light (default)
```razor
  <ToastContainer Theme="ToastTheme.Light" />
```
Dark
```razor
  <ToastContainer Theme="ToastTheme.Dark" />
```
Minimal
```razor
  <ToastContainer Theme="ToastTheme.Minimal" />
```
Minimal Outline
```razor
  <ToastContainer Theme="ToastTheme.MinimalOutline" />
```
📍 Positioning
```razor
  <ToastContainer Position="ToastPosition.BottomRight" />
```
Available positions:

    TopLeft

    TopRight

    BottomLeft

    BottomRight

📊 Progress Bar

Enabled automatically for timed toasts:
```csharp
  Toast.Show("Auto dismiss in 3s", ToastLevel.Info);
```
Disable globally:
```razor
  <ToastContainer ShowProgressBar="false" />
```
🧪 Demo Project

A full demo is available here:

👉 https://github.com/alain-mathy/ToastBlazorDemo

Includes:

    Basic toast examples

    Success / Error / Info / Warning

    Theme switching

    Positioning

    Custom icons

    Infinite toasts

    Progress bar

    Animations

🛣️ Roadmap

    [ ] Queued toasts

    [ ] Swipe‑to‑dismiss

    [ ] Accessibility improvements

    [ ] Auto‑theme (match system dark/light)

🤝 Contributing

Pull requests are welcome.
If you want to add themes, animations, or features, feel free to open an issue.
📄 License

MIT License.
