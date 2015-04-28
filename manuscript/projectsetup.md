#Project or Solution Setup

Base App.xaml:
```
<Application x:Class="CodeBehind.App"
             xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             StartupUri="MainWindow.xaml">
    <Application.Resources>

    </Application.Resources>
</Application>
```

After bringing in the control styles:
```
<Application x:Class="CodeBehind.App"
             xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             StartupUri="MainWindow.xaml">
    <Application.Resources>
        <ResourceDictionary>
            <ResourceDictionary.MergedDictionaries>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/themes/dialogs/BaseMetroDialog.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/controls.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/controls.buttons.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/FlatButton.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/fonts.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/colors.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/sizes.xaml"></ResourceDictionary>

                <!-- Will insert default style and color scheme here -->

                <ResourceDictionary Source="pack://application:,,,/CodeBehind;component/Resources/Icons.xaml"></ResourceDictionary>
            </ResourceDictionary.MergedDictionaries>
        </ResourceDictionary>
    </Application.Resources>
</Application>
```

###Color Scheme and Base Color Usage

Mahapps uses two base color usage patterns:

 * Light (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/BaseLight.xaml`)
 * Dark (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/BaseDark.xaml`)

Along with several color schemes:
 * Amber (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Amber.xaml`)
 * Blue (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Blue.xaml`)
 * Brown (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Brown.xaml`)
 * Cobalt (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Cobalt.xaml`)
 * Crimson (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Crimson.xaml`)
 * Cyan (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Cyan.xaml`)
 * Emerald (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Emerald.xaml`)
 * Green (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Green.xaml`)
 * Indigo (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Indigo.xaml`)
 * Lime (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Lime.xaml`)
 * Magenta (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Magenta.xaml`)
 * Mauve (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Mauve.xaml`)
 * Olive (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Olive.xaml`)
 * Orange (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Orange.xaml`)
 * Pink (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Pink.xaml`)
 * Purple (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Purple.xaml`)
 * Red (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Red.xaml`)
 * Sienna (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Sienna.xaml`)
 * Steel (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Steel.xaml`)
 * Taupe (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Taupe.xaml`)
 * Teal (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Teal.xaml`)
 * Violet (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Violet.xaml`)
 * Yellow (`pack://application:,,,/MahApps.Metro;Component/Styles/Accents/Yellow.xaml`)

It seems as if the preferential order to insert the base light/dark accent; along with the color scheme is after the "styles" xaml documents, but before the Icons reference.  For completeness, let's use {TBD} below:

```
<Application x:Class="CodeBehind.App"
             xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
             xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
             StartupUri="MainWindow.xaml">
    <Application.Resources>
        <ResourceDictionary>
            <ResourceDictionary.MergedDictionaries>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/themes/dialogs/BaseMetroDialog.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/controls.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/controls.buttons.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/FlatButton.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/fonts.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/colors.xaml"></ResourceDictionary>
                <ResourceDictionary Source="pack://application:,,,/MahApps.Metro;component/styles/sizes.xaml"></ResourceDictionary>



                <ResourceDictionary Source="pack://application:,,,/CodeBehind;component/Resources/Icons.xaml"></ResourceDictionary>
            </ResourceDictionary.MergedDictionaries>
        </ResourceDictionary>
    </Application.Resources>
</Application>
```

### Custom Colors and Styles
Now, this is a WPF application afterall. You do not need to use the light/dark accents, nor do you need to use every styles/* reference from the above examples.  You are completely free to customize each control to suit your exact need for your application.
