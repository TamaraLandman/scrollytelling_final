<script>
    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
    import JobsChart from "../lib/JobsChart.svelte";

    let options = {
        chart: {
            type: "pie",
        },
        title: {
            text: "Pie Chart Showing...",
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
                        format: "{point.percentage:.1f}%",
                        style: {
                            fontSize: "1.2em",
                            textOutline: "none",
                        },
                        filter: {
                            operator: ">",
                            property: "percentage",
                            value: 10,
                        },
                    },
                ],
            },
        },
        series: [
            {
                name: "Group",
                data: [
                    // {
                    //     name: "Group 1",
                    //     y: 151,
                    // },
                    { name: "Group 6",
                     y: 65, 
                    
                    },
                    {
                        name: "Group 2",
                        sliced: true,
                        selected: true,
                        y: 180,
                    },
                    {
                        name: "Group 3",
                        y: 32,
                    },
                    {
                        name: "Group 4",
                        y: 103,
                        sliced: true,
                    },
                    {
                        name: "Group 5",
                        y: 77,
                    },
                ],
            },
        ],
    };
</script>

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <JobsChart />
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <p class="job-text">Here's a visualization depicting the workforce representation of Black people in 
                    Cuyahoha County, categorized by job type.
                </p>
            </ArticleText>

            <ArticleText>
               <p class="job-text">When mousing over the chart, it is clear that the two fewest job roles that Black people have are
                <strong>Professional</strong> and <strong>Management</strong>.
                <br> <br>
                These two job titles often require college degrees or a form of higher education and since many 
                Black people don't possess degrees from higher educational institutions, they are unable to 
                obtain these jobs, which also come with higher wages.
                </p>
            </ArticleText>

            <ArticleText>
                <p class="job-text">On the other hand, as the chart indicates, many Black people in Cuyahoga County
                    possess roles such as <strong>Productions/Labor</strong> and <strong>Service</strong>
                    which tend to be lower paying and don't require a college degree.</p>
            </ArticleText>


        {/snippet}
    </Scroller>
</div>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&family=Inclusive+Sans:ital,wght@0,300..700;1,300..700&family=Lexend:wght@100..900&display=swap');
    .job-text{
        font-size: 20px;
        font-family: "Hind", sans-serif;
        font-weight: 400;
        font-style: normal;
    }

    .chart {
        width: 90%;
        margin: 0px auto;
    }
</style>
