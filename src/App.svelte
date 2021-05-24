<script>
	import TextAreaInput from "./TextAreaInput.svelte";
	import TextAreaOutput from "./TetAreaOutput.svelte";
	let input = "";
	let output = "";

	function upperCase(){
		output = input.toUpperCase();
		document.getElementById("focus_id").focus();
	}

	function lowerCase(){
		console.log("Wololox ");
		output = input.toLowerCase();
		document.getElementById("focus_id").focus();
	}

	function capitalCase(){
		console.log("Wololo ");
		output = input.replace(/(^\w{1})|(\s{1}\w{1})/g, match => match.toUpperCase());
		document.getElementById("focus_id").focus();
	}
</script>


<div class="main">

	<p>Made with:  </p>
	<div id="logo">
		<img src="img/Svelte_Logo.png" alt="">
	</div>

	<TextAreaInput bind:input_text={input}></TextAreaInput>

	<div id="buttons">
		<button on:click={upperCase}>UPPER CASE</button>
		<button on:click={lowerCase}>lower case</button>
		<button on:click={capitalCase}>Capitalized Case</button>
	</div>

	<TextAreaOutput input_text={output}></TextAreaOutput>

</div>



<style>

	p{
		display: flex;
		justify-content: center;
		font-family: Roboto;
		font-style: normal;
		font-weight: normal;
		font-size: 12px;
		line-height: 14px;

		color: #FFFFFF;
	}	

	#logo{
		display: flex;
		justify-content: center;
	}

	img{
		width: 79px;
		margin-top: 5px;
	}

	#buttons{
		margin-top: 19px;
		display: flex;
		justify-content: center;
	}

	button{
		width: 220px;
		height: 60px;
		left: 264px;
		top: 362px;
		background: #7E44F8;
		border-radius: 15px;
		margin-left: 40px;
		margin-right: 40px;
		outline: none;
		border: 0px solid #7E44F8;
		cursor: pointer;

		font-family: Roboto;
		font-style: normal;
		font-weight: normal;
		font-size: 24px;
		line-height: 28px;

		color: #FFFFFF;
	}

	button:hover{
		background: #9462ff;
	}

</style>