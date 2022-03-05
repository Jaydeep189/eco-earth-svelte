<script>
import { Link } from 'svelte-navigator'
export let num;
const env = process.env.TEST
</script>

<main>
    <div class="main-banner">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6 col-md-12">
                    <div class="main-banner-content">
                        <span>{num.mainBanner.subtitle}</span>
                        <h1>{num.mainBanner.title}</h1> <h1>{env}</h1>
                        <p>
                            {num.mainBanner.details}
                        </p>
                        <Link to="/contact" class="btn btn-primary">Make Appointment</Link>
                    </div>
                </div>
                <div class="col-lg-6 col-md-12">
                    <div class="banner-image">
                        <img src="assets/img/banner-img1.png" alt="" />
                        <img src="assets/img/bg-shape2.png" alt="" />
                    </div>
                </div>
            </div>
        </div>
        <div class="shape-img1 rotateme">
            <img src="assets/img/shape-image/1.png" alt="" />
        </div>
        <div class="shape-img2">
            <img src="assets/img/shape-image/2.png" alt="" />
        </div>
        <div class="shape-img3 rotateme">
            <img src="assets/img/shape-image/3.png" alt="" />
        </div>
        <div class="shape-img4">
            <img src="assets/img/shape-image/4.png" alt="" />
        </div>
        <div class="shape-img5">
            <img src="assets/img/shape-image/5.png" alt="" />
        </div>
        <div class="shape-img6">
            <img src="assets/img/shape-image/6.png" alt="" />
        </div>
        <div class="shape-img7">
            <img src="assets/img/shape-image/7.png" alt="" />
        </div>
        <div class="shape-img8">
            <img src="assets/img/shape-image/8.png" alt="" />
        </div>
    </div>

    <section class="boxes-area">
        <div class="container">
            <div class="row">
            {#each num.services as service}
            <div class="col-lg-4 col-md-6 col-sm-6">
                    <div class={`single-box ${service.color}`}>
                        <div class="icon">
                            <i class="flaticon-laboratory"></i>
                        </div>
                        <h3>{service.title}</h3>
                        <p>
                            {service.data}
                        </p>
                        <a href="api-intermediates.html" class="learn-more-btn">Learn More <i
                                class="flaticon-arrow-pointing-to-right"></i></a>
                        <div class="shape-box">
                            <img src="assets/img/shape-image/9.png" alt="" />
                            <img src="assets/img/shape-image/10.png" alt="" />
                        </div>
                    </div>
                </div>
            {/each}
            </div>
        </div>
    </section>

    <section class="about-area ptb-120">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-5 col-md-12">
                    <div class="about-image">
                        <img src="assets/img/about-img1.png" alt="" />
                    </div>
                </div>
                <div class="col-lg-7 col-md-12">
                    <div class="about-content">
                        <span>About Us</span>
                        <h2>{num.aboutus.title}</h2>
                        <p>
                            {num.aboutus.subtitle}
                        </p>
                        <ul class="about-features-list">
                        {#each num.aboutus.points as point}
                        <li><i class="flaticon-check-mark"></i>{point}</li>
                        {/each}
                        </ul>
                        <div class="btn-box">
                            <a href="about-us.html" class="btn btn-primary">Learn More</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="bg-shape1">
            <img src="assets/img/bg-shape1.png" alt="" />
        </div>
        <div class="shape-img9">
            <img src="assets/img/shape-image/4.png" alt="" />
        </div>
    </section>

    <section class="services-area ptb-120 pt-0">
        <div class="container">
            <div class="row mt-5">
            {#each num.services as service}
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

    <section class="appointment-area">
        <div class="container">
            <div class="section-title text-center">
                <span class="bg-f59f00">Appointment</span>
                <h2>We Are Here For You To Make An Appointment</h2>
            </div>
        </div>
        <div class="appointment-inner-area jarallax">
            <div class="container">
                <div class="appointment-form">
                    <h3>Reach Us</h3>
                    <form data-netlify="true" method="POST">
                        <div class="form-group">
                            <input type="text" class="form-control" id="name" name="name" placeholder="Name*" />
                        </div>
                        <div class="form-group">
                            <input type="email" class="form-control" id="email" name="email" placeholder="Email*" />
                        </div>
                        <div class="form-group">
                            <textarea name="message" id="message" cols="30" rows="6" class="form-control"
                                placeholder="Message"></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">
                            Send a Request
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <section class="performance-area ptb-120">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6 col-md-12">
                    <div class="performance-content">
                        <div class="section-title">
                            <span class="bg-0018ff">{num.performance.subtitle}</span>
                            <h2>{num.performance.title}</h2>
                        </div>
                        <div class="performance-progress-list">
                        {#each num.performance.plist as list}
                        <div class="single-progress">
                                <div class="progress-bar progress-count" data-percent={list.percentage}></div>
                                <div class="progress-content">
                                    <h3>{list.title}</h3>
                                    <p>{list.subtitle}</p>
                                </div>
                            </div>
                        {/each}
                        </div>
                        <div class="btn-box text-center">
                            <Link to="/manufacturing" class="mt-5 btn btn-primary">Learn More</Link>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6 col-md-12">
                    <div class="performance-image">
                        <img src="assets/img/performance-img1.png" alt="" />
                    </div>
                </div>
            </div>
        </div>
        <div class="bg-shape2">
            <img src="assets/img/bg-shape3.png" alt="" />
        </div>
        <div class="shape-img10">
            <img src="assets/img/shape-image/2.png" alt="" />
        </div>
        <div class="shape-img11 rotateme">
            <img src="assets/img/shape-image/4.png" alt="" />
        </div>
    </section>

    <section class="cta-area ptb-120">
        <div class="container">
            <div class="cta-content">
                <h3>We'll ensure you always get the best Results</h3>
                <h2><a href="/#">{num.contact.phone}</a></h2>

                <Link to="/contact" class="btn btn-primary">Contact Us</Link>
            </div>
        </div>
    </section>
</main>