<script>
    import {Link} from 'svelte-navigator'
   export let data;
</script>

<div class="page-title-area">
    <div class="container">
        <div class="page-title-content">
            <h2>Policies</h2>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li>Policies</li>
            </ul>
        </div>
    </div>
</div>
<section class="services-details-area ptb-115">
    <div class="container">
        <div class="row">
            <div class="col-lg-2">
            </div>
            <div class="col-lg-8 col-md-12">
                <div class="services-details text-center">
                    <div class="services-details-desc ">
                        {#each data as data}
                        <div class="mb-4 mt-5 section-title text-center">
                            <h2>{data.title}</h2>
                        </div>
                        <p>{data.data}</p>
                        {/each}
                    </div>
                </div>
            </div>

            <div class="col-lg-2">

            </div>
        </div>
    </div>
</section>