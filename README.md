# get-live-count

The purpose of using this package is to show the live user count on the current app. It uses socket.io package for managing the live user count.

### Usage
install liveusercount package
```
npm i liveusercount
```

install the socket.io package

```
npm i socket.io
```

or add CDN link for socket.io
```
<script src="https://cdn.socket.io/4.0.0/socket.io.min.js" integrity="sha384-DkkWv9oJFWLIydBXXjkBWnG1/fuVhw8YPBq37uvvD6WSYRFRqr21eY5Dg9ZhmWdy" crossorigin="anonymous"></script>
```

go to user root component and inside the useEffect hook add call this function

```
import React from 'react';
import getLiveCount from 'liveusercount'
const RootComponent = () => {
    React.useEffect(() =>{
        const config = {
            text: "Live user : ",
            backgroundColor: "red",
            textColor: "white",
            position: "absolute",
            top: "0px",
            left: "0px"
        }
        getLiveCount(config);
    }, []);
    return (
        <div></div>
    );
};

export default RootComponent;

```

it will automatically generate the section for the live count on the top left of the page.

### Customization

You can apply your own css on the class **live-count-class**.

and also you can configure some of its property in config object

| Paramteter | Description | Default | optional |
| :---    | :----| :---- | ----: |
| text | It is the text to be shown before the count | Live user | true|
| backgroundColor | Background color for the text wrapper | black | true|
| textColor | It is the color of the text to be shown | white | true|
| position | It is position configuration for the text wrapper  | absolute user | true|
| top | It is top value for the position | 0px | true|
| left | It is left value for the position | 0px | true|



