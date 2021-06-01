<template>
	<g-link class="logo" to="/">
	  <g-image alt="Author image" class="author__image" src="~/assets/images/aircrft-logo.png" width="180" height="180" blur="5" />
	  <span class="logo__text">
	    &larr; {{ $static.metadata.siteName }}
	  </span>
	</g-link>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style lang="scss">
.logo {
	text-decoration: none;
  color: var(--body-color)!important;
  font-size: .9em;

	&__image {
		vertical-align: middle;
		border-radius: 99px;
		height: 40px;
		width: 40px;
		margin-right: .5em;
	}
}
</style>
