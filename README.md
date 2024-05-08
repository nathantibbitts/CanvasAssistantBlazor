# CanvasAssistantBlazor
This is the repo for the Final Competency Assignment in the SDEV 1090 - Version Control Fundamentals course.

![Davis Tech Logo](https://www.davistech.edu/media/tlmaw4xt/png-logo-horizontal_60.png)

This is a rebuild of a project used to help improve efficiency when grading assignments using Instructure's Canvas. The original, [Found Here](https://github.com/cdmccauley/canvasser),
was made using Next.js, while this rebuild uses Blazor. A running version of the old build can be found [here](https://canvasser.vercel.app/).
This project is currently a work in progress, and is not functioning.

## Getting Started
- Fork the repo: https://github.com/Davis-Technical-College/CanvasAssistantBlazor
- Clone the repo to your local machine from the fork.
- Check the Issues page on the original repo to see what may need work.

### Dependencies
Install [.NET SDK C#](https://dotnet.microsoft.com/en-us/download) extension on VS or Code Editor of choice.
- .NET SDK version 8.0 or higher, an earlier version will not run the program.
- C# extension on Visual Studio (preferred over VS Code) or another code editor of choice.

## Help
Ensure that you are running an updated Visual Studio or text editor, and an updated .NET SDK. Currently the program is using version 8.0. It wont run on an earlier version.

As of 2/28/2024 the only pages available are a 'Hello, world!' page with a counter that increments by 3, another counter page that increments by one, and a weather page using randomized placeholder data.

Information on how to setup Visual Studio on your own device can be found in the [Visual Studio Setup](/docs/VisualStudioSetup.md) docs.  It also has some information for running the project on DTC computers.

## Steps on running the program with Visual Studio
 1. When you open the folder, you will see many files. Open up "CanvasAssistantBlazor.sln" with Visual studio **2022** or **NEWER**.
 2. On the top of the screen. You will see **https** with a green arrow. Click on that to run the program (it may take a minute to run).
 3. Once the program opens up, it will ask to save certificates to you computer. You will require Admin privilege to install them. **This is normal!**
 4. The app will function without the certificates installed, but your connection will **not** be secure.
 5. Congrats, the app has opened!

## Steps to run the program on Fedora Linux:
1. Install the packages `dotnet-sdk-8.0` to be able to build the program, and `aspnetcore-runtime-8.0` to be able to run the server: `shell # dnf install dotnet-sdk-8.0 aspnetcore-runtime-8.0`.
2. Navigate to the project root. If it throws an error that says `Couldn't find a project to run...`, you simply aren't in the correct folder. You want to be in the folder with Program.cs and some json files, and NOT the folder labeled with "client" on the end. You want to build the server.
3. You can do this one of two ways:
    1. `dotnet run`. This has the advantage of building and running the executable in one step.
    2. `dotnet build` followed by `shell ./path/to/executable` once the build is complete.
4. You now have the server running. Connect to localhost:port_number. The terminal will log with a message saying `listening on port 5nnn`.

## License
This project is licensed under the MIT License - see the LICENSE.txt file for details.


## Credits
George Ray,
Joseph Plaizer,
Derek Mowry,
William Cummings,
Nathan Tibbitts