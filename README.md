<!DOCTYPE html><html><head><meta charSet="utf-8"/><meta http-equiv="X-UA-Compatible" content="IE=edge"/><meta name="viewport" content="width=device-width,minimum-scale=1,initial-scale=1"/><title>DocumentPicker to Blob - Snack</title><meta name="description" content="Bacon: Use the DocumentPicker API to get a file, then fetch the URI and convert it to a Blob type that can be uploaded to a server."/><meta property="og:url" content="https://snack.expo.io/@bacon/documentpicker-to-blob"/><meta property="og:title" content="DocumentPicker to Blob - Snack"/><meta property="og:description" content="Bacon: Use the DocumentPicker API to get a file, then fetch the URI and convert it to a Blob type that can be uploaded to a server."/><meta property="og:type" content="website"/><meta property="og:image" content="https://s3.amazonaws.com/exp-brand-assets/SnackIcon_200.png"/><meta property="og:image:width" content="200"/><meta property="og:image:height" content="200"/><meta name="twitter:card" content="summary"/><meta name="twitter:site" content="@expo"/><meta name="twitter:title" content="DocumentPicker to Blob - Snack"/><meta name="twitter:description" content="Bacon: Use the DocumentPicker API to get a file, then fetch the URI and convert it to a Blob type that can be uploaded to a server."/><meta name="twitter:image" content="https://s3.amazonaws.com/exp-brand-assets/SnackIcon_200.png"/><meta name="google-site-verification" content="Fh25fNM-buRYptb-TO6MVgOjXGzdhmAnRgIC7sdrmbw"/><link rel="shortcut icon" href="/favicon.ico"/><link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:400,300,500,600"/><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/normalize/8.0.1/normalize.min.css"/><style type="text/css">
              :root {
                --font-normal: 'Source Sans Pro', 'Helvetica Neue', Helvetica, Arial, sans-serif;
                --font-monospace: 'Fira Code', 'Fira Mono', Monaco, Menlo, 'Ubuntu Mono', Consolas,
                  source-code-pro, monospace;
              }

              html {
                box-sizing: border-box;
              }

              *,
              *:before,
              *:after {
                box-sizing: inherit;
              }

              *:focus {
                outline: none;
              }

              *:focus-visible {
                outline: auto;
              }

              html,
              body {
                height: 100%;
                width: 100%;
                overflow: hidden;
              }

              body {
                font-family: var(--font-normal);
                font-size: 14px;
                line-height: 1.42857143;
                overscroll-behavior: none;
              }

              div {
                scrollbar-width: thin;
                scrollbar-color: var(--color-disabled) var(--color-background);
              }

              @media (hover) {
                ::-webkit-scrollbar {
                  width: 12px;
                  height: 12px;
                  background: var(--color-background);
                }
                ::-webkit-scrollbar-thumb {
                  background: var(--color-disabled);
                  border-radius: 10px;
                  border: 3px var(--color-background) solid;
                }
              }

              button,
              input,
              select,
              textarea {
                font: inherit;
                color: inherit;
                line-height: inherit;
              }

              button {
                cursor: pointer;
              }

              button[disabled] {
                cursor: default;
              }

              #root {
                height: 100vh;
              }

              a {
                color: #4099ff;
              }
            </style><style type="text/css" data-aphrodite="true">._7yafp1x{height:100% !important;width:100% !important;--color-primary:#4630EB !important;--color-secondary:#000020 !important;--color-error:#B71525 !important;--color-warning:#DB9600 !important;--color-success:#19971A !important;--color-primary-text:#ffffff !important;--color-secondary-text:#ffffff !important;--color-error-text:#ffffff !important;--color-warning-text:#ffffff !important;--color-success-text:#ffffff !important;--color-text:#060625 !important;--color-soft:#8F8F9D !important;--color-soft-text:#ffffff !important;--color-background:#F9F9F9 !important;--color-content:#ffffff !important;--color-hover:#F5F5F7 !important;--color-disabled:#CFCFD5 !important;--color-selected:#4630EB !important;--color-selected-text:#ffffff !important;--color-border:#DDDDE1 !important;--shadow-popover:0 2px 6px rgba(0,0,0,0.15) !important;--shadow-small:0 5px 10px rgba(0,0,0,0.12) !important;}._1vc9yjy{background-color:currentColor !important;opacity:0.2 !important;border-radius:3px !important;width:24px !important;height:24px !important;margin-left:16px !important;margin-right:16px !important;}._1qfgucq{min-width:0px !important;margin-right:16px !important;}._kcab8j{font-size:1.3em !important;line-height:1.3em !important;font-weight:600 !important;margin:0px !important;padding:1px 6px !important;}._dixpgu{font-size:12px !important;margin:0 6px !important;opacity:0.5 !important;}._162bvhe{width:80px !important;height:40px !important;pointer-events:none !important;}._1g65ehf{background-color:currentColor !important;opacity:0.2 !important;height:26px !important;width:26px !important;border-radius:13px !important;margin:0 16px !important;}._1pcb09u{-webkit-box-direction:normal !important;-webkit-box-orient:vertical !important;display:-webkit-box !important;display:-moz-box !important;display:-ms-flexbox !important;display:-webkit-flex !important;display:flex !important;-webkit-flex-direction:column !important;-ms-flex-direction:column !important;flex-direction:column !important;height:100% !important;width:100% !important;overflow:hidden !important;background-color:var(--color-background) !important;color:var(--color-text) !important;}@keyframes keyframe_9gmgni{0%{-webkit-transform:scale3d(0, 1, 1);-ms-transform:scale3d(0, 1, 1);transform:scale3d(0, 1, 1);opacity:1;}75%{-webkit-transform:scale3d(1, 1, 1);-ms-transform:scale3d(1, 1, 1);transform:scale3d(1, 1, 1);opacity:1;}100%{-webkit-transform:scale3d(1, 1, 1);-ms-transform:scale3d(1, 1, 1);transform:scale3d(1, 1, 1);opacity:0;}}._n39zzn{position:absolute !important;left:0px !important;right:0px !important;height:2px !important;z-index:1 !important;background-color:var(--color-primary) !important;-webkit-transform:scale3d(0, 1, 1) !important;-ms-transform:scale3d(0, 1, 1) !important;transform:scale3d(0, 1, 1) !important;-webkit-transform-origin:top left !important;-ms-transform-origin:top left !important;transform-origin:top left !important;-webkit-animation-name:keyframe_9gmgni !important;animation-name:keyframe_9gmgni !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;}._1fhj40{-webkit-box-pack:justify !important;-ms-flex-pack:justify !important;-webkit-box-align:center !important;-ms-flex-align:center !important;-webkit-box-direction:normal !important;-webkit-box-orient:horizontal !important;display:-webkit-box !important;display:-moz-box !important;display:-ms-flexbox !important;display:-webkit-flex !important;display:flex !important;-webkit-flex-direction:row !important;-ms-flex-direction:row !important;flex-direction:row !important;-webkit-align-items:center !important;align-items:center !important;-webkit-justify-content:space-between !important;justify-content:space-between !important;border-bottom:1px solid var(--color-border) !important;height:60px !important;background-color:var(--color-content) !important;}._pyropi{-webkit-box-align:center !important;-ms-flex-align:center !important;-webkit-box-direction:normal !important;-webkit-box-orient:horizontal !important;display:-webkit-box !important;display:-moz-box !important;display:-ms-flexbox !important;display:-webkit-flex !important;display:flex !important;-webkit-flex-direction:row !important;-ms-flex-direction:row !important;flex-direction:row !important;-webkit-align-items:center !important;align-items:center !important;min-width:0px !important;-webkit-flex:1 !important;-ms-flex:1 1 0% !important;flex:1 !important;}._18oqrvsw{-webkit-appearance:none !important;-moz-appearance:none !important;appearance:none !important;outline:0px !important;border-radius:3px !important;white-space:nowrap !important;text-align:center !important;text-decoration:none !important;-webkit-transition-duration:170ms !important;transition-duration:170ms !important;-webkit-transition-property:box-shadow !important;-moz-transition-property:box-shadow !important;transition-property:box-shadow !important;-webkit-transition-timing-function:linear !important;transition-timing-function:linear !important;color:var(--color-secondary-text) !important;background-color:var(--color-secondary) !important;border:1px solid transparent !important;padding:.5em 1em !important;margin:.5em !important;}._18oqrvsw:hover{box-shadow:var(--shadow-small) !important;}._ymhguf{-webkit-box-pack:justify !important;-ms-flex-pack:justify !important;-webkit-box-direction:normal !important;-webkit-box-orient:horizontal !important;display:-webkit-box !important;display:-moz-box !important;display:-ms-flexbox !important;display:-webkit-flex !important;display:flex !important;-webkit-flex:1 !important;-ms-flex:1 1 0% !important;flex:1 !important;-webkit-flex-direction:row !important;-ms-flex-direction:row !important;flex-direction:row !important;-webkit-justify-content:space-between !important;justify-content:space-between !important;position:relative !important;height:100% !important;min-height:0px !important;min-width:0px !important;}._1s11hu1{-webkit-box-direction:normal !important;-webkit-box-orient:vertical !important;height:100% !important;display:-webkit-box !important;display:-moz-box !important;display:-ms-flexbox !important;display:-webkit-flex !important;display:flex !important;-webkit-flex-direction:column !important;-ms-flex-direction:column !important;flex-direction:column !important;min-width:240px !important;border-right:1px solid var(--color-border) !important;background-color:var(--color-content) !important;}._1c40t29{-webkit-box-pack:center !important;-ms-flex-pack:center !important;-webkit-box-align:center !important;-ms-flex-align:center !important;display:-webkit-box !important;display:-moz-box !important;display:-ms-flexbox !important;display:-webkit-flex !important;display:flex !important;height:100% !important;width:100% !important;-webkit-align-items:center !important;align-items:center !important;-webkit-justify-content:center !important;justify-content:center !important;}._4w0mhx{-webkit-transform:scale(0.4) !important;-ms-transform:scale(0.4) !important;transform:scale(0.4) !important;opacity:0.2 !important;}._p6qm3x{position:relative !important;height:182px !important;width:182px !important;overflow:hidden !important;}@keyframes keyframe_1ysemx{0%{opacity:0;}39.9%{opacity:0;}40%{-webkit-transform:translate3d(78px, 68.5px, 0);-ms-transform:translate3d(78px, 68.5px, 0);transform:translate3d(78px, 68.5px, 0);opacity:1;}50%{-webkit-transform:translate3d(39px, 46.5px, 0);-ms-transform:translate3d(39px, 46.5px, 0);transform:translate3d(39px, 46.5px, 0);}}._1b0gwq5m{position:absolute !important;top:0px !important;left:0px !important;-webkit-animation-duration:4s !important;animation-duration:4s !important;-webkit-animation-delay:1s !important;animation-delay:1s !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;-webkit-animation-direction:alternate-reverse !important;animation-direction:alternate-reverse !important;-webkit-transform:translate3d(39px, 46.5px, 0) !important;-ms-transform:translate3d(39px, 46.5px, 0) !important;transform:translate3d(39px, 46.5px, 0) !important;-webkit-animation-name:keyframe_1ysemx !important;animation-name:keyframe_1ysemx !important;}@keyframes keyframe_1a1qkd5{0%{opacity:0;}49.9%{opacity:0;}50%{-webkit-transform:translate3d(39px, 46.5px, 0);-ms-transform:translate3d(39px, 46.5px, 0);transform:translate3d(39px, 46.5px, 0);opacity:1;}60%{-webkit-transform:translate3d(39px, 0px, 0);-ms-transform:translate3d(39px, 0px, 0);transform:translate3d(39px, 0px, 0);}}._14l78d6g{position:absolute !important;top:0px !important;left:0px !important;-webkit-animation-duration:4s !important;animation-duration:4s !important;-webkit-animation-delay:1s !important;animation-delay:1s !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;-webkit-animation-direction:alternate-reverse !important;animation-direction:alternate-reverse !important;-webkit-transform:translate3d(39px, 0px, 0) !important;-ms-transform:translate3d(39px, 0px, 0) !important;transform:translate3d(39px, 0px, 0) !important;-webkit-animation-name:keyframe_1a1qkd5 !important;animation-name:keyframe_1a1qkd5 !important;}@keyframes keyframe_10mcliz{}._1tvj80n9{position:absolute !important;top:0px !important;left:0px !important;-webkit-animation-duration:4s !important;animation-duration:4s !important;-webkit-animation-delay:1s !important;animation-delay:1s !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;-webkit-animation-direction:alternate-reverse !important;animation-direction:alternate-reverse !important;-webkit-transform:translate3d(0, 68.5px, 0) !important;-ms-transform:translate3d(0, 68.5px, 0) !important;transform:translate3d(0, 68.5px, 0) !important;-webkit-animation-name:keyframe_10mcliz !important;animation-name:keyframe_10mcliz !important;}@keyframes keyframe_1omr31l{0%{opacity:0;}29.9%{opacity:0;}30%{-webkit-transform:translate3d(39px, 90px, 0);-ms-transform:translate3d(39px, 90px, 0);transform:translate3d(39px, 90px, 0);opacity:1;}40%{-webkit-transform:translate3d(78px, 68.5px, 0);-ms-transform:translate3d(78px, 68.5px, 0);transform:translate3d(78px, 68.5px, 0);}}._1cqt99fk{position:absolute !important;top:0px !important;left:0px !important;-webkit-animation-duration:4s !important;animation-duration:4s !important;-webkit-animation-delay:1s !important;animation-delay:1s !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;-webkit-animation-direction:alternate-reverse !important;animation-direction:alternate-reverse !important;-webkit-transform:translate3d(78px, 68.5px, 0) !important;-ms-transform:translate3d(78px, 68.5px, 0) !important;transform:translate3d(78px, 68.5px, 0) !important;-webkit-animation-name:keyframe_1omr31l !important;animation-name:keyframe_1omr31l !important;}@keyframes keyframe_1pbmn7q{0%{-webkit-transform:translate3d(0, 68.5px, 0);-ms-transform:translate3d(0, 68.5px, 0);transform:translate3d(0, 68.5px, 0);}20%{-webkit-transform:translate3d(0, 68.5px, 0);-ms-transform:translate3d(0, 68.5px, 0);transform:translate3d(0, 68.5px, 0);}30%{-webkit-transform:translate3d(39px, 90px, 0);-ms-transform:translate3d(39px, 90px, 0);transform:translate3d(39px, 90px, 0);}}._1fho7xh9{position:absolute !important;top:0px !important;left:0px !important;-webkit-animation-duration:4s !important;animation-duration:4s !important;-webkit-animation-delay:1s !important;animation-delay:1s !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;-webkit-animation-direction:alternate-reverse !important;animation-direction:alternate-reverse !important;-webkit-transform:translate3d(39px, 90px, 0) !important;-ms-transform:translate3d(39px, 90px, 0) !important;transform:translate3d(39px, 90px, 0) !important;-webkit-animation-name:keyframe_1pbmn7q !important;animation-name:keyframe_1pbmn7q !important;}@keyframes keyframe_b5qg5v{0%{opacity:0;}59.9%{opacity:0;}60%{-webkit-transform:translate3d(39px, 0px, 0);-ms-transform:translate3d(39px, 0px, 0);transform:translate3d(39px, 0px, 0);opacity:1;}70%{-webkit-transform:translate3d(0, 23px, 0);-ms-transform:translate3d(0, 23px, 0);transform:translate3d(0, 23px, 0);}}._l9xbyq9{position:absolute !important;top:0px !important;left:0px !important;-webkit-animation-duration:4s !important;animation-duration:4s !important;-webkit-animation-delay:1s !important;animation-delay:1s !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;-webkit-animation-direction:alternate-reverse !important;animation-direction:alternate-reverse !important;-webkit-transform:translate3d(0, 23px, 0) !important;-ms-transform:translate3d(0, 23px, 0) !important;transform:translate3d(0, 23px, 0) !important;-webkit-animation-name:keyframe_b5qg5v !important;animation-name:keyframe_b5qg5v !important;}@keyframes keyframe_841g8u{0%{opacity:0;}69.9%{opacity:0;}70%{-webkit-transform:translate3d(0, 23px, 0);-ms-transform:translate3d(0, 23px, 0);transform:translate3d(0, 23px, 0);opacity:1;}80%{-webkit-transform:translate3d(39px, 42.5px, 0);-ms-transform:translate3d(39px, 42.5px, 0);transform:translate3d(39px, 42.5px, 0);}}._1oufavzh{position:absolute !important;top:0px !important;left:0px !important;-webkit-animation-duration:4s !important;animation-duration:4s !important;-webkit-animation-delay:1s !important;animation-delay:1s !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;-webkit-animation-direction:alternate-reverse !important;animation-direction:alternate-reverse !important;-webkit-transform:translate3d(39px, 42.5px, 0) !important;-ms-transform:translate3d(39px, 42.5px, 0) !important;transform:translate3d(39px, 42.5px, 0) !important;-webkit-animation-name:keyframe_841g8u !important;animation-name:keyframe_841g8u !important;}@keyframes keyframe_1x1yick{0%{-webkit-transform:translate3d(133px, 12.5px, 0) scale(0);-ms-transform:translate3d(133px, 12.5px, 0) scale(0);transform:translate3d(133px, 12.5px, 0) scale(0);}80%{-webkit-transform:translate3d(133px, 12.5px, 0) scale(0);-ms-transform:translate3d(133px, 12.5px, 0) scale(0);transform:translate3d(133px, 12.5px, 0) scale(0);}90%{-webkit-transform:translate3d(133px, 12.5px, 0) scale(1);-ms-transform:translate3d(133px, 12.5px, 0) scale(1);transform:translate3d(133px, 12.5px, 0) scale(1);}}._ce1yvye{position:absolute !important;top:0px !important;left:0px !important;-webkit-animation-duration:4s !important;animation-duration:4s !important;-webkit-animation-delay:1s !important;animation-delay:1s !important;-webkit-animation-iteration-count:infinite !important;animation-iteration-count:infinite !important;-webkit-animation-direction:alternate-reverse !important;animation-direction:alternate-reverse !important;-webkit-transform:translate3d(133px, 12.5px, 0) !important;-ms-transform:translate3d(133px, 12.5px, 0) !important;transform:translate3d(133px, 12.5px, 0) !important;-webkit-animation-name:keyframe_1x1yick !important;animation-name:keyframe_1x1yick !important;}._tzmlrt{height:100% !important;display:none !important;min-width:334px !important;background-color:var(--color-content) !important;border-left:1px solid var(--color-border) !important;}@media (min-width: 700px){._tzmlrt{display:-webkit-box !important;display:-moz-box !important;display:-ms-flexbox !important;display:-webkit-flex !important;display:flex !important;}}._1nsqli4{-webkit-box-align:center !important;-ms-flex-align:center !important;-webkit-box-direction:normal !important;-webkit-box-orient:horizontal !important;position:relative !important;display:-webkit-box !important;display:-moz-box !important;display:-ms-flexbox !important;display:-webkit-flex !important;display:flex !important;-webkit-flex-direction:row !important;-ms-flex-direction:row !important;flex-direction:row !important;-webkit-align-items:center !important;align-items:center !important;padding:0 .25em !important;border-top:1px solid var(--color-border) !important;background-color:var(--color-content) !important;color:var(--color-soft) !important;height:30px !important;z-index:10 !important;}</style><script>
               if (window.location.search.indexOf('hideQueryParams=true') >= 0) {
                 history.replaceState(null, document.title, window.location.pathname);
               }
               window.__INITIAL_DATA__ = {"data":{"type":"success","snack":{"id":"4e3d9835-2bdd-4efd-bcd2-bcddd66928de","hashId":"Hy4Esf7yN","code":{"App.js":{"type":"CODE","contents":"import * as React from 'react';\nimport { Text, View, StyleSheet } from 'react-native';\nimport { Constants, DocumentPicker } from 'expo';\n\n// You can import from local files\nimport AssetExample from './components/AssetExample';\n\n// or any pure javascript modules available in npm\nimport { Card } from 'react-native-paper';\n\nexport default class App extends React.Component {\n  onPress = async () => {\n    const { type, uri } = await DocumentPicker.getDocumentAsync({\n      copyToCacheDirectory: false,\n      type: '*/*',\n    });\n\n    if (type === 'cancel') {\n      return;\n    }\n    console.log('pickerResponse', uri);\n\n    try {\n      const fetchResponse = await fetch(uri);\n      console.log('fetchResponse', fetchResponse);\n      const blob = await fetchResponse.blob();\n      console.log('blob', blob);\n    } catch (error) {\n      console.log('ERR: ' + error.message);\n    }\n  };\n\n  render() {\n    return (\n      <View style={styles.container}>\n        <Text onPress={this.onPress} style={styles.paragraph}>\n          Change code in the editor and watch it change on your phone! Save to\n          get a shareable url.\n        </Text>\n        <Card>\n          <AssetExample />\n        </Card>\n      </View>\n    );\n  }\n}\n\nconst styles = StyleSheet.create({\n  container: {\n    flex: 1,\n    justifyContent: 'center',\n    paddingTop: Constants.statusBarHeight,\n    backgroundColor: '#ecf0f1',\n    padding: 8,\n  },\n  paragraph: {\n    margin: 24,\n    fontSize: 18,\n    fontWeight: 'bold',\n    textAlign: 'center',\n  },\n});\n"},"README.md":{"type":"CODE","contents":"# Sample Snack app\n\nWelcome to Expo!\n\nOpen the `App.js` file to start writing some code. You can preview the changes directly on your phone or tablet by clicking the **Run** button or use the simulator by clicking **Tap to Play**. When you're done, click **Save** and share the link!\n\nWhen you're ready to see everything that Expo provides (or if you want to use your own editor) you can **Export** your project and use it with [expo-cli](https://docs.expo.io/versions/latest/introduction/installation.html).\n\nProjects created in Snack are publicly available, so you can easily share the link to this project via link, or embed it on a web page with the **Embed** button.\n\nIf you're having problems, you can tweet to us [@expo](https://twitter.com/expo) or ask in our [forums](https://forums.expo.io).\n\nSnack is Open Source. You can find the code on the [GitHub repo](https://github.com/expo/snack-web).\n"},"assets/snack-icon.png":{"type":"ASSET","contents":"https://snack-code-uploads.s3.us-west-1.amazonaws.com/~asset/2f7d32b1787708aba49b3586082d327b"},"components/AssetExample.js":{"type":"CODE","contents":"import * as React from 'react';\nimport { Text, View, StyleSheet, Image } from 'react-native';\n\nexport default class AssetExample extends React.Component {\n  render() {\n    return (\n      <View style={styles.container}>\n        <Text style={styles.paragraph}>\n          Local files and assets can be imported by dragging and dropping them into the editor\n        </Text>\n        <Image style={styles.logo} source={require('../assets/snack-icon.png')} />\n      </View>\n    );\n  }\n}\n\nconst styles = StyleSheet.create({\n  container: {\n    alignItems: 'center',\n    justifyContent: 'center',\n    padding: 24,\n  },\n  paragraph: {\n    margin: 24,\n    marginTop: 0,\n    fontSize: 14,\n    fontWeight: 'bold',\n    textAlign: 'center',\n  },\n  logo: {\n    height: 128,\n    width: 128,\n  }\n});\n"}},"sdkVersion":"31.0.0","created":"2018-12-03T21:07:55.969Z","manifest":{"name":"DocumentPicker to Blob","sdkVersion":"31.0.0","description":"Bacon: Use the DocumentPicker API to get a file, then fetch the URI and convert it to a Blob type that can be uploaded to a server.","dependencies":{"react-native-paper":"2.1.3"}},"previewLocation":"https://snack-code-uploads.s3.us-west-1.amazonaws.com/~preview/ea39f053744dab2d13555039d1a2b2eb","status":"SUCCESS","dependencies":{"react-native-paper":{"version":"2.1.3","isUserSpecified":true}},"username":"snack","history":[{"hashId":"Hy4Esf7yN","savedAt":"2018-12-03T21:07:55.992Z"}],"isDraft":false,"userSnackId":"81593e70-f73f-11e8-a374-7d6da91fc76f"},"defaults":{"name":"brave kiwi","channel":"2ohtmlKAZ1"}},"splitTestSettings":{"defaultConnectionMethod":"account","authFlow":"save2","snackFirstSeen":"2021-01-31"},"queryParams":{},"postData":{}} </script></head><body><div id="root"><div class="_7yafp1x"><div class="_1pcb09u"><div class="_n39zzn" style="animation-delay:1000ms;animation-duration:2000ms"></div><div class="_1fhj40"><div class="_pyropi"><div class="_1vc9yjy"></div><div class="_1qfgucq"><h1 class="_kcab8j">DocumentPicker to Blob</h1><div class="_dixpgu">…</div></div></div><button type="button" class="_18oqrvsw _162bvhe"> </button><div class="_1g65ehf"></div></div><div class="_ymhguf"><div class="_1s11hu1"></div><div class="_1c40t29"><div class="_4w0mhx"><div class="_p6qm3x"><svg width="82px" height="95px" viewBox="0 0 82 95" class="_1b0gwq5m"><g transform="translate(2.000000, 2.000000)" stroke="#060625" stroke-linecap="round" stroke-linejoin="round" stroke-width="3"><polygon fill="#ffffff" points="0 22 40 44 40 91 0 69"></polygon><polygon fill="#ffffff" points="0 22 39 0 78 22 39 44"></polygon><polygon fill="#060625" points="78 69 40 91 40 44 78 22"></polygon></g></svg><svg width="82px" height="95px" viewBox="0 0 82 95" class="_14l78d6g"><g transform="translate(2.000000, 2.000000)" stroke="#060625" stroke-linecap="round" stroke-linejoin="round" stroke-width="3"><polygon fill="#ffffff" points="0 22 40 44 40 91 0 69"></polygon><polygon fill="#ffffff" points="0 22 39 0 78 22 39 44"></polygon><polygon fill="#060625" points="78 69 40 91 40 44 78 22"></polygon></g></svg><svg width="82px" height="95px" viewBox="0 0 82 95" class="_1tvj80n9"><g transform="translate(2.000000, 2.000000)" stroke="#060625" stroke-linecap="round" stroke-linejoin="round" stroke-width="3"><polygon fill="#ffffff" points="0 22 40 44 40 91 0 69"></polygon><polygon fill="#ffffff" points="0 22 39 0 78 22 39 44"></polygon><polygon fill="#060625" points="78 69 40 91 40 44 78 22"></polygon></g></svg><svg width="82px" height="95px" viewBox="0 0 82 95" class="_1cqt99fk"><g transform="translate(2.000000, 2.000000)" stroke="#060625" stroke-linecap="round" stroke-linejoin="round" stroke-width="3"><polygon fill="#ffffff" points="0 22 40 44 40 91 0 69"></polygon><polygon fill="#ffffff" points="0 22 39 0 78 22 39 44"></polygon><polygon fill="#060625" points="78 69 40 91 40 44 78 22"></polygon></g></svg><svg width="82px" height="95px" viewBox="0 0 82 95" class="_1fho7xh9"><g transform="translate(2.000000, 2.000000)" stroke="#060625" stroke-linecap="round" stroke-linejoin="round" stroke-width="3"><polygon fill="#ffffff" points="0 22 40 44 40 91 0 69"></polygon><polygon fill="#ffffff" points="0 22 39 0 78 22 39 44"></polygon><polygon fill="#060625" points="78 69 40 91 40 44 78 22"></polygon></g></svg><svg width="82px" height="95px" viewBox="0 0 82 95" class="_l9xbyq9"><g transform="translate(2.000000, 2.000000)" stroke="#060625" stroke-linecap="round" stroke-linejoin="round" stroke-width="3"><polygon fill="#ffffff" points="0 22 40 44 40 91 0 69"></polygon><polygon fill="#ffffff" points="0 22 39 0 78 22 39 44"></polygon><polygon fill="#060625" points="78 69 40 91 40 44 78 22"></polygon></g></svg><svg width="82px" height="95px" viewBox="0 0 82 95" class="_1oufavzh"><g transform="translate(2.000000, 2.000000)" stroke="#060625" stroke-linecap="round" stroke-linejoin="round" stroke-width="3"><polygon fill="#ffffff" points="0 22 40 44 40 91 0 69"></polygon><polygon fill="#ffffff" points="0 22 39 0 78 22 39 44"></polygon><polygon fill="#060625" points="78 69 40 91 40 44 78 22"></polygon></g></svg><svg width="48px" height="48px" viewBox="0 0 54 54" class="_ce1yvye"><g transform="translate(2.000000, 2.000000)" stroke="#060625" stroke-width="3"><circle fill="#ffffff" cx="24" cy="24" r="24"></circle><path d="M44.6358987,12 C41.7645228,28.8507274 27.0454631,41.1867351 9.80745621,41.1896317 C8.85831621,41.1896317 7.9291581,41.1896317 7,41.0707734 C15.5879325,49.5304234 29.1803651,50.3420227 38.7303845,42.9653834 C48.2804039,35.5887441 50.8101654,22.3240171 44.6358987,12 Z" fill="#060625"></path></g></svg></div></div></div><div class="_tzmlrt"></div></div><div class="_1nsqli4"></div></div></div></div><script>!function(){var analytics=window.analytics=window.analytics||[];if(!analytics.initialize)if(analytics.invoked)return;else{analytics.invoked=!0;analytics.methods=["trackSubmit","trackClick","trackLink","trackForm","pageview","identify","reset","group","track","ready","alias","debug","page","once","off","on"];analytics.factory=function(t){return function(){var e=Array.prototype.slice.call(arguments);e.unshift(t);analytics.push(e);return analytics}};for(var t=0;t<analytics.methods.length;t++){var e=analytics.methods[t];analytics[e]=analytics.factory(e)}analytics.load=function(t){var e=document.createElement("script");e.type="text/javascript";e.async=!0;e.src=("https:"===document.location.protocol?"https://":"http://")+"cdn.segment.com/analytics.js/v1/"+t+"/analytics.min.js";var n=document.getElementsByTagName("script")[0];n.parentNode.insertBefore(e,n)};analytics.SNIPPET_VERSION="4.0.0";    analytics.load('Ha0swpI6s2CVEMxK84cEmKmUVmBa1USu');    analytics.page();    analytics.identify({      user_properties: {"defaultConnectionMethod":"account","authFlow":"save2","snackFirstSeen":"2021-01-31"}    });}}();</script><script>(function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){(i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)})(window,document,'script','//www.google-analytics.com/analytics.js','ga');ga('create', 'UA-53647600-5', {cookieDomain: 'auto', siteSpeedSampleRate: 100});ga('send', 'pageview');</script><script src="https://cdnjs.cloudflare.com/ajax/libs/babel-polyfill/6.26.0/polyfill.min.js"></script><script src="/dist/app.bundle.js"></script></body></html>
