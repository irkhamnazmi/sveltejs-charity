<script>
  import CharityList from "../components/CharityList.svelte";
  import Header from "../components/Header.svelte";
  import Welcome from "../components/Welcome.svelte";
  import Promo from "../components/Promo.svelte";
  import Footer from "../components/Footer.svelte";
  import { charities } from "../data/charities";
  //   let charities = ["Charity 1", "Charity 2", "Charity 3", "Charity 4"];
  let title = "Charity";
</script>

<Header />
<Welcome />
<Promo />
<CharityList {charities} />
<Footer />
