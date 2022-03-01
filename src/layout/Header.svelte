<script>
	import { Router, Link, Route } from "svelte-navigator";
    import Home from "../pages/Home.svelte";
</script>

<main>
    <div class="navbar-area">
        <div class="labto-mobile-nav">
            <div class="logo">
                <Link class="navbar-brand" to="index.html">
                    <!-- <img src="assets/img/Narmada Organics Logo3.png" height="70px" alt=""> -->

                    <img src="/img/Narmada Organics Logo3.png" height="70px" alt="" />
                </Link>
            </div>
        </div>
        <div class="labto-nav">
            <div class="container">
                <nav class="navbar navbar-expand-md navbar-light">
                    <Link class="navbar-brand" to="/">
                        <img src="/img/Narmada Organics Logo3.png" height="120px" alt="" />
                        <!-- <img src="assets/img/Narmada Organics Logo3.png" height="120px" alt=""> -->
                    </Link>
                    <div class="collapse navbar-collapse mean-menu" id="navbarSupportedContent">
                        <ul class="navbar-nav">
                            <li class="nav-item">
                                <Link to="/" class="nav-link active">Home</Link>
                            </li>
                            <li class="nav-item">
                                <Link to="/services" class="nav-link">Services</Link>
                            </li>
                            <li class="nav-item">
                                <Link to="/api-intermediates" class="nav-link">API Intermediates</Link>
                            </li>
                            <li class="nav-item">
                                <a href="/#" class="nav-link">Manufacturing <i class="fas fa-chevron-down"></i></a>
                                <ul class="dropdown-menu">
                                    <li class="nav-item">
                                        <Link to="/policies" class="nav-link">Policies</Link>
                                    </li>
                                    <li class="nav-item">
                                        <Link to="/manufacturing" class="nav-link">Manufacturing Details</Link>
                                    </li>
                                </ul>
                            </li>
                            <li class="nav-item">
                                <Link to="/contact" class="nav-link">Contact</Link>
                            </li>
                            <li class="nav-item">
                                <Link to="/aboutus" class="nav-link">About Us</Link>
                            </li>
                        </ul>
                        <div class="others-options">
                            <Link to="/contact" class="btn btn-secondary">Let's Talk</Link>
                        </div>
                    </div>
                </nav>
            </div>
        </div>
    </div>
</main>