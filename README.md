
##CommonPopup

### Development

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
### Guide 
Instructions for using dynamic-dialog<br>
1. Using in dynamic-dialog tag <br>
Eg: <dynamic-dialog header-text="Input dialog" hidden-footer ....
- Using attributes don't transmit values same as paper-dialog 
(eg: no-cancel-on-outside-click, with-backdrop ...)
- Customize properties do not transmit values:
    + hidden-footer
    + hidden-cancel-button
    + hidden-ok-button
- Customize properties transmit values:<br>
    a. Transmit text<br>
    <table>
        <tr>
            <td>Attributes</td>
            <td>Description</td>
            <td>Default value</td>
            <td>Eg</td>
        </tr>
        <tr>
            <td>header-text</td>
            <td></td>
            <td>Input dialog</td>
            <td>header-text="Change password dialog"</td>
        </tr>
        <tr>
            <td>cancel-label</td>
            <td></td>
            <td>Cancel</td>
            <td>cancel-label="Cancel"</td>
        </tr>
        <tr>
            <td>ok-label</td>
            <td></td>
            <td>OK</td>
            <td>ok-label ="OK"</td>
        </tr>
        <tr>
            <td>content-message</td>
            <td>Use for confirm-dialog, notification-dialog</td>
            <td>Do you want to continue?</td>
            <td>content-message="Do you want to delete this item?   "</td>
        </tr>
    </table>
    <br>
    b. Transmit function<br>
    <br>
    <table>
        <tr>
            <td>Attributes</td>
            <td>Description</td>
            <td>Eg</td>
        </tr>
        <tr>
            <td>on-cancel-click</td>
            <td>function implementation when click Cancel button</td>
            <td></td>
        </tr>
        <tr>
            <td>on-ok-click</td>
            <td>function implementation when click OK button</td>
            <td>on-ok-click="submitChangeForm"</td>
        </tr>
    </table>
2. Content inside <dynamic-dialog>"This content" </dynamic-dialog>.<br>
    Default is the html content of the dialog body.<br>
    You can add **title icon** by using tag contains slot="titleIcon".
    Eg: \<img slot="titleIcon" class="title-img" src="images/icon_share.png"/> .<br>
    Change **close icon** by using tag contains slot="closeIcon".
    Eg: \<img slot="closeIcon" class="close-img" src="images/ic_close_48px_white.png"/>. 
<br>
    3. Other customize style element, using in dynamic-dialog tag <br>
    <table>
        <tr>
            <td><b>Attributes</b></td>
            <td><b>Description</b></td>
            <td><b>Eg</b></td>
        </tr>
        <tr>
            <td>header-style</td>
            <td>style for element</td>
            <td> header-style="background-color: #1E88E5; "</td>
        </tr>
        <tr>
            <td>&nbsp;&nbsp;&nbsp;header-left-style</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;title-icon-style</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;header-text-style</td>
            <td></td>
            <td>header-text-style="color:white;"</td>
        </tr>
        <tr>
            <td>&nbsp;&nbsp;&nbsp;close-btn-style</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>body-style</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>footer-style</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;&nbsp;&nbsp;cancel-btn-style</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>&nbsp;&nbsp;&nbsp;ok-btn-style</td>
            <td></td>
            <td></td>
        </tr>
    </table>
