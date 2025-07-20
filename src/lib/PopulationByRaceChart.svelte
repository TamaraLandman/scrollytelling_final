<script>

    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "./Scroller.svelte";
    import ArticleText from "./ArticleText.svelte";


    let options = {
        chart: {
            type: "bar",
        },
        title: {
            text: "Population of Cuyahoga County According to Race",
        },
        xAxis : {
            categories: ['Asian', 'Hispanic', 'Black', 'White'],
            title: {
            text: null
             },
        gridLineWidth: 1,
        lineWidth: 0,
        },

        yAxis: {
        min: 0,
        title: {
            text: 'Population (thousands)',
            align: 'high'
        },
        labels: {
            overflow: 'justify'
        },
        gridLineWidth: 0
    },
    tooltip: {
        valueSuffix: ' thousand'
    },
    plotOptions: {
        bar: {
            borderRadius: '50%',
            dataLabels: {
                enabled: true
            },
            groupPadding: 0.1
        }
    },
    legend: {
        layout: 'vertical',
        align: 'right',
        verticalAlign: 'top',
        x: -40,
        y: 80,
        floating: true,
        borderWidth: 1,
        backgroundColor: 'var(--highcharts-background-color, #ffffff)',
        shadow: true
    },
    credits: {
        enabled: false
    },

        series: [
            {
                name: "Group",
                data: [
                    // {
                    //     name: "Group 1",
                    //     y: 151,
                    // },
                    { name: "Asian",
                     y: 41, 
                    
                    },
                    {
                        name: "Hispanic",
                        y: 85,
                    },
                    {
                        name: "Black",
                        sliced: true,
                        selected: false,
                        y: 362,
                    },
                    {
                        name: "White",
                        y: 734,
                
                    },
                    // {
                    //     name: "Group 5",
                    //     y: 77,
                    // },
                ],
            },
        ],
    };

    </script>

<div class="chart1">
            <Chart {options} highcharts={Highcharts} />
</div>

         
<style>
    .chart1 {
        width: 105%;
        margin: 0px auto;
    }
</style>