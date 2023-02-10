## Table of Contents

- [Ternary Operators](#ternary operators)

## Ternary Operator

Display users name if it exists, otherwise display the name from the email address and split at @

```jsx
        <div className="font-bold">
                        {user?.displayName || user.email?.split("@")[0]}
                      </div>
                      ```
