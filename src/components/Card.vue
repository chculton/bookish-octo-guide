<template>
	<div class="card">
		<div class="card-picture">
			<slot name="picture"></slot>
		</div>

		<div class="content-area">
			<div>
				<slot name="title"></slot>
			</div>
			<div>
				<slot name="card-content"></slot>
			</div>
		</div>
	</div>
</template>

<style>
	.card {
		box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
		border-radius: 5px;
		transition: 0.3s;
		display: flex;
		flex-direction: row;
		min-height: 10rem;
		cursor: pointer;
		background: #101010;
		margin-bottom: 1rem;
	}

	.card:hover {
		box-shadow: 0 8px 16px 0 rgba(0, 0, 0, 0.2);
	}

	.content-area {
		padding: 2px 16px;
		margin: 1rem;
		display: flex;
		flex-direction: column;
	}

	img {
		border-radius: 5px 0 0 5px;
		width: 10rem;
		height: 10rem;
	}

	@media (max-width: 600px) {
		.card {
			height: auto;
			min-height: 10rem;
		}

		.card-picture img {
			visibility: hidden;
			border-radius: 0;
			width: 0rem;
			height: 0rem;
		}
	}
</style>
