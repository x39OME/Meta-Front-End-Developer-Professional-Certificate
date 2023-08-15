# Self-review: Implementing scroller position with render props

1. Considering the `MousePosition` component receives a prop called `render`, which is a function, what are valid options of JSX returned from the component?
    -   ```jsx
        return render({ mousePosition });
        ```
    -   ```jsx
        return (
            <div>
                render({mousePosition})
            </div>
        ); 
        ```
    -   ```jsx
        return render(<div>{mousePosition}</div>); 
        ```
    ```
    A: return render({ mousePosition });
    ```

2. The `PointMouseLogger` component returns the below JSX. 
    ```jsx
    <p>
        ({mousePosition.x}, {mousePosition.y})
    </p>
    ```
    After incorporating the `MousePosition` component as part of the JSX returned by `PointMouseLogger`, what should be the new JSX that `PointMouseLogger` returns
    -   ```jsx
        return(
            <MousePosition>
                {({ mousePosition }) => (
                    <p>
                        ({mousePosition.x}, {mousePosition.y})
                    </p>
                )}
            </MousePosition>
        );
        ```
    -   ```jsx
        return(
            <MousePosition>
                <p>
                    ({mousePosition.x}, {mousePosition.y})
                </p>
            </MousePosition>
        );
        ```
    -   ```jsx
        return(
            <MousePosition
                render={({ mousePosition }) => (
                    <p>
                        ({mousePosition.x}, {mousePosition.y})
                    </p>
                )}
            />
        );
        ```
    ```
    A: return(
                <MousePosition
                    render={({ mousePosition }) => (
                        <p>
                            ({mousePosition.x}, {mousePosition.y})
                        </p>
                    )}
                />
            );
    ```

3. The App component initially presents the below output structure
    ```jsx
    function App() {
        return(
            <div className="App">
                <header className="Header">Little Lemon Restaurant 🍕</header>
                <PanelMouseLogger />
                <PointMouseLogger />
            </div>
        );
    }
    ```
    After adding the MousePosition component into the mix, would you still have to perform any changes to the App component?
    - No
    - Yes
    ```
    A: No
    ```
