<script>
    import {Link} from 'svelte-navigator';
    export let data;
</script>

<main>
    <div class="page-title-area">
        <div class="container">
            <div class="page-title-content">
                <h2>Manufacturing Details</h2>
                <ul>
                    <li><a href="index.html">Home</a></li>
                    <li>Manufacturing Details</li>
                </ul>
            </div>
        </div>
    </div>
    {#each data as data}
    <section class="research-details-area ptb-120">
        <div class="container">
            <div class="section-title">
                <span>{data.subtitle}</span>
                <h2>{data.title}</h2>
            </div>
            <div class="row">
                {#each data.DataItems as item}
                <div class="col-lg-4 col-md-12">
                    <div class="research-details-info">
                        <h3>{item.title}</h3>
                        <ul>
                            {#each item.points as point}
                            <li>
                                <i class="flaticon-check-mark"></i>
                                {#if point.subtitle === ""}
                                <span style="margin-top: 25px;">{point.title}</span>
                                {point.subtitle}
                                {:else}
                                <span>{point.title}</span>
                                {point.subtitle}
                                {/if}
                            </li>
                            {/each}
                        </ul>
                    </div>
                </div>
                {/each}
            </div>
        </div>
    </section>
    {/each}
</main>