# Forms

## A Twitter/SMS Input Component

This exercise examines how to use and manage input events for form components.

1. Create an input component for composing tweets (or SMS/text messages).
   Your component should display the character count remaining
   whenever a character is typed.
   Your component should display three things:
     - The main text input field
     - The character count
     - A "Send" button to ultimately send the message

#### Handling the message send

A parent component might want to use your component like this:

  ```js
  function MyParentComponent {
    handleSend(message) {
      // send the message
    }

    return (
      <TweetBox onSend={handleSend} />
    );
  }
  ```

1. Have your component call the parent's supplied `onSend` prop when the user presses the "Send" button.

  > The TweetBox is responsible for collecting the data to send, but it doesn't know _how_ to send it (eg via SMS, twitter etc). That's the parent's responsibility.

  >  So it calls up to its parent to do that, passing it the message to send.

  > The `handleSend()` in the parent is the callback that TweetBox will ultimately call to send the message.



## Stretch Task

### Creating an 'Edit Invoice' Component

The plan here is to create a component that enables us to edit an invoice.

1. View the [screen mockup](images/edit-invoice-screen.pdf).

2. Build a React component for this screen. It should:
   - display the invoice recipient's name and address at the top - don't worry about editing this here;
   - enable you to enter line items one by one, and delete line items you are no longer interested in;
   - compute the grand total of all the line items.

### Hints

- Think about how you will break this down into smaller components.
- Build it step-by-step - get one piece working well, then move on to the next.
- When building a component, focus on its _external_ API first. What should it be called? What props should it receive? Should it be passed any callbacks, and if so what should they be called, and what arguments will they take?
- You can even 'call' a component using its external API, and just 'mock' its internal details until you need to render it.

