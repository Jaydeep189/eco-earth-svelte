<script>
    import {Link} from 'svelte-navigator';
    export let data;
</script>

<main>
    <div class="page-title-area">
        <div class="container">
            <div class="page-title-content">
                <h2>Contact Us</h2>
                <ul>
                    <li><a href="index.html">Home</a></li>
                    <li>Contact</li>
                </ul>
            </div>
        </div>
    </div>


    <section class="contact-area ptb-120">
        <div class="container">
            <div class="section-title text-center">
                <span class="bg-ff5d24">Message Us</span>
                <h2>Reach Us</h2>
            </div>
            <form id="contactForm" data-netlify="true" method="POST">
                <div class="row">
                    <div class="col-lg-6 col-md-6">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Your Name" name="name" id="name" required data-error="Please enter your name">
                            <div class="help-block with-errors"></div>
                        </div>
                    </div>
                    <div class="col-lg-6 col-md-6">
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Your Email Address" name="email" id="email" required data-error="Please enter your email">
                            <div class="help-block with-errors"></div>
                        </div>
                    </div>

                    <div class="col-lg-6 col-md-6">
                        <div class="form-group">
                            <input type="text" class="form-control" name="phone_number" placeholder="Phone Number" id="phone_number" required data-error="Please enter your number">
                            <div class="help-block with-errors"></div>
                        </div>
                    </div>
                    <div class="col-lg-6 col-md-6">
                        <div class="form-group">
                            <input type="text" class="form-control" name="msg_subject" placeholder="Subject" id="msg_subject" required data-error="Please enter your subject">
                            <div class="help-block with-errors"></div>
                        </div>
                    </div>
                    <div class="col-lg-12 col-md-12">
                        <div class="form-group">
                            <textarea name="message" class="form-control" id="message" cols="30" rows="10" placeholder="Type Your Message Here" required data-error="Write your message"></textarea>
                            <div class="help-block with-errors"></div>
                        </div>
                    </div>
                    <div class="col-lg-12 col-md-12">
                        <button type="submit" class="btn btn-primary">Send Message</button>
                        <div id="msgSubmit" class="h3 text-center hidden"></div>
                        <div class="clearfix"></div>
                    </div>
                </div>
            </form>
            <div class="contact-info">
                <div class="section-title text-center">
                    <h2>Don't Hesitate to contact with us</h2>
                </div>
                <div class="contact-info-content">
                    <h3>Call us for imidiate support</h3>
                    <h2><a href="tel:+91 94091 33000">{data.phone}</a></h2>
                    <ul class="social">
                        <li><a href={data.social.twitter} target="_blank"><i class="fab fa-tw0itter"></i></a></li>
                        <li><a href={data.social.youtube} target="_blank"><i class="fab fa-youtube"></i></a></li>
                        <li><a href={data.social.facebook} target="_blank"><i class="fab fa-facebook-f"></i></a></li>
                        <li><a href={data.social.linkedin} target="_blank"><i class="fab fa-linkedin-in"></i></a></li>
                        <li><a href={data.social.instagram} target="_blank"><i class="fab fa-instagram"></i></a></li>
                    </ul>
                </div>
            </div>
        </div>
    </section>


    <div id="map">
        <iframe title="" src={data.mapLink}> </iframe>
    </div>
</main>