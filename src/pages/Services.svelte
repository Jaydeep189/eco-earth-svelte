<script>
    import {Link} from 'svelte-navigator';
    export let data;
    const secret = process.env.NT
</script>

<main>
    <div class="page-title-area">
        <div class="container">
            <div class="page-title-content">
                <h2>{secret}</h2>
                <ul>
                    <li><a href="index.html">Home</a></li>
                    <li>Services</li>
                </ul>
            </div>
        </div>
    </div>


    <section class="services-area ptb-120 pt-0">
        <div class="container">
            <div class="row mt-5">
                {#each data.services as service}
            <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class="single-services-box">
                        <div class={`icon ${service.color}`}>
                            <i class={service.icon}></i>
                        </div>
                        <h3>{service.title}</h3>
                        <p>
                            {service.data}
                        </p>
                    </div>
                </div>
            {/each}
            </div>
        </div>
    </section>

</main>