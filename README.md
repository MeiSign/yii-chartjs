yii-chartjs Extension
=====================

![ChartJs](http://www.img-host.de/bild.php/38141,chartsC3E4P.jpg "ChartJS")

Yii Extension for ChartJS library(http://www.chartjs.org/)

This is a simple wrapper to use the ChartJS charts as yii framework php widgets.

Installation
============
1. Clone this repository to the extension folder of your yii app(myApp/protected/extensions)

2. Add to you main.php config(myApp/protected/config/main.php)
`Yii::setPathOfAlias('chartjs', dirname(__FILE__).'/../extensions/yii-chartjs');`

3. Add in the component section of your main.php config(myApp/protected/config/main.php)
`'chartjs'=>array(
    'class' => 'chartjs.components.ChartJs',
),`

4. Add in the preload section of your main.php config(myApp/protected/config/main.php)  

        'preload' => array(
            'chartjs'
        ),

5. Use the widgets:
    
Bar Chart
---------

        <?php 
            $this->widget(
                'chartjs.widgets.ChBars', 
                array(
                    'width' => 600,
                    'height' => 300,
                    'htmlOptions' => array(),
                    'labels' => array("January","February","March","April","May","June"),
                    'datasets' => array(
                        array(
                            "fillColor" => "#ff00ff",
                            "strokeColor" => "rgba(220,220,220,1)",
                            "data" => array(10, 20, 30, 40, 50, 60)
                        )       
                    ),
                    'options' => array()
                )
            ); 
        ?>

Line Chart
----------

        <?php 
            $this->widget(
                'chartjs.widgets.ChLine', 
                array(
                    'width' => 600,
                    'height' => 300,
                    'htmlOptions' => array(),
                    'labels' => array("January","February","March","April","May","June"),
                    'datasets' => array(
                        array(
                            "fillColor" => "rgba(220,220,220,0.5)",
                            "strokeColor" => "rgba(220,220,220,1)",
                            "pointColor" => "rgba(220,220,220,1)",
                            "pointStrokeColor" => "#ffffff",
                            "data" => array(10, 20, 25, 25, 50, 60)
                        ),
                        array(
                            "fillColor" => "rgba(220,220,220,0.5)",
                            "strokeColor" => "rgba(220,220,220,1)",
                            "pointColor" => "rgba(220,220,220,1)",
                            "pointStrokeColor" => "#ffffff",
                            "data" => array(55, 50, 45, 30, 20, 10)
                        )      
                    ),
                    'options' => array()
                )
            ); 
        ?>

Radar Chart
-----------

        <?php 
            $this->widget(
                'chartjs.widgets.ChRadar', 
                array(
                    'width' => 600,
                    'height' => 300,
                    'htmlOptions' => array(),
                    'labels' => array("January","February","March","April", "May"),
                    'datasets' => array(
                        array(
                            "fillColor" => "rgba(220,220,220,0.5)",
                            "strokeColor" => "rgba(220,220,220,1)",
                            "pointColor" => "rgba(220,220,220,1)",
                            "pointStrokeColor" => "#ffffff",
                            "data" => array(5, 15, 50, 25, 35)
                        ),
                        array(
                            "fillColor" => "rgba(220,220,220,0.5)",
                            "strokeColor" => "rgba(220,220,220,1)",
                            "pointColor" => "rgba(220,220,220,1)",
                            "pointStrokeColor" => "#ffffff",
                            "data" => array(55, 50, 45, 30, 20)
                        )      
                    ),
                    'options' => array()
                )
            ); 
        ?>

Polar Area Chart
----------------

        <?php 
            $this->widget(
                'chartjs.widgets.ChPolar', 
                array(
                    'width' => 600,
                    'height' => 300,
                    'htmlOptions' => array(),
                    'drawLabels' => true,
                    'datasets' => array(
                        array(
                            "value" => 50,
                            "color" => "rgba(220,30, 70,1)",
                            "label" => "Hunde"
                        ),
                        array(
                            "value" => 25,
                            "color" => "rgba(66,66,66,1)",
                            "label" => "Katzen"
                        ),
                        array(
                            "value" => 40,
                            "color" => "rgba(100,100,220,1)",
                            "label" => "Vögel"
                        ),
                        array(
                            "value" => 15,
                            "color" => "rgba(20,120,120,1)",
                            "label" => "Mäuse"
                        )
                    ),
                    'options' => array()
                )
            ); 
        ?>
        
Pie Chart
---------

        <?php 
            $this->widget(
                'chartjs.widgets.ChPie', 
                array(
                    'width' => 600,
                    'height' => 300,
                    'htmlOptions' => array(),
                    'drawLabels' => true,
                    'datasets' => array(
                        array(
                            "value" => 50,
                            "color" => "rgba(220,30, 70,1)",
                            "label" => "Hunde"
                        ),
                        array(
                            "value" => 25,
                            "color" => "rgba(66,66,66,1)",
                            "label" => "Katzen"
                        ),
                        array(
                            "value" => 40,
                            "color" => "rgba(100,100,220,1)",
                            "label" => "Vögel"
                        ),
                        array(
                            "value" => 15,
                            "color" => "rgba(20,120,120,1)",
                            "label" => "Mäuse"
                        )
                    ),
                    'options' => array()
                )
            ); 
        ?>

Doughnut Chart
--------------

        <?php 
            $this->widget(
                'chartjs.widgets.ChDoughnut', 
                array(
                    'width' => 600,
                    'height' => 300,
                    'htmlOptions' => array(),
                    'drawLabels' => true,
                    'datasets' => array(
                        array(
                            "value" => 50,
                            "color" => "rgba(220,30, 70,1)",
                            "label" => "Hunde"
                        ),
                        array(
                            "value" => 25,
                            "color" => "rgba(66,66,66,1)",
                            "label" => "Katzen"
                        ),
                        array(
                            "value" => 40,
                            "color" => "rgba(100,100,220,1)",
                            "label" => "Vögel"
                        ),
                        array(
                            "value" => 15,
                            "color" => "rgba(20,120,120,1)",
                            "label" => "Mäuse"
                        )
                    ),
                    'options' => array()
                )
            ); 
        ?>
