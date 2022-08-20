<script>
	import '../app.css';

    let open = false

    function handleClick() {
        open = !open
    }
</script>

<div class="container">
	<div class="card">
		<div class="imgBg">
			<img class="imgDrawer" src="images/drawers.jpg" alt="" />
		</div>
		<div class="content">
			<h1 class="headerContent">
				Shift the overall look and feel by adding these wonderful touches to furniture in your home
			</h1>
			<p class="subContent">
				Ever been in a room and felt like something was missing? Perhaps it felt slightly bare and
				uninviting. I’ve got some simple tips to help you make any room feel complete.
			</p>
			<div class="profile">
				<div class="personal">
					<img class="imgPersonal" src="images/avatar-michelle.jpg" alt="" />
					<div class="dataPersonal">
						<p class="name">Michelle Appleton</p>
						<p class="date">26 Jun 2022</p>
					</div>
				</div>
				<div class="toolTip">
					<button class="btn" on:click={handleClick}>
						<img src="images/icon-share.svg" alt="" />
					</button>
                    {#if open}
                    <div class="share">
						<p style="color: var(--darkBlue);">SHARE</p>
						<div class="socialMedia">
							<img class="icon" src="images/icon-facebook.svg" alt="" />
							<img class="icon" src="images/icon-twitter.svg" alt="" />
							<img class="icon" src="images/icon-pinterest.svg" alt="" />
						</div>
					</div>
                    {/if}
					
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.container {
		width: 100vw;
		height: 100vh;
		display: flex;
		justify-content: center;
	}

	.card {
		display: flex;
		margin: auto;
		width: 50%;
		border: 1px solid var(--blueGrayish);
		border-radius: 10px;
		background-color: white;
		box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
	}

	.imgBg {
		width: 40%;
	}

	.imgDrawer {
		width: 100%;
		border-top-left-radius: 10px;
		border-bottom-left-radius: 10px;
	}

	.content {
		width: 60%;
		padding: 0px 20px;
	}

	.headerContent {
		font-size: 18px;
		padding: 20px;
		letter-spacing: 1px;
	}

	.subContent {
		padding: 10px 20px;
		line-height: 1.2rem;
	}

	.profile {
		display: flex;
		justify-content: space-between;
		padding: 10px 20px;
		width: 100%;
	}

	.personal {
		display: flex;
		align-items: center;
		position: relative;
	}

	.imgPersonal {
		width: 40px;
		height: 40px;
		border-radius: 50%;
	}

	.dataPersonal {
		margin-left: 10px;
	}

	.name {
		font-weight: 700;
		margin-bottom: 5px;
	}

	.date {
		color: var(--darkGrayish);
	}

	.btn {
		display: flex;
		justify-content: center;
		align-items: center;
		border-radius: 50%;
		/* background-color: var(--darkBlue); */
		border: 1px solid var(--lightBlue);
		width: 30px;
		height: 30px;
		cursor: pointer;
	}

	.btn:hover {
		background-color: var(--darkGrayish);
	}

	.toolTip {
		position: relative;
	}

	.share {
		position: absolute;
		bottom: 60px;
		right: -80px;
		background-color: var(--darkGrayish);
		padding: 10px;
		border-radius: 10px;
		display: flex;
		width: 200px;
		justify-content: space-evenly;
		align-items: center;
	}

	.share::after {
		content: '';
		position: absolute;
		top: 100%;
		left: 50%;
		margin-left: -5px;
		border-width: 5px;
		border-style: solid;
		border-color: var(--darkGrayish) transparent transparent transparent;
	}

	.socialMedia {
		display: flex;
		align-items: center;
		width: 50%;
		justify-content: space-around;
	}

	.icon {
		width: 15px;
		height: 15px;
        cursor: pointer;
	}

	@media only screen and (max-width: 768px) {
		.container {
			padding: 50px;
		}
		.card {
			flex-direction: column;
		}

		.imgBg {
			width: 100%;
		}

		.imgDrawer {
			width: 100%;
			border-top-right-radius: 10px;
			border-bottom-left-radius: 0px;
		}

		.content {
			width: 100%;
			padding: 10px;
		}

		.headerContent {
			font-size: 18px;
			padding: 10px;
			letter-spacing: 0px;
		}
	}
</style>
