# ステートマシン

Comable では注文情報に [state_mashine](https://github.com/pluginaweek/state_machine) を利用することで、注文のフローや管理の実現を容易にしています。

## 注文

注文のステートは次のように遷移します。

```mermaid
graph TD;
    cart --> orderer;
    orderer --> delivery;
    delivery --> shipment;
    shipment --> payment;
    payment --> confirm;
    confirm --> completed;
    completed --> canceled;
    completed --> returned;
    canceled --> resumed;
    resumed --> canceled;
    resumed --> returned;

    cart[cart<br/>ショッピングカート];
    orderer[orderer<br/>請求先入力];
    delivery[delivery<br/>配送先入力];
    shipment[shipment<br/>配送選択];
    payment[payment<br/>決済選択];
    confirm[confirm<br/>注文確認];
    completed[completed<br/>注文完了];
    resumed[resumed<br/>再開];
    canceled[canceled<br/>キャンセル];
    returned[returned<br/>返品済み];
```

## 下書き注文

注文のステートは次のように遷移します。注文完了後の遷移は通常の注文と同じです。

```mermaid
graph TD;
    draft --> shipment;
    shipment --> completed;

    draft[draft<br/>下書き];
    shipment[shipment<br/>配送選択];
    completed[completed<br/>注文完了];
```

## 配送

配送のステートは次のように遷移します。

```mermaid
graph TD;
    pending --> ready;
    ready --> completed;
    completed --> canceled;
    canceled --> resumed;
    resumed --> canceled;

    pending[pending<br/>準備中];
    ready[ready<br/>準備完了];
    completed[completed<br/>発送完了];
    resumed[resumed<br/>再開];
    canceled[canceled<br/>キャンセル];
```

## 決済

決済のステートは次のように遷移します。

```mermaid
graph TD;
    pending --> ready;
    ready --> completed;
    completed --> canceled;
    canceled --> resumed;
    resumed --> canceled;

    pending[pending<br/>準備中];
    ready[ready<br/>オーソリ完了];
    completed[completed<br/>決済完了];
    resumed[resumed<br/>再開];
    canceled[canceled<br/>キャンセル];
```
