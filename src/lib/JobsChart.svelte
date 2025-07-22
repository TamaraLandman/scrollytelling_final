<script>
    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";

    let options = {
        chart: {
            type: "pie",
        },
        zooming: {
            type: 'xy'
        },  
        panning: {
            enabled: true,
            type: 'xy'
        },
        title: {
            text: "Workforce Representation by Job Role",
        },
        subtitle: {
        text:
        'Source:<a href="https://public.tableau.com/views/BWDC-EMP15_17525572314110/EMP15?:language=en-US&padding=0&:embed=y&:sid=&:redirect=auth&:origin=viz_share_link&:display_count=n&position=relative" target="_default">BWDC</a>'
        },
        tooltip: {
            valueSuffix: '%'
        },
        plotOptions: {
            pie: {
                allowPointSelect: true,
                dataLabels: [
                    {
                        enabled: true,
                        distance: 20,
                    },
                    {
                        enabled: true,
                        distance: -40,
                        // format: "{point.percentage:.1f}%",
                        style: {
                            fontSize: "1.2em",
                            textOutline: "none",
                        },
                        filter: {
                            operator: ">",
                            // property: "percentage",
                            value: 10,
                        },
                    },
                ],
            },
        },
        series: [
            {
                name: "Percentage",
                colorByPoint: true,
                data: [
                    {
                        name: "Production/Labor",
                        y: 30.7,
                        color: "#561B36",
    
                        
                    },
                    { name: "Management",
                        y: 9.1, 
                        // sliced: true,
                        // selected: true,

                    
                    },
                    {
                        name: "Professional",
                        // sliced: true,
                        // selected: true,
                        y: 9.6,
                        color: "#03084E",
                    },
                    {
                        name: "Sales/Admin",
                        y: 23,
                        color: "#a53860",
                        
                    },
                    {
                        name: "Service",
                        y: 39.5,
                        color: "#820D42",
                
                    },
                    {
                        name: "Technical",
                        y: 25.4,
                        color: '#221749',
                    },
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
        width: 85%;
        margin: 0px auto;
        font-family: 'Courier New', Courier, monospace;
        /* border: solid, 10px, "#820D42"; */
        box-shadow: 50px 50px 2px #27111b67;
        /* border-radius: 40px; */
    }
    </style>