
#### Updating State

Our `<Contact>` component is nice, but what we'd really like is an 'expandable' `<Contact>`:

*Unexpanded state:*

![Component in unexpanded state](images/component-in-unexpanded-state.png?raw=true)

*Expanded state:*

![Component in expanded state](images/component-in-expanded-state.png?raw=true)

1. Update your `<Contact>` to handle the two states. Don't worry about the fancy graphics - get it working. :-) One way to do this is to have an `isExpanded` state value that you update when you click it.

## Stretch Task

1. Write a `StarRating` component. The component should render 5 empty stars, and enable the user to click one of them to choose their rating. Display the rating in the console.

  > You can use these Unicode code points if that helps:

  ```js  
  const BLACK_STAR = "\u2605";
  const WHITE_STAR = "\u2606";
  ```
