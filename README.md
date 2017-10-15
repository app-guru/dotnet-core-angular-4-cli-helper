# dotnet-core-angular-4-cli-helper

#### STEP-1 : Add bellow ItemgGroup on your \<project-name\>.csproj for run & debug 

```
  <ItemGroup>
    <PackageReference Include="Microsoft.AspNetCore.Hosting.Abstractions" Version="1.1.3" />
    <PackageReference Include="Microsoft.AspNetCore.Http.Abstractions" Version="1.1.2" />
    <PackageReference Include="Microsoft.AspNetCore.Http.Extensions" Version="1.1.2" />
    <PackageReference Include="Microsoft.Extensions.Options" Version="1.1.2" />
    <PackageReference Include="Newtonsoft.Json" Version="10.0.3" />
    <PackageReference Include="System.Diagnostics.Process" Version="4.3.0" />
    <PackageReference Include="AppGuru.AspNetCore.AngularCLI" Version="1.0.1" />
  </ItemGroup>
```

#### STEP-2 : Add bellow Target on your \<project-name\>.csproj for publish
```
  <Target Name="PrepublishScript" BeforeTargets="PrepareForPublish">
    <Exec Command="ng build --prod" />
  </Target>
```

#### STEP-4 : Run `dotnet restore`

#### STEP-5 : Add bellow code on your Startup.cs
```csharp
  if (env.IsDevelopment())
  {
    app.UseNgProxy();
  }
```

#### STEP-6 : Hit F5 for Debug 


### For realtime sample
[dotnet-core-angular-4-cli](https://github.com/app-guru/dotnet-core-angular-4-cli)

### Credit & Thanks to
[andfomin-NgProjectTemplate](https://github.com/andfomin/NgProjectTemplate)
