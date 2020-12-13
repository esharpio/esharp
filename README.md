# esharp
c# compiler for the esharp smart contract langauge

## Abstract

esharp is a new Ethereum smart contract language, influenced by Microsofts .NET c#.  Just like vyper is a python like language, compiled with python, esharp aims to have an alternative smart contract lanauge for .NET developers.

## Structure of a contract


### State Variables

```
public contract SimpleStorage
{
    uint storedData;
}
```

### Methods (Functions and Voids)

```
public contract SimpleAuction
{
  [Payable]
  public void Bid()
  {
    // ...
  }
}
```

### Method Attributes


### Events

```
public event void HighestBidIncreased(address bidder, uint amount);

public contract SimpleAuction
{
  [Payable]
  public void Bid()
  {
    HighestBidIncreased?.Invoke(msg.Sender, msg.Value);
  }
}
```
