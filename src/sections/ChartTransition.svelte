<script>

    import * as Highcharts from "highcharts";
    import "highcharts/modules/exporting";
    import { Chart } from "@highcharts/svelte";
    import Scroller from "../lib/Scroller.svelte";
    import ArticleText from "../lib/ArticleText.svelte";
    import DegreeChart from "../lib/CollegeDegreesChart.svelte";
    import { fade, fly } from "svelte/transition";
    import ObservedArticleText from "../lib/ObservedArticleText.svelte";
    import PopulationByRaceChart from "../lib/PopulationByRaceChart.svelte";



    let options1 = {
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



    let chart2IsVisible = $state(false);

    const options = {
        threshold: [0.85, 0.95],
    };

    const simpleCallback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                // "active" state
                elem.style.backgroundColor = "#03084ee0";
            } else if (entry.intersectionRatio < 0.9) {
                // "inactive" state
                elem.style.backgroundColor = "#03084ee0";
            }
        });
    };

    const showChart2Callback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                elem.style.backgroundColor = "#03084ee0";
                chart2IsVisible = true;
            } else if (entry.intersectionRatio < 0.9) {
                elem.style.backgroundColor = "#03084ee0";
            }
        });
    };

    const removeChart2Callback = (entries, observer) => {
        entries.forEach((entry) => {
            const elem = entry.target;

            if (entry.intersectionRatio >= 0.9) {
                elem.style.backgroundColor = "#03084ee0";
                chart2IsVisible = false;
            } else if (entry.intersectionRatio < 0.9) {
                elem.style.backgroundColor = "#03084ee0";
            }
        });
    };

</script>
<div class="page3-background">
 <div>
    <!-- <Scroller layout="right">
        {#snippet sticky()}
            <div class="chart">
                <Chart {options} highcharts={Highcharts} />
            </div>
            <p>
                Here's an example chart using
                <a href="https://www.highcharts.com/">Highcharts</a>!
            </p>
            <p>
                📈 <strong>Highcharts</strong> is a super-flexible library for
                creating all kinds of charts. See demos of different chart types
                <a href="https://www.highcharts.com/demo">here</a>.
            </p>
            <p>
                Since we're using Highcharts through Svelte, the syntax is a
                little different from what you might see in the demos. But all
                of Highcharts' functionality is available through the Highcharts
                for Svelte package.
            </p>
            <p>
                The configuration is done through the
                <code>options</code> json object passed to the chart, which you'll
                see in the source code for this template.
            </p>
            <p>
                Use the
                <a href="https://api.highcharts.com/highcharts/"
                    >API reference</a
                >
                to understand what each element in the <code>options</code> object
                does.
            </p>
        {/snippet}

        {#snippet scrolly()}
            <ArticleText>
                <strong>Welcome to the KWK Data Scrollytelling Template!</strong
                >
            </ArticleText>

            <ArticleText>
                This is a <strong>basic example</strong> of how you might create
                a scrollytelling piece using Svelte and Highcharts.
            </ArticleText>

            <ArticleText>
                You can use this template as a <strong>starting point</strong>
                for your project.
                <br /><br />
                Or, if you want to build something from scratch, you can use it as
                a <strong>reference</strong> for specific functionality.
            </ArticleText>

            <ArticleText>
                This is <strong>just one way</strong> that scrollytelling can
                look.
                <br /><br />
                <strong>
                    If you use this template, be sure to modify it and make it
                    your own!
                </strong>
            </ArticleText>
        {/snippet}
    </Scroller> -->
</div> 

<div>
    <Scroller layout="right">
        {#snippet sticky()}
            <div>
                {#if chart2IsVisible}
                    <DegreeChart />
                   
                {:else}
                    <PopulationByRaceChart />
        
                {/if}

                <br />
            </div>
        {/snippet}

        {#snippet scrolly()}
            <ObservedArticleText callback={removeChart2Callback} {options}>
              <p class="explanation-text"> According to the Black Wealth Data Center (BWDC), the Black population of Cuyahoga County is the second largest by far, compared
                to other racial groups. </p>
                
        
            </ObservedArticleText>

            <ObservedArticleText callback={showChart2Callback} {options}>
              <p class="explanation-text">  However, when examining the percentage of <strong>College Degrees </strong>
                attained by residents of the county, only <strong>18.4%</strong> of Black people recieved a Bachelor's degree.
                <br><br>
                Not only is this percent a low amount, it is also the lowest of these four races, which is 
                disproportionate to the amount of Black people living in the county. </p>
            </ObservedArticleText>

            <!-- <ObservedArticleText callback={removeChart2Callback} {options}>
                When this box scrolls into view, the callback will set
                <code>duckIsVisible</code> to <code>false</code>.
                <br /><br />
                Svelte then automatically updates the page (more precisely, the DOM)
                and removes the duck component.
                <br /><br />
                The Svelte transition
                <code>{"out:fade"}</code>
                handles animating the transition.
            </ObservedArticleText>

            <ObservedArticleText callback={simpleCallback} {options}>
                Pretty slick, huh?
                <br /><br />
                🤔
                <strong
                    >How might you use a transition like this for emotional
                    impact in your final project?</strong
                >
            </ObservedArticleText> -->
        {/snippet}
    </Scroller>
  </div>
</div>

<style>

    @import url('https://fonts.googleapis.com/css2?family=Mulish:ital,wght@0,200..1000;1,200..1000&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&family=Mulish:ital,wght@0,200..1000;1,200..1000&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Hind:wght@300;400;500;600;700&family=Inclusive+Sans:ital,wght@0,300..700;1,300..700&family=Lexend:wght@100..900&display=swap');
    /* .duck-img {
        margin: 0px auto;
    } */
    .chart {
        width: 90%;
        margin: 0px auto;
    }

    .page3-background {
        background-color: #292929;
    } 

    .explanation-text{
        /* font-family: "Lato", sans-serif; */
        font-family: "Hind", sans-serif;
        font-weight: 400;
        font-style: normal;
        font-size: 20px;
    }
</style>






