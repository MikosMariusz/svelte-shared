<div class="container">
	<svg
		class="h-full w-full"
		xmlns="http://www.w3.org/2000/svg"
		viewBox="0 0 600 400"
		preserveAspectRatio="xMidYMid slice"
	>
		<!-- Gradienty -->
		<defs>
			<radialGradient id="sunGradient" cx="0.5" cy="0.5" r="0.5">
				<stop offset="0%" stop-color="#FFEBB8" />
				<stop offset="60%" stop-color="#ffec7f" />
				<stop offset="100%" stop-color="#fcec96" />
			</radialGradient>
			<linearGradient id="sky" x1="0" y1="0" x2="0" y2="1">
				<stop offset="0%" stop-color="#87B5D6">
					<animate
						attributeName="stop-color"
						values="#87B5D6;#5C7081;#5C7081;#4A5663;#87B5D6"
						keyTimes="0;0.4;0.6;0.9;1"
						dur="30s"
						repeatCount="indefinite"
					/>
				</stop>
				<stop offset="100%" stop-color="#B0D0E8">
					<animate
						attributeName="stop-color"
						values="#B0D0E8;#7D9BAF;#5E6C77;#4A5663;#B0D0E8"
						keyTimes="0;0.4;0.6;0.9;1"
						dur="30s"
						repeatCount="indefinite"
					/>
				</stop>
			</linearGradient>
			<linearGradient id="far" x1="0" y1="0" x2="0" y2="1">
				<stop offset="0%" stop-color="#7FA878" />
				<stop offset="100%" stop-color="#5E8760" />
			</linearGradient>
			<linearGradient id="middle" x1="0" y1="0" x2="0" y2="1">
				<stop offset="0%" stop-color="#A8CBA4" />
				<stop offset="100%" stop-color="#7FA878" />
			</linearGradient>
			<linearGradient id="front" x1="0" y1="0" x2="0" y2="1">
				<stop offset="0%" stop-color="#BFD8B8" />
				<stop offset="100%" stop-color="#A8CBA4" />
			</linearGradient>
		</defs>

		<!-- Tło nieba -->
		<rect width="600" height="400" fill="url(#sky)" />

		<path id="sunPath" d="M -600,0 Q 300,-50 700,900" fill="none" stroke="none" />

		<!-- Słońce z gradientem -->
		<circle cx="450" cy="80" r="50" fill="url(#sunGradient)">
			<animateMotion repeatCount="indefinite" dur="30s">
				<mpath href="#sunPath" />
			</animateMotion>
		</circle>

		<!-- Gwiazdy -->
		<g id="stars">
			<circle cx="100" cy="100" r="1.5" fill="white">
				<animate
					attributeName="opacity"
					values="0;0;1;0"
					keyTimes="0;0.5;0.9;1"
					dur="30s"
					repeatCount="indefinite"
				/>
			</circle>
			<circle cx="200" cy="150" r="1.5" fill="white">
				<animate
					attributeName="opacity"
					values="0;0;1;0"
					keyTimes="0;0.5;0.9;1"
					dur="30s"
					repeatCount="indefinite"
				/>
			</circle>
			<circle cx="300" cy="80" r="1.5" fill="white">
				<animate
					attributeName="opacity"
					values="0;0;1;0"
					keyTimes="0;0.5;0.9;1"
					dur="30s"
					repeatCount="indefinite"
				/>
			</circle>
			<circle cx="400" cy="120" r="1.5" fill="white">
				<animate
					attributeName="opacity"
					values="0;0;1;0"
					keyTimes="0;0.5;0.9;1"
					dur="30s"
					repeatCount="indefinite"
				/>
			</circle>
			<circle cx="500" cy="200" r="1.5" fill="white">
				<animate
					attributeName="opacity"
					values="0;0;1;0"
					keyTimes="0;0.5;0.9;1"
					dur="30s"
					repeatCount="indefinite"
				/>
			</circle>
			<circle cx="600" cy="250" r="1.5" fill="white">
				<animate
					attributeName="opacity"
					values="0;0;1;0"
					keyTimes="0;0.5;0.9;1"
					dur="30s"
					repeatCount="indefinite"
				/>
			</circle>
		</g>

		<!-- Warstwy gór -->
		<g id="layer1">
			<path
				d="M0,250 Q50,200 100,230 T200,210 T300,240 T400,220 T500,250 T600,240 T700,260 T800,250 L800,400 L0,400 Z"
				fill="url(#far)"
			/>
		</g>
		<g id="layer2">
			<path
				d="M0,280 Q60,240 120,260 T240,240 T360,270 T480,250 T600,270 T720,250 T800,280 L800,400 L0,400 Z"
				fill="url(#middle)"
			/>
		</g>
		<g id="layer3">
			<path
				d="M0,310 Q80,270 160,290 T320,280 T480,310 T640,300 T800,310 L800,400 L0,400 Z"
				fill="url(#front)"
			/>
		</g>
	</svg>
</div>

<style>
	.container {
		width: 100%;
		height: 100%;
		background-color: red;
	}
</style>
