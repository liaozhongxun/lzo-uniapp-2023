<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		},
		globalData: {
			name: 'lzo'
		}
	}
</script>

<style>
	/*每个页面公共css */
	@import url('./static/css/base.scss');

	.globalTestClass {
		background-color: #f00 !important;
	}

	page {
		border: 1px solid #f0f;
		width: 100%;
		height: 100%;
	}
</style>
