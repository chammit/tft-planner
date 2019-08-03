<template>
	<div id="app">
		<div class="board">
			<div class="hex-row hex-row-odd">
				<div class="hex hex-top" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-top" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-top" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-top" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-top" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-top" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-top" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
			</div>
			<div class="hex-row hex-row-even">
				<div class="hex hex-mid" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-mid" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-mid" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-mid" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-mid" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-mid" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-mid" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
			</div>
			<div class="hex-row hex-row-odd">
				<div class="hex hex-bot" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-bot" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-bot" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-bot" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-bot" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-bot" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="hex hex-bot" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop">
					<!-- <div class="occupied"> -->
						<!-- <div class="hex-img-div"> -->
							<!-- <img src="./assets/images/champions/Lucian.png" class="hex-img"> -->
							<!-- <div class="hex-star-bg">
								<img src="./assets/images/star.png">
								<img src="./assets/images/star.png">
							</div> -->
						<!-- </div> -->
						<!-- <div class="hex-trait-div">
							<div>
								<img src="./assets/images/tft-assets/trait_icon_noble.png">
							</div>
							<div>
								<img src="./assets/images/tft-assets/trait_icon_gunslinger.png">
							</div>
						</div> -->
						<!-- <div class="hex-item-div">
							<div>
								<img src="./assets/images/tft-assets/tft_item_cursedblade.tft.png">
							</div>
							<div>
								<img src="./assets/images/tft-assets/tft_item_redbuff.tft.png">
							</div>
							<div>
								<img src="./assets/images/tft-assets/tft_item_swordbreaker.tft.png">
							</div>
						</div> -->
					<!-- </div> -->
				</div>
			</div>
			<div class="bench-row">
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
				<div class="bench-square" @dragenter="handleDragEnter" @dragleave="handleDragLeave" @dragover="handleDragOver" @drop="handleDrop"></div>
			</div>
		</div>
		<div class="selections">
			<div class="champions">
				<div @dragstart="handleDragStart" @dragend="handleDragEnd" draggable="true" class="champion" v-for="(champion, index) in champions" :key="index">
					<img :src="getImage(champion.name)">
					<p>{{champion.name}}</p>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import _ from 'lodash';
import tft_data from './assets/data/tft.json';

export default {
	name: 'app',
	components: {
	},
	data() {
		return {
			champions: [],
			dragSrcEl: null
		};
	},
	created() {
		this.champions = _.orderBy(tft_data.champions, 'name', 'asc');
	},
	methods: {
		getImage(championName) {
			let newChampionName = championName.replace(/[\s.'&*+?^${}()|[\]\\]/g, '');
			return `./images/champions/${newChampionName}.png`;
		},
		handleDragStart(e) {
			// console.log(e);
			e.target.style.opacity = '0.5';
			this.dragSrcEl = e.target;
			// e.dataTransfer.effectAllowed = 'move';
			// this.files = e.dataTransfer.files;
			// e.dataTransfer.setDragTest('hi');
		},
		handleDragEnd(e) {
			e.target.style.opacity = '1';
		},
		handleDragEnter(e) {
			e.target.classList.add('over');
		},
		handleDragLeave(e) {
			e.target.classList.remove('over');
		},
		handleDragOver(e) {
			if (e.preventDefault) {
				e.preventDefault();
			}
			// e.dataTransfer.dropEffect = 'move';
			return false;
		},
		handleDrop(e) {
			if (e.stopPropagation) {
				e.stopPropagation();
			}
			// console.log(this.dragSrcEl);
			console.log(e);
			e.target.classList.remove('over');
			// e.preventDefault();
			// e.target.style.background = `url(${this.dragSrcEl.src})`;
			// e.target.style.backgroundSize = `100% 100%`;

			let testEl = document.createElement('div');
			testEl.className = 'occupied';
			let testEl2 = document.createElement('div');
			testEl2.className = 'hex-img-div';
			testEl.appendChild(testEl2);
			let testEl3 = document.createElement('img');
			testEl3.className = 'hex-img';
			testEl3.src = this.dragSrcEl.src;
			testEl2.appendChild(testEl3);

			e.target.appendChild(testEl);

			return false;
		}
	}
};
</script>

<style lang="scss">
html, body, #app {
	width: 100%;
	height: 100%;
	margin: 0;
}

html {
	background: #000;
	color: #fff;
}

#app {
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}

.board {
	// background: url('./assets/images/board_bg2.jpg') no-repeat;
	// background-size: contain;
	// background-size: 1200px 455px;
	// width: 1200px;
	// height: 455px;
}

[draggable] {
	cursor: move;
}

.hex-row {
	white-space: nowrap;
	clear: left;
}

.hex {
	margin-top: 60px;
	margin-left: 30px;
	width: 104px;
	height: 60px;
	background-color: #6C6;
	position: relative;
	display: inline-block;

	&:hover {
		background-color: red;
	}

	&.over {
		background-color: blue;
	}
}

.hex:before {
	content: "";
	width: 0;
	height: 0;
	border-bottom: 30px solid #6C6;
	border-left: 52px solid transparent;
	border-right: 52px solid transparent;
	position: absolute;
	top: -30px;
}

.hex:after {
	content: "";
	width: 0;
	position: absolute;
	bottom: -30px;
	border-top: 30px solid #6C6;
	border-left: 52px solid transparent;
	border-right: 52px solid transparent;
}

.hex-row-odd {
	margin-left: 76px;
}

.hex-row-even {
	margin-left: 10px;
}

.hex:hover {
	background-color: red;

	&:before {
		border-bottom: 30px solid red;
	}

	&:after {
		border-top: 30px solid red;
	}
}

.bench-row {
	margin-top: 50px;
}

.bench-square {
	background: url("");
	background-color: #6C6;
	height: 104px;
	width: 104px;
	display: inline-block;
	margin-left: 15px;

	&:hover {
		background-color: red;
	}

	&.over {
		background-color: blue;
	}
}

.champions {
	margin-top: 15px;
	margin-left: 4px;
	display: flex;
	flex-wrap: wrap;
	justify-content: flex-start;
	align-content: stretch;
}

.champion {
	font-size: 14px;

	img {
		height: 90px;
		width: 90px;
	}
}

.occupied {
	height: 120px;
	width: 104px;
	margin-top: -31px;
	position: absolute;
	z-index: 1;
	text-align: center;

	div.hex-img-div {
		clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
	}  

	img.hex-img {
		height: 100%;
		margin-left: -8px;
		margin-top: 1px;
	}

	div.hex-trait-div {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		display: flex;
		justify-content: center;

		div {
			clip-path: polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%);
			
			&:nth-child(1) {
				background-color: #d4a501;
			}

			&:nth-child(2) {
				background-color: #a0410d;
			}
		}

		img {
			height: 25px;
		}
	}

	div.hex-star-bg {
		background-color: rgba(0, 0, 0, .5);
		width: 100%;
		height: 50px;
		margin-top: -50px;
		position: absolute;

		img {
			height: 15px;
		}
	}

	div.hex-item-div {
		width: 100%;
		display: flex;
		justify-content: center;
		margin-top: -30px;
		position: absolute;
		z-index: 1;

		img {
			height: 25px;
			margin: 0 1px;
			border: 1px solid #fff;
		}
	}
}
</style>
