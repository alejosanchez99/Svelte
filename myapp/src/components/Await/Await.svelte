<script>
  const breeds = ["affenpinscher", "african", "airedale"];
  let selectedBreed = breeds[0];
  let imageSrc;
  let hasError = false;
  let isFetching = false;

//   $: fetchDogImageAsync(selectedBreed);

//   async function fetchDogImageAsync(breed) {
//     try {
//       hasError = false;
//       isFetching = true;
//       imageSrc = null;
//       const response = await GetRandomDogImage(breed);
//       imageSrc = response.message;
//     } catch (error) {
//       console.log(error);
//       hasError = true;
//     } finally {
//       isFetching = false;
//     }
//   }

  async function GetRandomDogImage(breed) {
    const response = await fetch(
      `https://dog.ceo/api/breed/${breed}/images/random`
    );

    return await response.json();
  }
</script>

<select bind:value={selectedBreed}>
  {#each breeds as breed}
    <option value={breed}>{breed}</option>
  {/each}
</select>

Selected breed: {selectedBreed}

<hr />

{#await GetRandomDogImage(selectedBreed)}
  loading...
{:then obj}
  <img src={obj.message} alt="Dog" />
{:catch}
  Oops. something is wrong.
{/await}

<!-- {#if hasError}
  Oops. something is wrong.
{:else if isFetching}
  loading...
{:else}
  <img src={imageSrc} alt="Dog" />
{/if} -->
