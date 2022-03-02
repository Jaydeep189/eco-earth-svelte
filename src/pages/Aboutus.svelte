<script>
    import {Link} from 'svelte-navigator';
    export let ServiceData;
    export let AboutData;
</script>

<main>
    <section class="about-our-company ptb-120 pb-0">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6 col-md-12">
                    <div class="about-company-content">
                        <span>{AboutData.aboutus1.subtitle}</span>
                        <h2>{AboutData.aboutus2.title}</h2>
                        <p><b>{AboutData.aboutus1.data}</b></p>
                    </div>
                </div>
                <div class="col-lg-6 col-md-12">
                    <div class="about-company-image">
                        <img src={AboutData.aboutus1.image} alt="">
                    </div>
                </div>
            </div>
        </div>
        <div class="about-our-company-inner">
            <div class="container">
                <div class="row align-items-center">
                    <div class="col-lg-6 col-md-12">
                        <div class="about-inner-company-image">
                            <img src={AboutData.aboutus2.image} alt="">
                        </div>
                    </div>
                    <div class="col-lg-6 col-md-12">
                        <div class="about-inner-company-content">
                            <h2>{AboutData.aboutus2.title}</h2>
                            <p>{AboutData.aboutus2.data}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="services-area ptb-120">
        <div class="container">
            <div class="section-title text-center">
                <span>Services</span>
                <h2>We are the Trusted Experts for your support</h2>
            </div>
            <div class="row">
                {#each ServiceData.services as service}
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