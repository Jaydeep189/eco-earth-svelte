<script>
    import {Link} from 'svelte-navigator'
</script>
<main>
    <section class="error-area">
        <div class="d-table">
            <div class="d-table-cell">
                <div class="container">
                    <div class="error-content">
                        <img src="assets/img/404.png" alt="error">
                        <h3>Page Not Found</h3>
                        <p>The page you are looking for might have been removed had its name changed or is temporarily unavailable.</p>
                        <Link to="/" class="btn btn-secondary">Go to Home</Link>
                    </div>
                </div>
            </div>
        </div>
    </section>
</main>