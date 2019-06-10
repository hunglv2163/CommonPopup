## Development

In order to run it locally you'll need to fetch some dependencies and a basic server setup.

1. Install [bower](http://bower.io/) & [polyserve](https://npmjs.com/polyserve):

    ```sh
    $ npm install -g bower polyserve
    ```

2. Install local dependencies:

    ```sh
    $ bower install
    ```

3. Start development server and open `http://localhost:8081/components/hello-world-polymer/`.

    ```sh
    $ polyserve
    ```
## Guide 
Instructions for using dynamic-dialog<br>
1. Using in dynamic-dialog tag <br>
Eg: <dynamic-dialog header-text="Input dialog" hidden-footer ....
- Using attributes don't transmit values same as paper-dialog 
(eg: no-cancel-on-outside-click, with-backdrop ...)
- Customize properties do not transmit values:
    + hidden-footer
    + hidden-cancel-button
    + hidden-ok-button
- Customize properties transmit values:
    1. Transmit text<br>
    | Attributes       | Description                                   | Default value            | Eg                                                     |
    |------------------|-----------------------------------------------|--------------------------|--------------------------------------------------------|
    | header\-text     |                                               | Input dialog             | header\-text="Change password dialog"                  |
    | cancel\-label    |                                               | Cancel                   | cancel\-label="Cancel"                                 |
    | ok\-label        |                                               | OK                       | ok\-label ="OK"                                        |
    | content\-message | Use for confirm\-dialog, notification\-dialog | Do you want to continue? | content\-message="Do you want to delete this item?   " |
    <br>
    2. Transmit function<br>
    | Attributes        | Description                                      | Eg                |
    |-------------------|--------------------------------------------------|-------------------|
    | on\-cancel\-click | function implementation when click Cancel button | on\-cancel\-click |
    | on\-ok\-click     | function implementation when click OK button     | on\-ok\-click     |
    <br>
2. Content inside <dynamic-dialog>"This content" </dynamic-dialog>.<br>
    Default is the html content of the dialog body.<br>
    You can add **title icon** by using tag contains slot="titleIcon".
    Eg: \<img slot="titleIcon" class="title-img" src="images/icon_share.png"/> .<br>
    Change **close icon** by using tag contains slot="closeIcon".
    Eg: \<img slot="closeIcon" class="close-img" src="images/ic_close_48px_white.png"/>. 
<br>
3. Other customize style element, using in dynamic-dialog tag <br>
    | Attributes                  | Description       | Eg                                             |
    |-----------------------------|-------------------|------------------------------------------------|
    | header\-style               | style for element |  header\-style="background\-color: \#1E88E5; " |
    |    header\-left\-style      |                   |                                                |
    |         title\-icon\-style  |                   |                                                |
    |         header\-text\-style |                   | header\-text\-style="color:white;"             |
    |    close\-btn\-style        |                   |                                                |
    | body\-style                 |                   |                                                |
    | footer\-style               |                   |                                                |
    |    cancel\-btn\-style       |                   |                                                |
    |    ok\-btn\-style           |                   |                                                |
    |                             |                   |                                                |

