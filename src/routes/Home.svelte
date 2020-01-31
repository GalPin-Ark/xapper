<script>
  
   import Button, { Label } from "@smui/button/bare.js";
  import TopAppBar, { Section, Title } from "@smui/top-app-bar/bare.js";
  import Fab, { Icon } from "@smui/fab/bare.js";
  import Chip, { Set, Text } from "@smui/chips/bare.js";
  import Textfield from "@smui/textfield/bare.js";
   import { Link} from "svelte-routing";
  import Card, {
    Content,
    PrimaryAction,
    Media,
    MediaContent,
    Actions,
    ActionButtons,
    ActionIcons
  } from "@smui/card/bare.js";

  import IconButton from "@smui/icon-button/bare.js";

  import { Col, Container, Row } from "sveltestrap";
import "@smui/fab/bare.css";
  import "@smui/button/bare.css";
  import "@smui/icon-button/bare.css";
  import "@smui/top-app-bar/bare.css";
  import "@smui/card/bare.css";
  // Used for SSR. A falsy value is ignored by the Router.

    let prominent = false;
  let dense = false;
  let secondaryColor = false;
</script>
<div class="chai align-items-center justify-content-center">
<h1>Hello </h1>
    <Button variant="raised" >
      <Link to="blog">About</Link>
    </Button>
    <p>
      Visit the
      <a href="https://svelte.dev/tutorial">Svelte tutorial</a>
      to learn how to build Svelte apps.
    </p>
    <Container>
      <Row class="justify-content-center">
        <Col xs="12" md="6" sm="12" lg="4" style="padding-top:1rem; ">
          <Card style="width: auto;">
            <PrimaryAction on:click={() => alert('open page!')}>
              <Media
                style="background-image:
                url(https://via.placeholder.com/320x180.png?text=16x9);"
                aspectRatio="16x9">
                <MediaContent>
                  <div
                    style="color: #fff; position: absolute; bottom: 16px; left:
                    16px;">
                    <h2 class="mdc-typography--headline6" style="margin: 0;">
                      Glorious Item
                    </h2>
                    <h3 class="mdc-typography--subtitle2" style="margin: 0;">
                      People are saying you need to buy it.
                    </h3>
                  </div>
                </MediaContent>
              </Media>
              <Content class="mdc-typography--body2">
                This item is so glorious that you would have to be some kind of
                fool to not immediately buy it.
              </Content>
            </PrimaryAction>
            <Actions>
              <ActionButtons>
                <Button on:click={() => alert('add!')}>
                  <Label>Add to Card</Label>
                </Button>
                <Button on:click={() => alert('buy!')}>
                  <Label>Buy Now</Label>
                </Button>
              </ActionButtons>
              <ActionIcons>
                <IconButton
                  on:click={() => alert('dddsd!')}
                  toggle
                  aria-label="Add to favorites"
                  title="Add to favorites">
                  <Icon class="material-icons" on>favorite</Icon>
                  <Icon class="material-icons">favorite_border</Icon>
                </IconButton>
                <IconButton
                  class="material-icons"
                  on:click={() => alert('share!')}
                  title="Share">
                  share
                </IconButton>
              </ActionIcons>
            </Actions>
          </Card>
        </Col>
        <Col xs="12" md="6" sm="12" lg="4" style="padding-top:1rem;">
          <Card variant="raised" style="width: auto;">
            <PrimaryAction on:click={() => alert('open page!')}>
              <Media
                style="background-image:
                url(https://via.placeholder.com/320x180.png?text=16x9);"
                aspectRatio="16x9">
                <MediaContent>
                  <div
                    style="color: #fff; position: absolute; bottom: 16px; left:
                    16px;">
                    <h2 class="mdc-typography--headline6" style="margin: 0;">
                      Glorious Item
                    </h2>
                    <h3 class="mdc-typography--subtitle2" style="margin: 0;">
                      People are saying you need to buy it.
                    </h3>
                  </div>
                </MediaContent>
              </Media>
              <Content class="mdc-typography--body2">
                This item is so glorious that you would have to be some kind of
                fool to not immediately buy it.
              </Content>
            </PrimaryAction>
            <Actions>
              <ActionButtons>
                <Button on:click={() => alert('add!')}>
                  <Label>Add to Card</Label>
                </Button>
                <Button on:click={() => alert('buy!')}>
                  <Label>Buy Now</Label>
                </Button>
              </ActionButtons>
              <ActionIcons>
                <IconButton
                  on:click={() => alert('dddd!')}
                  toggle
                  aria-label="Add to favorites"
                  title="Add to favorites">
                  <Icon class="material-icons" on>favorite</Icon>
                  <Icon class="material-icons">favorite_border</Icon>
                </IconButton>
                <IconButton
                  class="material-icons"
                  on:click={() => alert('share!')}
                  title="Share">
                  share
                </IconButton>
              </ActionIcons>
            </Actions>
          </Card>
        </Col>
        <Col xs="12" md="6" lg="4" sm="12" style="padding-top:1rem;">
          <Card variant="raised" style="width: auto;">
            <PrimaryAction on:click={() => alert('open page!')}>
              <Media
                style="background-image:
                url(https://via.placeholder.com/320x180.png?text=16x9);"
                aspectRatio="16x9">
                <MediaContent>
                  <div
                    style="color: #fff; position: absolute; bottom: 16px; left:
                    16px;">
                    <h2 class="mdc-typography--headline6" style="margin: 0;">
                      Glorious Item
                    </h2>
                    <h3 class="mdc-typography--subtitle2" style="margin: 0;">
                      People are saying you need to buy it.
                    </h3>
                  </div>
                </MediaContent>
              </Media>
              <Content class="mdc-typography--body2">
                This item is so glorious that you would have to be some kind of
                fool to not immediately buy it.
              </Content>
            </PrimaryAction>
            <Actions>
              <ActionButtons>
                <Button on:click={() => alert('add!')}>
                  <Label>Add to Card</Label>
                </Button>
                <Button on:click={() => alert('buy!')}>
                  <Label>Buy Now</Label>
                </Button>
              </ActionButtons>
              <ActionIcons>
                <IconButton
                  on:click={() => alert('dddd!')}
                  toggle
                  aria-label="Add to favorites"
                  title="Add to favorites">
                  <Icon class="material-icons" on>favorite</Icon>
                  <Icon class="material-icons">favorite_border</Icon>
                </IconButton>
                <IconButton
                  class="material-icons"
                  on:click={() => alert('share!')}
                  title="Share">
                  share
                </IconButton>
              </ActionIcons>
            </Actions>
          </Card>
        </Col>
      </Row>

    </Container>
    <div class="fabi">
      <Fab color={'primary'} on:click={() => alert('FAB!')}>
        <Icon class="material-icons">favorite</Icon>
      </Fab>
    </div>
    </div>
    <style>
  .chai {
    text-align: center;
    
    /* padding: 1em;
		max-width: 240px; */
    margin: 0;

    padding-top: 4rem;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
  .fabi {
    position: fixed !important;
    right: 20px !important;
    bottom: 15px !important;
  }
  .cardi {
    display: flex;
    position: relative;
    justify-content: center;
  }
</style>