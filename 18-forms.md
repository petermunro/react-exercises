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

