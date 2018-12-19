
See the Settings folder for the latest Rider and VS settings.

## Visual Studio

### Settings

Open the "Tools > Options" window and search for the following key words:

- "Diagnostic tools" Debugging = disable
- "UI Debugging Tools for XAML" Debugging = disable
- "XAML Designer" = disable
- "Scroll Bars" Use map mode for vertical scroll bar = enable

- Debugging > Symbols > Cache symbols in this directory = C:\Source\_symbols
- Debugging > General > Enable Just My Code = disable
- Debugging > General > Enable source server support = enable
- Text Editor > General > Show Structure guide lines = disable (we will use Indent Guides extension instead.)

### Add Nuget Package sources

- Copy NuGet.Config file from %appdata%\NuGet
- When restoring packages for the first time disable the NuGet source and use MyGet. Once all the Orc.* libraries have been restored then enable NuGet source and re-build solution.

### Extensions

NOTE: Login to Visual Studio and then go to "Tools > Extensions and Updates > Roaming Extension Manager" and install extensions from there.

Don't really need Resharper when using VS-Preview with these extensions:

- [Working File List](https://marketplace.visualstudio.com/items?itemName=Ant-f.WorkingFilesList)
  - Options > Working Files List > General > Document display order = Recent
- [Region Expander](https://marketplace.visualstudio.com/items?itemName=DavidPerfors.RegionExpander)
- [CodeNav](https://marketplace.visualstudio.com/items?itemName=SamirBoulema.CodeNav)
- [Output Enhancer](https://marketplace.visualstudio.com/items?itemName=NikolayBalakin.Outputenhancer)
- [Trailing White Space](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.TrailingWhitespaceVisualizer)
- [Word Highlight With Margin](https://marketplace.visualstudio.com/items?itemName=TrungKienPhan.WordHighlight-18439)

#### Testing:

- [Switch Startup Project](https://marketplace.visualstudio.com/items?itemName=vs-publisher-141975.SwitchStartupProjectforVS2017)
- [Microsoft Code Analysis 2017](https://marketplace.visualstudio.com/items?itemName=VisualStudioPlatformTeam.MicrosoftCodeAnalysis2017)
- [Sharpen](https://marketplace.visualstudio.com/items?itemName=ironcev.sharpen)
- [Indent Guides](https://marketplace.visualstudio.com/items?itemName=SteveDowerMSFT.IndentGuides)
  - Default.Highlight Style = Solid (thick)
  - Unaligned.Visible = False
  - #0.Visible = True
  - Highlighting > Select "Current block"

#### Keep an eye on:

- [Quick Diagram Tool for C#](https://marketplace.visualstudio.com/items?itemName=FerencVizkeleti.QuickDiagramToolforC)

#### Removed:

- [Productivity Power Tools](https://marketplace.visualstudio.com/items?itemName=VisualStudioProductTeam.ProductivityPowerPack2017) (I don't think this adds much anymore when using the VS=Preview)
- [IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.VSIntelliCode) (Good concept but it did not really make a big difference)
- [Viasfora](https://marketplace.visualstudio.com/items?itemName=TomasRestrepo.Viasfora) (Colors are hard to see)
- [Code Graph](https://marketplace.visualstudio.com/items?itemName=YaobinOuyang.CodeAtlas) (Not very intuitive)

## Rider

Has a lot of good stuff already backed in. Don't need nearly as many plugins or extensions.

### Extensions

- [Code Glance](https://plugins.jetbrains.com/plugin/7275-codeglance)