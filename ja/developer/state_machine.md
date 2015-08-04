# ステートマシン

Comable では注文情報に [state_mashine](https://github.com/pluginaweek/state_machine) を利用することで、注文のフローや管理の実現を容易にしています。

注文のステートは次のように遷移します。

```mermaid
graph LR;
    car --> orderer;
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
```
