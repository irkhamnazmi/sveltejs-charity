<script>
  import CharityList from "../components/CharityList.svelte";
  import Header from "../components/Header.svelte";
  import Welcome from "../components/Welcome.svelte";
  import Promo from "../components/Promo.svelte";
  import Footer from "../components/Footer.svelte";
  import Loader from "../components/Loader.svelte";
  // import { charities } from "../data/charities";
  //   let charities = ["Charity 1", "Charity 2", "Charity 3", "Charity 4"];
  let title = "Charity";
  let data = getData();

  let charities = [];

  async function getData() {
    const res = await fetch(" https://bwacharity.fly.dev/charities");
    const data = await res.json();

    if (res.ok) {
      return data;
    } else {
      throw new Error(data);
    }
  }
</script>

<Header />
<Welcome />
{#await data}
  <Loader />
  <!-- #preloader -->
{:then charities}
  <CharityList {charities} />
{/await}
<Promo />
<Footer />
