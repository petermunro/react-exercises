# Rendering a List of Items

You have already created a `<Contact>` component which renders an `<Address>` component. Now to create a component to render a list of contacts.

1. In your App.js, import this [contacts.json](contacts.json) file as a
   data source:

    ```js
    import contacts from './contacts.json';
    ```

    This makes the contacts available as a JS array. Try `console.log(contacts)` to verify.

2. Now write a component you will render in `App` like this:

    ```js
    function App() {
      return (
        <div className="App">
          // ...
          <ContactList contacts={contacts} />
          // ...
        </div> 
      )
    }
    ```

  Your `ContactList` component should take the array of contacts, and for each one, render a `Contact` to display it.
