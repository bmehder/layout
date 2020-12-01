<script>
  // Layout Components
  import Header from "./Layouts/Header.svelte";
  import Section from "./Layouts/Section.svelte";
  import Grid from "./Layouts/Grid.svelte";
  import Flex from "./Layouts/Flex.svelte";
  import Footer from "./Layouts/Footer.svelte";

  // UI Components
  import Timeline from "./UI/Timeline.svelte";
  import Tabs from "./UI/Tabs.svelte";
  import FancyCard from "./UI/FancyCard.svelte";
  import Form from "./UI/Form.svelte";
  import Blockquote from "./UI/Blockquote.svelte";
  import Hero from "./UI/Hero.svelte";
  import Button from "./UI/Button.svelte";
  import Fetcher from "./UI/Fetcher.svelte";
  import Animation from "./UI/Animation.svelte";

  // Data Stores
  import { tennis } from "./Data/tennis.js";
  import { tabData } from "./Data/tabData.js";
</script>

<div class="wrapper">
  <Header />
  <main>
    <Hero
      background="https://source.unsplash.com/random/"
      title="We're leaving now. Thanks for all the fish.">
      <Button uppercase reflection shadow background="darkorange">
        Make My Day
      </Button>
    </Hero>

    <Section background="linear-gradient(to right, #b24592, #f15f79)">
      <Timeline data={tennis} />
    </Section>

    <Section background="dodgerblue">
      <Tabs data={tabData} />
    </Section>

    <Section boxed background="white" padding="40px 20px">
      <h3>Lorem Ipsum</h3>
      <Grid columns="1fr 1fr" gap="3em">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate
          nulla ullam, sed dolor accusantium totam eius modi nobis quo id
          repellendus nesciunt sint earum reprehenderit repellat non ea, labore
          rerum nisi consequuntur exercitationem voluptas magni quibusdam illum?
          Tempora distinctio sed veniam velit nihil molestias, animi aliquid
          nobis ab dignissimos esse.
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur, adipisicing elit. Alias,
          dolore suscipit vero nulla incidunt fugit veritatis, ad laborum
          eveniet saepe maiores a cum at hic ipsam ullam amet expedita. Totam
          eligendi fugiat deserunt. Harum reprehenderit temporibus ad pariatur.
          Ex dolorum eum possimus quis soluta dolore eius consectetur alias
          voluptas nesciunt?
        </p>
      </Grid>
      <p>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Alias, dolore
        suscipit vero nulla incidunt fugit veritatis, ad laborum eveniet saepe
        maiores a cum at hic ipsam ullam amet expedita. Totam eligendi fugiat
        deserunt. Harum reprehenderit temporibus ad pariatur. Ex dolorum eum
        possimus quis soluta dolore eius consectetur alias voluptas nesciunt?
      </p>
      <Blockquote shadow>
        Lorem ipsum dolor sit amet consectetur, adipisicing elit. Alias, dolore
        suscipit vero.
      </Blockquote>
    </Section>

    <Section background="#f3f3f3">
      <Flex justify="space-around" align="center">
        <FancyCard ribbon />
        <FancyCard raise fx />
      </Flex>
      <FancyCard
        metal
        ribbon
        blur
        title="My Custom Title"
        content="Lorem ipsum dolor sit amet consectetur, adipisicing elit. Alias, dolore
        suscipit vero nulla incidunt fugit veritatis, ad laborum eveniet saepe
        maiores a cum at hic ipsam ullam amet expedita. Totam eligendi fugiat
        deserunt. Harum reprehenderit temporibus ad pariatur. Ex dolorum eum
        possimus quis soluta dolore eius consectetur alias voluptas nesciunt?" />
    </Section>

    <Section background="#323232">
      <Grid columns="1fr 1fr" gap="2em">
        <FancyCard ribbon />
        <FancyCard raise fx />
      </Grid>
      <FancyCard
        ribbon
        blur
        title="My Custom Title"
        content="Lorem ipsum dolor sit amet consectetur, adipisicing elit. Alias, dolore
        suscipit vero nulla incidunt fugit veritatis, ad laborum eveniet saepe
        maiores a cum at hic ipsam ullam amet expedita. Totam eligendi fugiat
        deserunt. Harum reprehenderit temporibus ad pariatur. Ex dolorum eum
        possimus quis soluta dolore eius consectetur alias voluptas nesciunt?" />
    </Section>

    <Section
      background="linear-gradient(to right, #005c97, #363795)"
      padding="2em 0 0">
      <Flex justify="center">
        <Form
          title="Send Us A Message"
          titleColor="white"
          buttonText="Submit Message"
          buttonColor="darkorange" />
      </Flex>
    </Section>

    <!-- <Section background="linear-gradient(to right, #005c97, #363795)">
      <Fetcher />
    </Section> -->

    <Section
      background="radial-gradient(
      circle 60em,
      transparent,
      rgba(48, 122, 213, 0.8)
    )">
      <Animation />
    </Section>
  </main>
  <Footer background="#323232">
    &copy; 2021 Brad Mehder. All rights reserved.
  </Footer>
</div>

<style>
  :global(body) {
    background-color: white;
  }
  .wrapper {
    display: grid;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
  }
</style>
