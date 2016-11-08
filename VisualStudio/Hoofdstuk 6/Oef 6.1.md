# Oefening 6.1: Cirkel door sliders

**XAML**

```
<Window x:Class="slider2.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:local="clr-namespace:slider2"
        mc:Ignorable="d"
        Title="Sliderz" Height="350" Width="525">
    <Canvas x:Name="paperCanvas" >
        <Slider x:Name="horizSlider" HorizontalAlignment="Left" Margin="39,291,0,0" VerticalAlignment="Top" Width="444" Height="18" ValueChanged="horizSlider_ValueChanged"/>
        <Slider x:Name="vertSlider" HorizontalAlignment="Left" Height="22" Margin="-119,139,0,0" VerticalAlignment="Top" Width="280" RenderTransformOrigin="0.5,0.5" ValueChanged="vertSlider_ValueChanged">
            <Slider.RenderTransform>
                <TransformGroup>
                    <ScaleTransform/>
                    <SkewTransform/>
                    <RotateTransform Angle="90"/>
                    <TranslateTransform/>
                </TransformGroup>
            </Slider.RenderTransform>
        </Slider>
        <Label x:Name="vertLabel" Content="Label" Height="25" Canvas.Left="2" Canvas.Top="129" Width="42"/>
        <Label x:Name="horizLabel" Content="Label" Height="25" Canvas.Left="230" Canvas.Top="286" Width="42"/>
    </Canvas>
</Window>
```
Dit maakt hetgeen deze ![afbeelding](D:\5ITN\MathiasV\AfbeeldingenGithub\2016-11-08 14_03_47-WpfSlider - Microsoft Visual Studio Sliders1.png) weergeeft.
**De Eventhandlers**

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

namespace slider2
{
    public partial class MainWindow : Window
    {
        private Ellipse ellipse;

        public MainWindow()
        {
            InitializeComponent();
            
            vertSlider.Minimum = 0;
            vertSlider.Maximum = 275;

            horizSlider.Minimum = 0;
            horizSlider.Maximum = 450;
            
            vertLabel.Content = Convert.ToString(vertSlider.Value);
            horizLabel.Content = Convert.ToString(horizSlider.Value);

            CreateEllipse();
        }

        private void vertSlider_ValueChanged(object sender, RoutedPropertyChangedEventArgs<double> e)
        {
            int vertical = Convert.ToInt32(vertSlider.Value);
            vertLabel.Content = Convert.ToString(vertical);
            UpdateEllipse();
        }

        private void horizSlider_ValueChanged(object sender, RoutedPropertyChangedEventArgs<double> e)
        {
            int horizontal = Convert.ToInt32(horizSlider.Value);
            horizLabel.Content = Convert.ToString(horizontal);
            UpdateEllipse();
        }

        private void CreateEllipse()
        {
            ellipse = new Ellipse();
            ellipse.Width = horizSlider.Value;
            ellipse.Height = vertSlider.Value;
            ellipse.Stroke = new SolidColorBrush(Colors.Blue);
            ellipse.Fill = new SolidColorBrush(Colors.Blue);
            ellipse.Margin = new Thickness(40, 0, 0, 0);
            paperCanvas.Children.Add(ellipse);
        }

        private void UpdateEllipse()
        {
            ellipse.Width = horizSlider.Value;
            ellipse.Height = vertSlider.Value;
        }
    }
}
```

Deze code zorgt voor het effect dat deze ![afbeelding](D:\5ITN\MathiasV\AfbeeldingenGithub\2016-11-08 14_05_18-Sliderz sliders2.png) weergeeft.
