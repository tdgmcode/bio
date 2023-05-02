<style>
    .wrapper {
        text-align: center;
        height: 100vh;
        display: flex;
        align-items: center;
    }
    .big {
        font-size: 3rem;
        font-weight: bold;
    }

    .semibig {
        font-size: 2rem;
        font-weight: bold;
        color: rgb(255, 0, 0);
    }
    .main {
        margin: 5px;
    }
</style>

<script>
    let date = new Date("March 28 2026 00:00:00 GMT-0400 (Eastern Daylight Time)");
    let initDate = 0;

    let intervals = [
        "FullYear",
        "Month",
        "Date",
        "Hours",
        "Minutes",
        "Seconds"
    ];

    let intervalNames = [
        "years",
        "months",
        "days",
        "hours",
        "minutes",
        "seconds"
    ];

    let time = "";

    let comparSeg = [];

    let itsHere = false;

    setInterval(() => {
        initDate = new Date();

        itsHere = (date <= initDate);

        if (itsHere) return;

        let dateSeg = intervals.map(x => date["get" + x]());
        let dateSegInit = intervals.map(x => initDate["get" + x]());

        comparSeg = dateSegInit.map((x,i) => {
            let addDiff = 0;

            for (var j = i; j < dateSeg.length; j++) {
                if (dateSeg[j] < dateSegInit[j]) {
                    addDiff = -1;
                    break;
                }

                if (dateSeg[j] > dateSegInit[j]) {
                    addDiff = 0;
                    break;
                }
            }

            return dateSeg[i] - dateSegInit[i] 
        })

        
        while (comparSeg.find(x => x < 0)) {
            
            for (var i = comparSeg.length - 1; i >= 0; i--) {
                if (comparSeg[i] < 0) {
                    let tempDateInit = new Date(initDate);
                    let tempDate = new Date(date);

                    tempDateInit["set" + intervals[i]](0);
                    tempDate["set" + intervals[i]](comparSeg[i]);

                    comparSeg[i] = tempDate["get" + intervals[i]]() - tempDateInit["get" + intervals[i]]();

                    if (i > 0) {
                        comparSeg[i-1]--;
                    }
                }
            }
        }

        comparSeg = comparSeg.map((x,i) => [x,intervalNames[i]]);
        
    },200);
</script>

<div class='wrapper'>
    <div>
    {#if itsHere}
        <p class='semibig'>Welcome to life.</p>
    {:else}
        {#each comparSeg as seg}
            <span class='main'><span class='big'>{seg[0]}</span> {seg[1]}</span>
        {/each}
        <p class='semibig'>until I need to truly get a life.</p>
    {/if}
    <p>Time ticks.</p>
    </div>
</div>