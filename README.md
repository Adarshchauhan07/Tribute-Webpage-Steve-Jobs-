1. Higher Order Component

export const withLabelRestaurantsCard = (RestaurantsCard) => {
	return (restaurants) => {
		return (
			<div>
				<label>Promoted</label>
				<RestaurantsCard {...restaurants} />
			</div>
		);
	};
};


import RestaurantsCard, { withLabelRestaurantsCard } from "./RestaurantsCard";

const LabeledRestaurantsCard = withLabelRestaurantsCard(RestaurantsCard);

<LabeledRestaurantsCard
	key={restaurants.info.id}
	restaurants={restaurants.info}
/>
