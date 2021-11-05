<script>
	import { Tab, Nav, NavItem, NavButton, TabContent, TabPane } from './svelte-bootstrap-tab';
</script>

<main>
	<Tab class="tab-component">
		<Nav slot="nav-tabs">
			<NavItem>
				<NavButton tabId="home" active>Home</NavButton>
			</NavItem>
			<NavItem>
				<NavButton tabId="profile">Profile</NavButton>
			</NavItem>
			<NavItem>
				<NavButton tabId="contact">Contact</NavButton>
			</NavItem>
		</Nav>
		<TabContent slot="tab-content">
			<TabPane tabId="home">
				<h1>Home</h1>
			</TabPane>
			<TabPane tabId="profile">
				<h1>Profile</h1>
			</TabPane>
			<TabPane tabId="contact">
				<h1>Contact</h1>
			</TabPane>
		</TabContent>
	</Tab>
</main>

<style>
	/**/
</style>