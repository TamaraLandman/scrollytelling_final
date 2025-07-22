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
            text: "Population of Cuyahoga County According to Race",
        },
        subtitle: {
        text:
        'Source:<a href="https://public.tableau.com/views/BWDC-Population-Section1/Dashboard-V1?:language=en-US&padding=0&:embed=y&:sid=&:redirect=auth&:origin=viz_share_link&:display_count=n&position=relative" target="_default">BWDC</a>'
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
            text: 'Population (thousands)',
            align: 'high'
        },
        labels: {
            overflow: 'justify'
        },
        gridLineWidth: 0
    },
    tooltip: {
        valueSuffix: ',000'
    },
    plotOptions: {
        bar: {
            borderRadius: '30%',
            pointWidth: 40,
            pointPadding: 0,
            dataLabels: {
                enabled: true
            },
            groupPadding: 1,
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
                name: null,
                data: [
                    // {
                    //     name: "Group 1",
                    //     y: 151,
                    // },
                    { name: "Asian",
                     y: 41, 
                     color: '#221749',
                    
                    },
                    {
                        name: "Hispanic",
                        y: 85,
                        color: "#03084E",
                    },
                    {
                        name: "Black",
                        sliced: true,
                        selected: false,
                        y: 362,
                        color: "#561B36",
                    },
                    {
                        name: "White",
                        y: 734,
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

<div class="chart1-background">
<div class="chart1">
            <Chart {options} highcharts={Highcharts} />
</div>
</div>

         
<style>
    .chart1-background {

    }


    .chart1 {
        width: 100%;
        margin: 0px auto;
        font-family: 'Courier New', Courier, monospace;
        /* border: solid, 10px, "#820D42"; */
        box-shadow: 50px 50px 2px #27111b67;
        /* border-radius: 40px; */
    }

</style>