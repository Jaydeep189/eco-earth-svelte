<script>
	import Home from "./pages/Home.svelte";
	import Header from "./layout/Header.svelte";
	import Footer from './layout/Footer.svelte';
	import { Router, Link, Route } from "svelte-navigator";
	import Services from './pages/Services.svelte';
	import Policies from "./pages/Policies.svelte";
	import Manufacturing from './pages/Manfacturing.svelte';
	import Error from './pages/Error.svelte';
	import Contact from './pages/Contact.svelte';
	import Api from './pages/Api.svelte';
	import Aboutus from "./pages/Aboutus.svelte";
</script>

<main>
<Router>
	<Header />
	<Route path="/" component={Home}/>
	<Route path="/services" component={Services}/>
	<Route path="/policies" component={Policies}/>
	<Route path="/manufacturing" component={Manufacturing}/>
	<Route path="/contact" component={Contact}/>
	<Route path="/api-intermediates" component={Api}/>
	<Route path="/aboutus" component={Aboutus}/>
	<Route path="" component={Error} />
	<Footer />
</Router>

</main>