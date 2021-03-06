# ion-loading-controller

Loading controllers programmatically control the loading component. Loadings can be created and dismissed from the loading controller. View the [Loading](../loading) documentation for a full list of options to pass upon creation.




<!-- Auto Generated Below -->


## Usage

### Javascript

```javascript
async function presentLoading() {
  const loadingController = document.querySelector('ion-loading-controller');
  await loadingController.componentOnReady();

  const loadingElement = await loadingController.create({
    message: 'Please wait...',
    spinner: 'crescent',
    duration: 2000
  });
  return await loadingElement.present();
}
```



## Methods

### `create(options?: LoadingOptions | undefined) => Promise<HTMLIonLoadingElement>`

Create a loading overlay with loading options.

#### Parameters

| Name      | Type                          | Description                               |
| --------- | ----------------------------- | ----------------------------------------- |
| `options` | `LoadingOptions \| undefined` | The options to use to create the loading. |

#### Returns

Type: `Promise<HTMLIonLoadingElement>`



### `dismiss(data?: any, role?: string | undefined, id?: string | undefined) => Promise<boolean>`

Dismiss the open loading overlay.

#### Parameters

| Name   | Type                  | Description                                                                                                                                                                                                                                         |
| ------ | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `data` | `any`                 | Any data to emit in the dismiss events.                                                                                                                                                                                                             |
| `role` | `string \| undefined` | The role of the element that is dismissing the loading. This can be useful in a button handler for determining which button was clicked to dismiss the loading. Some examples include: ``"cancel"`, `"destructive"`, "selected"`, and `"backdrop"`. |
| `id`   | `string \| undefined` | The id of the loading to dismiss. If an id is not provided, it will dismiss the most recently opened loading.                                                                                                                                       |

#### Returns

Type: `Promise<boolean>`



### `getTop() => Promise<HTMLIonLoadingElement | undefined>`

Get the most recently opened loading overlay.

#### Returns

Type: `Promise<HTMLIonLoadingElement | undefined>`




----------------------------------------------

*Built with [StencilJS](https://stenciljs.com/)*
