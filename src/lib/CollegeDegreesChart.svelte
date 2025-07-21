<script>

    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "./Scroller.svelte";
    import ArticleText from "./ArticleText.svelte";


    let options = {
        chart: {
            type: "bar",
            // borderColor: '#C2C1C2',
            // borderWidth: 4,
            // borderRadius: "2.5%",
        },
        title: {
            text: "Percentage of Bachelors Degrees Attained by Race",
        },
        xAxis : {
            categories: ['Asian', 'Hispanic', 'Black', 'White'],
            title: {
            text: null
             },
        gridLineWidth: 0,
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
        valueSuffix: '%'
    },
    plotOptions: {
        bar: {
            borderRadius: '30%',
            pointWidth: 40,
            pointPadding: 0,
            dataLabels: {
                enabled: true
            },
            groupPadding: 0.5,
        }
    },
    legend: {
        layout: 'vertical',
        align: 'right',
        verticalAlign: 'top',
        x: -40,
        y: 80,
        floating: false,
        borderWidth: 0,
        backgroundColor: 'var(--highcharts-background-color, #ffffff)',
        shadow: false,
        },
    credits: {
        enabled: false
    },

        series: [
            {
                data: [
                    // {
                    //     name: "Group 1",
                    //     y: 151,
                    // },
                    { name: "Asian",
                     y: 66.8,
                     color: '#221749',
                    
                    },
                    {
                        name: "Hispanic",
                        y: 19.4,
                        color: "#03084E",
                    },
                    {
                        name: "Black",
                        sliced: true,
                        selected: false,
                        y: 18.4,
                        color: "#561B36",
                    },
                    {
                        name: "White",
                        y: 43.1,
                        color: "#820D42",
                
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
        width: 100%;
        margin: 0px auto;
        box-shadow: 50px 50px 2px #27111b67;
    }
</style>