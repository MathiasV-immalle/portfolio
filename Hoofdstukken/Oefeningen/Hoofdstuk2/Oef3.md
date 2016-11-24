# Oefening 2.3: MessageBox gebruiken

## XAML

```
<Window x:Class="WPFOef2._3MessageBox.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:WPFOef2._3MessageBox"
        mc:Ignorable="d"
        Title="MainWindow" Height="350" Width="525">
    <Grid>
        <Button x:Name="button" Content="Button" HorizontalAlignment="Left" Margin="10,10,0,0" VerticalAlignment="Top" Width="75" Click="button_Click"/>

    </Grid>
</Window>
```

#### Dit maakt hetgeen deze afbeelding weergeeft.

![afbeelding](https://github.com/MathiasV-immalle/portfolio/blob/master/AfbeeldingenGithub/Oef2.3/2016-11-11%2009_57_37-WPFOef2.3MessageBox%20-%20Microsoft%20Visual%20Studio.png)

## Eventhandlers

```
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace WPFOef2._3MessageBox
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            MessageBox.Show("UwNaam");
        }

        private void button_Click(object sender, RoutedEventArgs e)
        {
            MessageBox.Show("UwLeeftijd");
        }
    }
}
```

#### Deze code zorgt voor het effect dat deze afbeeldingen weergeven indien:

##### ctrl + F5 om het programma te starten worden ingedrukt

![UwNaam](https://github.com/MathiasV-immalle/portfolio/blob/master/AfbeeldingenGithub/Oef2.3/2016-11-11%2009_59_25-.png)

##### De eerste MessageBox wordt gesloten

![MainWindow](https://github.com/MathiasV-immalle/portfolio/blob/master/AfbeeldingenGithub/Oef2.3/2016-11-11%2009_59_47-MainWindow.png)

##### De button-knop wordt ingedrukt.

![UwLeeftijd](https://github.com/MathiasV-immalle/portfolio/blob/master/AfbeeldingenGithub/Oef2.3/2016-11-11%2010_00_08-.png)
