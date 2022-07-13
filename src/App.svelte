<script>
	import MainContent from './components/MainContent/MainContent.svelte'
	(function() {
		document.addEventListener("mousemove", parralax)
		function parralax(e) {
			const elem = document.getElementById("elipse1")
			const elem2 = document.getElementById("elipse2")
			const elem3 = document.getElementById("elipse3")
			const elem4 = document.getElementById("elipse4")
			const elem5 = document.getElementById("elipse5")
			const elem6 = document.getElementById("elipse6")
			const elem7 = document.getElementById("elipse7")
			let _w = window.innerWidth/2
			let _h= window.innerHeight/2
			let _mouseX = e.clientX
			let _mouseY = e.clientY
			let _depth1 = `${50 - (_mouseX - _w) * 0.01}% ${50 - (_mouseY - _h) * 0.01}%`;
        	let _depth2 = `${50 - (_mouseX - _w) * 0.02}% ${50 - (_mouseY - _h) * 0.02}%`;
        	let _depth3 = `${50 - (_mouseX - _w) * 0.06}% ${50 - (_mouseY - _h) * 0.06}%`;
        	let x = `${_depth3}, ${_depth2}, ${_depth1}`;
			elem.style.right = `${50 - (_mouseX - _w) * 0.01}% `;
			elem.style.top = `${-70 - (_mouseY - _h) * 0.01}% `;
			elem2.style.left = `${80 - (_mouseX - _w) * 0.01}%`;
			elem2.style.top = `${10 - (_mouseY - _h) * 0.01}%`;
			elem3.style.left = `${90 - (_mouseX - _w) * 0.03}%`;
			elem3.style.top = `${5 - (_mouseY - _h) * 0.01}%`;
			elem4.style.left = `${85 - (_mouseX - _w) * 0.03}%`;
			elem4.style.top = `${40 - (_mouseY - _h) * 0.01}%`;
			elem5.style.left = `${10 - (_mouseX - _w) * 0.01}%`;
			elem5.style.top = `${80 - (_mouseY - _h) * 0.01}%`;
			elem6.style.left = `${5 - (_mouseX - _w) * 0.03}%`;
			elem6.style.top = `${75 - (_mouseY - _h) * 0.01}%`;
			elem7.style.left = `${65 - (_mouseX - _w) * 0.03}%`;
			elem7.style.top = `${70 - (_mouseY - _h) * 0.01}%`;

		}
	})();
</script>

<main>
	<div class="elipse" id="elipse">
	<div class="BigElipseRed" id="elipse1"></div>
	<div class="WhiteEllipse" id="elipse2"></div>
	<div class="SmallElipseRed" id="elipse3"></div>
	<div class="MediumElipseGray" id="elipse4"></div>
	<div class="WhiteEllipse" id="elipse5"></div>
	<div class="SmallElipseGray" id="elipse6"></div>
	<div class="BigElipseGray" id="elipse7"></div>
</div>
<MainContent/>
</main>

<style>
	main {
		z-index: -1;
		background-color: rgba(31, 35, 38, 1);
		width: 100%;
		height: 100%;
	}
	.elipse{
		width: 100%;
		height: 100%;
	}
	.BigElipseRed{
		position: absolute;
		background-color:rgba(255, 70, 86, 1);
		top: -600px;
		width: 70em;
		height: 70em;
		border-radius:50%;
	}
	
	.WhiteEllipse{
		position: absolute;
		background-color:rgba(239, 239, 239, 1);
		width: 268px;
		height: 268px;
		border-radius:50%;
		top:182px;
		right: 104px;
	}
	.SmallElipseRed{
		position: absolute;
		background-color:rgba(255, 70, 86, 1);
		width: 44px;
		height: 44px;
		border-radius:50%;
		top: 74px;
		right: 219px;
	}
	.MediumElipseGray{
		position: absolute;
		background-color:rgba(80, 81, 85, 1);
		width: 98px;
		height: 98px;
		border-radius:50%;
		top: 475px;
		right: 55px;
	}
	#elipse5{
		position: absolute;
		top: 750px;
		left: 177px;
		width: 400px;
		height: 400px;
	}
	.SmallElipseGray{
		position: absolute;
		background-color:rgba(80, 81, 85, 1);

		top: 700px;
		left: 112px;
		width: 63px;
		height: 63px;
		border-radius:50%;
	}
	.BigElipseGray{
		position: absolute;
		background-color: rgba(41, 44, 49, 1);
		width: 50em;
		height: 50em;
		top: 650px;
		border-radius:50%;
		right: -250px;
	}
</style>