<script>
  import AgeCalculator from "./AgeCalculator.svelte";
  import MathCalculator from "./MathCalculator.svelte";
  import CalorieCalculator from "./CalorieCalculator.svelte";
  import BMICalculator from "./BMICalculator.svelte";

	export let menu = 0;
</script>

<style>
	ul#menu li{
    display: inline;
    align-items: flex-end;
	}

  .card1 {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    width: 300px;
    height: 300px;
    left: calc(50% - 300px/2 - 524px);
    top: 301px;

    background: #28282B;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 16px;
  }

  .text1 {
    text-align: center;
    vertical-align: middle;
    position: relative;
    width: 177px;
    height: 29px;

    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 29px;
    /* identical to box height */

    letter-spacing: 0.384px;

    color: #FFFFFF;
  }

  .card2 {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    width: 300px;
    height: 300px;
    left: calc(50% - 300px/2 - 170px);
    top: 301px;

    background: #28282B;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 16px;
  }

  .text2 {
    position: relative;
    width: 191px;
    height: 29px;
    

    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 29px;
    /* identical to box height */

    letter-spacing: 0.384px;

    color: #FFFFFF;
  }

  .card3 {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    position: absolute;
    width: 300px;
    height: 300px;
    left: calc(50% - 300px/2 + 184px);
    top: 300px;

    background: #28282B;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 16px;
  }

  .text3 {
    position: relative;
    width: 175px;
    height: 29px;
    

    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 29px;
    /* identical to box height */

    letter-spacing: 0.384px;

    color: #FFFFFF;
  }

  .card4 {
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    width: 300px;
    height: 300px;
    left: calc(50% - 300px/2 + 538px);
    top: 300px;

    background: #28282B;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 16px;
  }

  .text4 {
    position: absolute;
    width: 215px;
    height: 29px;

    font-family: 'Inter';
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 29px;
    /* identical to box height */

    letter-spacing: 0.384px;

    color: #FFFFFF;

  }

ul {
  left: 0;
  margin-block-start: 0;
  margin: 0;
  padding: 0;
}

</style>

<ul id="menu" class="list">
	<li><a href="/" on:click|preventDefault={() => (menu = 1)}>AgeCalculator</a></li> |
	<li><a href="/" on:click|preventDefault={() => (menu = 2)}>MathCalculator</a></li> |
  <li><a href="/" on:click|preventDefault={() => (menu = 3)}>CalorieCalculator</a></li> |
  <li><a href="/" on:click|preventDefault={() => (menu = 4)}>BMICalculator</a></li>

</ul>

{#if menu === 1}
<AgeCalculator />
{:else if menu === 2}
<MathCalculator />
{:else if menu === 3}
<CalorieCalculator />
{:else if menu === 4}
<BMICalculator />
{:else}

<div class="card1">
<p class="text1">Age Calculator</p>
</div>

<div class="card2">
<p class="text2">Math Calculator</p>
</div>

<div class="card3">
<p class="text3">BMI Calculator</p>
</div>

<div class="card4">
  <p class="text4">Calorie Calculator</p>
  </div>

{/if}
