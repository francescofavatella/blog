---
permalink: /react.html
---
# React
## How to css component
```
    file name should be <Component>.module.css
    import styles from './<Component>.module.css'

    className={styles.container}
```

## How to pass multiple props to a component (spread operator)
```
    const myProps={name='my-name', age=30}
    <MyComponent {...myprops} />

    <MyComponent name={myProps.name} age={myProps.age} />
```