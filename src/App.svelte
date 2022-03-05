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
	import { onMount } from 'svelte';
	import {HomepageData, ServiceData, PolicyData, Mdata, ContactData, ApiData, AboutData} from './data'
	let photos = [];
	let data1= [];
	let data2 = [];
	onMount(async () => {
		if (localStorage.getItem("data")){
			var temp = JSON.parse(localStorage.getItem('data'));
			data1 = temp.slice(0, 5);
			data2 = temp.slice(6, 8);
		}else {
			const res = await fetch(`https://jsonplaceholder.typicode.com/photos?_limit=10`);
			photos = await res.json();
			localStorage.setItem("data", JSON.stringify(photos));
			console.log(localStorage.getItem("data"));
			data1 = photos.slice(0, 5);
			data2 = photos.slice(6, 8);
		}

	});
</script>

<main>
<Router>
	<Header />
	<Route path="/">
		<Home num={HomepageData}/>
	</Route>
	<Route path="/services">
		<Services data={ServiceData}/>
	</Route>
	<Route path="/policies">
		<Policies data={PolicyData}/>
	</Route>
	<Route path="/manufacturing">
		<Manufacturing data={Mdata}/>
	</Route>
	<Route path="/contact">
		<Contact data={ContactData}/>
	</Route>
	<Route path="/api-intermediates" >
		<Api data={ApiData}/>
	</Route>
	<Route path="/aboutus" >
		<Aboutus AboutData={AboutData} ServiceData={ServiceData}/>
	</Route>
	<Route>
		<Error />
	</Route>
	<Footer />
</Router>

</main>