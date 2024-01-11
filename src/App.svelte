<script>
  import Modal from "./Modal.svelte";

  export let name;
  let count = 0;
  const counter = () => {
    count++;
  };

  let products = [
    {
      name: "candy",
      price: "200",
    },
    {
      name: "pencil",
      price: "30",
    },
    {
      name: "pen",
      price: "10",
    },
  ];

  let sampletext = "lorem";

  const changeText = () => {
    sampletext = "ispum dei rv";
  };

  const handleInput = (e) => {
    sampletext = e.target.value;
  };

  let backgroundColor = "";
  let textColor = "";

  const changeBcolor = () => {
    if (backgroundColor == "white" && textColor == "black") {
      backgroundColor = "#607274";
      textColor = "#FBF9F1";
    } else {
      backgroundColor = "white";
      textColor = "black";
    }
  };

  let firstName = "John";
  let lastName = "Doe";
  $: fullName = firstName + " " + lastName;

  let number, result;

  function squared(number) {
    result = Math.pow(number, 2);
    return result;
  }

  let grossSalary,
    incomeTax = 0;
  function calculateIncomeTax(grossSalary) {
    if (grossSalary > 10000 && grossSalary < 24000) {
      incomeTax = grossSalary * 0.05;
    } else if (grossSalary > 24000 && grossSalary < 36000) {
      incomeTax = grossSalary * 0.1;
    } else if (grossSalary > 36000 && grossSalary < 48000) {
      incomeTax = grossSalary * 0.15;
    } else if (grossSalary > 48000 && grossSalary < 60000) {
      incomeTax = grossSalary * 0.175;
    } else if (grossSalary > 60000 && grossSalary < 72000) {
      incomeTax = grossSalary * 0.19;
    } else {
      incomeTax = 0;
    }
    return incomeTax;
  }

  let people = [
    { name: "yoshi", beltColour: "black", age: 25, id: 1 },
    { name: "mario", beltColour: "orange", age: 45, id: 2 },
    { name: "luigi", beltColour: "brown", age: 35, id: 3 },
  ];

  const deletePeople = (id) => {
    people = people.filter((person) => person.id != id);
  };
  let num = 4;
  let showModal = false;

  const toggleModal = () => {
    showModal = !showModal;
  };
</script>

<Modal {showModal} on:click={toggleModal}>
  <!--   <h3>Add a new person</h3>
 -->
  <form action="" method="post">
    <input type="text" name="name" id="name" placeholder="name" />
    <input type="text" name="name" id="name" placeholder="beltColor" />
    <button>Add Person</button>
  </form>
  <div slot="title">
    <h3>Add a new person</h3>
  </div>
</Modal>

<main style="background-color: {backgroundColor}; color: {textColor}">
  <nav class="navbar">
    <ul>
      <li><a href="/home">Home</a></li>
      <li><a href="/about">About</a></li>
      <li><a href="/contact">Contact</a></li>
      <li><a href="/other">Other</a></li>
    </ul>
  </nav>
  <h1>Hello {name}!</h1>
  <button on:click|once={toggleModal}>Open Modal</button>
  <h3>The quick brown fox jumped over the fence</h3>
  <p>{count}</p>
  <button on:click={counter}>Add</button>

  {#each products as item}
    <ul>
      <li>{item.name} Ksh{item.price}</li>
    </ul>
  {/each}

  <h5>Changing text {sampletext}</h5>
  <button on:click={changeText}>Change</button>
  <br />
  <input type="text" bind:value={sampletext} />

  <br />
  <button on:click={changeBcolor}>Change colors</button>

  <br />
  <input type="text" bind:value={firstName} />
  <input type="text" bind:value={lastName} />
  <p>{fullName}</p>

  <input
    type="text"
    placeholder="Enter gross salary"
    bind:value={grossSalary}
  />
  <button on:click={calculateIncomeTax}>Calculate</button>

  <p>The income tax is {incomeTax}</p>

  {#each people as person (person.id)}
    <div>
      <h4>{person.name}</h4>
      {#if person.beltColour === "black"}
        <p><strong>MASTER NINJA</strong></p>
      {/if}
      <p>{person.age} years old, {person.beltColour} belt</p>
    </div>
    <button on:click={() => deletePeople(person.id)}>Delete</button>
  {:else}
    <p>There are no people to show</p>
  {/each}
  {#if num > 10}
    <p>Greater than 10</p>
  {:else if num < 10}
    <p>Less than 10</p>
  {/if}
</main>

<style>
  .navbar ul {
    display: flex;
    flex-direction: row;
  }
  .navbar ul li {
    margin: 10px;
  }
  main {
    text-align: center;
    padding: 1em;
    max-width: 240px;
    margin: 0 auto;
  }

  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }
  ul {
    list-style-type: none;
  }

  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
