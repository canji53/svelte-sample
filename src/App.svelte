<script lang="ts">
    import { Route, Router } from "svelte-routing";
    import Layout from "./components/Layout.svelte";
    import Home from "./pages/Home.svelte";
    import Help from "./pages/Help.svelte";
    import NotFound from "./pages/NotFound.svelte";
</script>

<Router>
    <Layout>
        <Route path="/">
            <Home />
        </Route>
        <Route path="/help">
            <Help />
        </Route>
        <Route path="/*" component={NotFound} />
    </Layout>
</Router>