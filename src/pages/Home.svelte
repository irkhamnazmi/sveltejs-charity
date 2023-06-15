<script>
  import { onDestroy } from "svelte";
  import CharityList from "../components/CharityList.svelte";
  import Header from "../components/Header.svelte";
  import Welcome from "../components/Welcome.svelte";
  import Promo from "../components/Promo.svelte";
  import Footer from "../components/Footer.svelte";
  import { xlink_attr } from "svelte/internal";
  // import { charities } from "../data/charities";
  //   let charities = ["Charity 1", "Charity 2", "Charity 3", "Charity 4"];

  // let charities = [];

  onDestroy(function () {
    window.scrollTo(0, 0);
  });
</script>

<Header />
<Welcome />
<!-- #preloader -->

<CharityList />

<Promo />
<Footer />
