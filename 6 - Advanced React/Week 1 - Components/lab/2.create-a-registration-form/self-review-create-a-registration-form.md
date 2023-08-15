# Self-review: Create a registration form

1. When setting a new value for the password state, that is represented by an object with two properties, `value` and `isTouched`, what’s the correct call to the `setPassword` state setter inside the `onChange` event handler? Select all that apply.
    -   ```jsx
        setPassword({ ...password, value: e.target.value }); 
        ```
    -   ```jsx
        setPassword({ isTouched: false, value: e.target.value }); 
        ```
    -   ```jsx
        setPassword({ value: e.target.value }); 
        ```
    ```
    A: setPassword({ ...password, value: e.target.value }); 
    ```

2. What’s the correct event prop you should use to determine when an input has been interacted with at least once? Select all that apply.
    - `onFocus`
    - `onBlur`
    - `onChange`
    ```
    A: onBlur
    ```

3. How do you prevent the default behavior of the `form` HTML tag in React when a submission event occurs?
    - By returning `false` from the `onSubmit` function prop that the `form` tag provides. 
    - By calling `preventDefault` on the event object inside any `onChange` handler from an `input` tag.
    - By calling `preventDefault` on the event object inside the `onSubmit` function prop from the `form` tag. 
    ```
    A: By calling preventDefault on the event object inside the onSubmit function prop from the form tag. 
    ```
