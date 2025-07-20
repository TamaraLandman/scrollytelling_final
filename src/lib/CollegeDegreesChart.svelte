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
            text: "Percentage of Bachelors Degrees Attained by Race",
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
            text: 'Percent',
            align: 'high'
        },
        labels: {
            overflow: 'justify'
        },
        gridLineWidth: 0
    },
    tooltip: {
        valueSuffix: ' %'
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
                     y: 66.8, 
                    
                    },
                    {
                        name: "Hispanic",
                        y: 19.4,
                    },
                    {
                        name: "Black",
                        sliced: true,
                        selected: false,
                        y: 18.4,
                    },
                    {
                        name: "White",
                        y: 43.1,
                
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

<div class="chart">
                <Chart {options} highcharts={Highcharts} />
</div>

         
<style>
    .chart {
        width: 105%;
        margin: 0px auto;
    }
</style>