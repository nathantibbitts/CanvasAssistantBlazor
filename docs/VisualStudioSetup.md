# Visual Studio Setup
The following is an explanation of how to set up Visual Studio for the SDEV 1090 - Session 10 - Final Competency Assignment.

## Using DTC Computers
If you are using the computers in the DTC Software Development lab, no further steps are required to setup Visual Studio.  Please continue to [How To Launch the Solution](#how-to-launch-the-solution).

## Using a Personal Computer
If you are using a personal Windows computer instead of a DTC computer, please follow these steps.

> It is *highly* recommended that Visual Studio be used for this project.  Visual Studio Code will not work.

1. Navigate to the [Visual Studio Webpage](https://visualstudio.microsoft.com/downloads/) and download the 2022 Community version.

![Visual Studio Download Webpage](/docs/screenshots/VisualStudioDownload.jpg)

2. Launch the downloaded file when is has finished and walk through the installation wizard to install Visual Studio Installer.
3. When you start to select your workloads, select the **ASP.NET and web development** and click **Install** (not shown in the image below).

![Visual Studio Workload Installation](/docs/screenshots/VsWorkloads.jpg)

4. After the installation has completed, open command prompt.  Type:
``` terminal
dotnet --info
```

5. Review the results.  If it says:
+ Your architecture is *x86*
+ There are no SDKs found
+ Paths are to Program Files (x86)

![Visual Studio Workload Installation](/docs/screenshots/cmd86.jpg)

Then, continue to [Change Visual Studio from x86 to x64](#change-visual-studio-from-x86-to-x64).

If it says:
+ Your architecture is *x64*
+ There are some SDKs found
+ Paths are to Program Files

![Visual Studio Workload Installation](/docs/screenshots/cmd64.jpg)

Then continue to [How to Launch the Solution](#how-to-launch-the-solution).

### Change Visual Studio from x86 to x64
If your computer has a x64 bit based architecture, that is the version that of Visual Studio that would have been installed on your computer.  If your computer is pointing to the x86 version, it will not recognized that you have any SDKs installed.  These steps explain how to change which version Visual Studio looks at.

1. Click the Start button and open the **Control Panel**.

![Windows Start Menu Search Control Panel](/docs/screenshots/ControlPanel.jpg)

2. Click on **System**.

![Control Panel Page](/docs/screenshots/System.jpg)

3. On the right hand side, click on Advanced system settings.

![System Properties Page](/docs/screenshots/AdvancedSystemSettingssmall.jpg)

4. Click on the **Environment Variables** button on the bottom.

![Advanced System Settings Page](/docs/screenshots/EnvironmentVariablessmall.jpg)

5. Under the *System variables* on the bottom half of the screen, click **Path** and click **Edit**.

![Environment Variables](/docs/screenshots/SystemVariablessmall.jpg)

6. Look for `C:\Program Files (x86)\dotnet\` and `C:\Program Files\dotnet\`.  The x86 should be above the other.

![Edit Path Variable screen](/docs/screenshots/Path86Abovesmall.jpg)

7. Move `C:\Program Files\dotnet\` so that it is above `C:\Program Files (x86)\dotnet\` using the **Up** and **Down** buttons on the right.  When finished, click **OK** on all open windows until you get back to the *System* screen, which can be closed.

![Edit Path Variable screen](/docs/screenshots/Path86Belowsmall.jpg)

Continue to [How to Launch the Solution](#how-to-launch-the-solution).


## How To Launch the Solution
Please follow these steps to launch the solution file (.sln).

1. Click the Start button and open **Visual Studio 2022**.
2. Click the open a project or solution button.

![Visual Studio Launch Window](/docs/screenshots/VSOpenProjectsmall.jpg)

3. Navigate to your cloned repo and find the **CanvasAssistantBlazor.sln** file.
> Alternatively you can navigate to the .sln file in your File Explorer and double click it

4. Once the project loads, click the green arrow with "https" next to it at the top of the window.

![Visual Studio Run Solution Window](/docs/screenshots/InitialVSLoad.jpg)

5. You may be prompted to install some certificates.  Click **Yes** when they appear.

![ASP.NET Core Certificate Installation Prompt](/docs/screenshots/ASPnetCoreCertificatessmall.jpg)

You may also receive a warning when attempting to install the certificates.  Again, click **Yes** to continue.

![ASP.NET Core Certificate Installation Warning](/docs/screenshots/ASPnetCoreSecurityWarningsmall.jpg)

6. You default browser should open.  If you are presented with a certificate warning, press Advanced and Accept the certificate to continue.

![CanvasAssistantBlazor Webpage Certificate Warning](/docs/screenshots/WebpageCertificateError.jpg)

7. The webpage should then load.

![CanvasAssistantBlazor Webpage](/docs/screenshots/CanvasAssistantBlazorWebpagesmall.jpg)
![CanvasAssistantBlazor Webpage](/docs/screenshots/CanvasAssistantBlazorWebpageCountersmall.jpg)

[Return to README](/README.md)