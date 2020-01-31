<script>
  import { Router, Route } from "svelte-routing";
  import NavLink from "./components/NavLink.svelte";
  import Home from "./routes/Home.svelte";
  import About from "./routes/About.svelte";
  import Blog from "./routes/Blog.svelte";
   import Button, { Label } from "@smui/button/bare.js";
  import TopAppBar, { Section, Title } from "@smui/top-app-bar/bare.js";
     import IconButton from "@smui/icon-button/bare.js";

  import { Col, Container, Row } from "sveltestrap";

    import "@smui/button/bare.css";
  import "@smui/icon-button/bare.css";
  import "@smui/top-app-bar/bare.css";
  // Used for SSR. A falsy value is ignored by the Router.
  export let url = "";
let prominent = false;
  let dense = false;
  let secondaryColor = false;

  let current = "main";
  let drawer;
  let drawerOpen = false;

  console.log("asdasd " + drawerOpen);
  function go(key) {
    current = key;
    drawerOpen = false;
  }
</script>

<Router url="{url}">
 <div class="flexy">
    <div class="top-app-bar-container">
      <TopAppBar
        variant="standar"
        {prominent}
        {dense}
        color={secondaryColor ? 'secondary' : 'primary'}>
        <Row style="margin-left: 0;margin-right: 0;">
          <Section>
            <IconButton
              on:click={() => (drawerOpen = !drawerOpen)}
              class="material-icons">
              menu
            </IconButton>
            <Title>Static</Title>
          </Section>
          <Section align="end" toolbar>
            <IconButton class="material-icons" aria-label="Download">
              file_download
            </IconButton>
            <IconButton class="material-icons" aria-label="Print this page">
              print
            </IconButton>
            <IconButton class="material-icons" aria-label="Bookmark this page">
              bookmark
            </IconButton>
          </Section>
        </Row>
      </TopAppBar>
    
 </div>
  <div>
    <Route path="about" component="{About}" />
    <Route path="blog/*" component="{Blog}" />
    <Route path="/" component="{Home}" />
  </div>
</Router>
