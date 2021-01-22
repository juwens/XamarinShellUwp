#WPF

https://dev.to/krdmllr/setting-up-a-xamarin-forms-wpf-backend-on-net-core-109l

# Errors

## ShellNavigationView:
```
Cannot find a resource with the given key: ShellNavigationView.
```

ShellNavigationView + UWP is only supported for Xamarin.Forms >= 5.0

see: https://github.com/xamarin/Xamarin.Forms/issues/11505

## wpf

```
App.xaml : error :  : XamlC error XFC0000 : Cannot resolve type "Application".
```

Solution:
Add this to csproj
```
    <ItemGroup>
        <EmbeddedResource Remove="**\*.xaml" />
    </ItemGroup>
```