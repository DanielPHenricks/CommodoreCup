<!-- CardContainer.svelte -->

<script>
    let cards = [
        {
            imageUrl: "/images/carbon-neutral.png",
            mainStat: "Carbon Neutral",
            desc: "Vanderbilt has been carbon neutral since FY20.",
        },
        {
            imageUrl: "/images/LEED.png",
            mainStat: "24+",
            desc: "Vanderbilt has 24+ LEED certified projects and was the first university in TN to earn LEED certification.",
        },
        {
            imageUrl: "/images/waterIcon.svg",
            mainStat: "253M gallons",
            desc: "As of 2022, the University's water usage was down over 60% compared to 10 years ago.",
        },
    ];
</script>

<div class="container">
    <p class="sectionName">STATISTICS</p>
    <h2 class="mainText">
        Some of Vanderbilt's most significant sustainabililty metrics
    </h2>
    <div class="card-container">
        {#each cards as card (card.imageUrl)}
            <div class="card">
                <img src={card.imageUrl} alt="Card Image" />
                <h2 class="mainText">{card.mainStat}</h2>
                <p class="sectionName">{card.desc}</p>
            </div>
        {/each}
    </div>
    <div class="card-container">
        {#each cards as card (card.imageUrl)}
            <div class="card">
                <img src={card.imageUrl} alt="Card Image" />
                <h2 class="mainText">{card.mainStat}</h2>
                <p class="sectionName">{card.desc}</p>
            </div>
        {/each}
    </div>
</div>

<style>
    .sectionName {
        font-family: "FiraCode";
        font-size: 20px;
    }

    .mainText {
        font-family: "FiraCode";
        font-size: 40px;
        font-weight: bold;
    }

    .container {
        padding: 40px;
    }

    .card-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 40px;
        padding: 20px;
    }

    .card {
        background-color: #dedede;
        border-radius: 8px;
        padding: 5px;
        padding-top: 20px;
        text-align: center;
        height: 75vh;
    }

    .card img {
        max-width: 100%;
        height: 20vh;
        border-radius: 4px;
    }
</style>
