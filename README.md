# AzurePipelinesTest3
AzurePipelines Example project to show build errors for net35 and uap10


## net35
Errors are solved by adding this in the csproj:
``` xml
<!-- https://github.com/Microsoft/msbuild/issues/1333 -->
<PropertyGroup Condition=" '$(TargetFramework)' == 'net35' ">
    <!-- <FrameworkPathOverride>C:\Program Files (x86)\Reference Assemblies\Microsoft\Framework\.NETFramework\v3.5\Profile\Client</FrameworkPathOverride> -->
    <FrameworkPathOverride>C:\Program Files (x86)\Reference Assemblies\Microsoft\Framework\.NETFramework\v4.6.2</FrameworkPathOverride>
</PropertyGroup>
```

## uap10
TODO
