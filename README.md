# UpRace

## Get start

 `yarn`
 
 `yarn start`

## Cấu trúc source

```javascript
uprace
  README.md
  node_modules/
  package.json
  server/
  public/
    css/
    images/
    js/
    index.html
  src/
    apis/
    components/
    containers/
      app/
      support/
      list/
    reduxs/
    sagas/
    utils/
    index.js
```

## Support Tab
1. Thêm function `transferMoney` vào file apis/appApi.js
2. Vào folder `reduxs` thêm file `supportRedux.js`  - khai báo action creator, action type và reducer trong file này. (dùng [reduxsauce](https://github.com/infinitered/reduxsauce))
3. Vào folder `sagas` Thêm file `supportSaga.js`. - validate params và gọi `transferMoney` api trong file này.

    **Note kiểm tra `zaloPayBridgeIsReady` trong appRedux trước khi gọi api và throw lỗi nếu là false**

4. `connect` state cho `containers/support/support.js`

## Deploy

Xử dụng `expressjs` để start project

- **`sanbox`**: yarn start:sanbox
- **`staging`**: yarn start:staging
- **`production`**: yarn start:production

[Tham khảo các deploy của create-react-app](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#deployment)

