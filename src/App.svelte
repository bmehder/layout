<script>
  import Header from "./Header.svelte";
  import Section from "./Section.svelte";
  import Grid from "./Grid.svelte";
  import Flex from "./Flex.svelte";
  import Footer from "./Footer.svelte";
</script>

<div class="wrapper">
  <Header />
  <main>
    <Section
      background="linear-gradient(to bottom, blue, green)"
      padding="2em 1em"
      margin="2em 0">
      <Flex align="center">
        <p>1</p>
        <p>2</p>
        <p>3</p>
      </Flex>
    </Section>

    <Section boxed background="dodgerblue" padding="40px">
      <Flex direction="row" align="end" justify="space-around">
        <p>4</p>
        <p>5</p>
        <p>6</p>
      </Flex>
    </Section>

    <Section boxed background="dodgerblue" padding="40px">
      <Flex direction="row" align="center" justify="center">
        <p>7</p>
        <p>8</p>
        <p>9</p>
      </Flex>
    </Section>

    <Section boxed background="coral" padding="40px">
      <Flex justify="space-between">
        <p style="flex:1;">10</p>
        <p style="flex:1;">11</p>
      </Flex>
    </Section>

    <Section background="yellow" padding="40px">
      <Grid columns="1fr 1fr 1fr 1fr" gap="40px" place="center">
        <p style="width:100%;">12</p>
        <p style="width:100%;">13</p>
        <p style="width:100%;">14</p>
      </Grid>
    </Section>

    <Section boxed background="magenta" padding="40px">
      <Grid columns="1fr 1fr 1fr 1fr">
        <p>15</p>
        <p>16</p>
        <p>17</p>
        <Grid columns="1fr">
          <p style="width: 100%;">18</p>
          <!-- <p>19</p>
          <p>20</p> -->
        </Grid>
      </Grid>
    </Section>

    <Section
      background="url('https://source.unsplash.com/random/') center center/cover"
      margin="2em auto"
      padding="40px">
      <Flex justify="center">
        <p
          style="background: none; text-shadow: 0 0 10px rgba(0,0,0,0.5);font-size:4em;text-align:center;padding:2em;">
          Hello World!
        </p>
      </Flex>
    </Section>

    <Section
      boxed
      background="darkorange"
      padding="80px 40px"
      margin="2em auto">
      <Grid
        columns="1fr 4fr 1fr"
        rows="minmax(200px, 400px) 1fr"
        place="center"
        gap="2em">
        <p style="width:100%;height:100%;">21</p>
        <p style="width:100%;height:100%;">22</p>
        <p style="width:100%;height:100%;">23</p>
        <p style="width:100%;height:100%;">X</p>
        <p style="width:100%;height:100%;">Y</p>
        <p style="width:100%;height:100%;">Z</p>
      </Grid>
    </Section>
  </main>
  <Footer>Copyright 2021</Footer>
</div>

<style>
  :global(body) {
    background-color: blanchedalmond;
  }
  .wrapper {
    display: grid;
    grid-template-rows: auto 1fr auto;
    min-height: 100vh;
  }
  /* Temp */
  p {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 50px;
    height: 50px;
    background-color: gray;
    color: white;
  }
  p:nth-child(1) {
    background-color: red;
  }
  p:nth-child(2) {
    background-color: green;
  }
  p:nth-child(3) {
    background-color: blue;
  }
  /* End Temp */
</style>
