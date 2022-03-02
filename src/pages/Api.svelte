<script>
    import {Link} from 'svelte-navigator'
    export let data;
</script>

<main>
    <div class="page-title-area">
        <div class="container">
            <div class="page-title-content">
                <h2>API Intermediates</h2>
                <ul>
                    <li><a href="index.html">Home</a></li>
                    <li>API Intermediates</li>
                </ul>
            </div>
        </div>
    </div>


    <section class="services-area ptb-120 pt-0">
        <div class="container">
            <div class="row mt-5">
                {#each data as api }
                <div class="col-lg-4 col-md-6 col-sm-6 mb-5">
                    <div class="single-services-box h-100">
                        <div class={`icon ${api.color}`}>
                            <i class={api.icon}></i>
                        </div>
                        <h3>{api.title}</h3>
                        {#each api.Datapoints as point }
                        <p>{point}</p>                            
                        {/each}
                    </div>
                </div>
                {/each}
            </div>
        </div>
    </section>

</main>