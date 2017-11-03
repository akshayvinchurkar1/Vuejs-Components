<template>
	<div class="navbar">
		<ul>
			<li v-for="navbarlink in links">
				<a v-bind:href="''+navbarlink.linkaddress+''">{{ navbarlink.linkname }}</a>
			</li>
		</ul>
	</div>
</template>

<script>
export default {
  name: 'navbar',
  data () {
    return {
      links: [{linkname: 'Home', linkaddress: 'https://www.google.com'}, {linkname: 'About', linkaddress: 'https://www.google.com'}, {linkname: 'Blog', linkaddress: 'https://www.google.com'}, {linkname: 'Author', linkaddress: 'https://www.google.com'}, {linkname: 'Work', linkaddress: 'https://www.google.com'}]
    }
  }
}
</script>

<style scoped>
	.navbar {
		width: 100%;
		height: 100px;
		background-color: #333;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.navbar ul {
		 list-style: none;
	}

	.navbar ul li {
		 display: inline-block;
		 list-style: none;
		 margin-right: 40px;
	}

	.navbar ul li a{
		 text-decoration: none;
		 color: #fff;
		 font-size: 14px;
		 text-transform: uppercase;
		 font-weight: 400;
	}
</style>