# DotNet_Visibility_Internal_for_Tests
How to enable the tests to be able to use the internal classes from another assembly

```
<ItemGroup>
  <AssemblyAttribute Include="System.Runtime.CompilerServices.InternalsVisibleTo">
    <_Parameter1>Logic.Tests</_Parameter1>
  </AssemblyAttribute>
</ItemGroup>
```

Or Properties\AssemblyInfo.cs with:
```
using System.Runtime.CompilerServices;

[assembly:InternalsVisibleTo("MyTests")]
```
