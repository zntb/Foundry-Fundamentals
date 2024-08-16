# Custom Error

Using a basic `revert()` statement may not provide evidence on why a transaction failed. A better approach is to define custom errors by combining the **contract name** with a **description**, such as `Raffle__UpkeepNotNeeded()`. Additionally, including **parameters** can offer more detailed information about the cause of the transaction failure.

```solidity
Raffle__UpkeepNotNeeded(address balance, uint256 length, uint256 raffleState);
```

<hr>

## Mid section recap

### Quick recap

Congratulations, we wrote a bunch of great code!

What did we do?

- We implemented Chainlink VRF to get a random number;
- We defined a couple of variables that we need both for Raffle operation and for Chainlink VRF interaction;
- We have a not-so-small constructor;
- We've created a method for the willing participants to enter the Raffle;
- Then made the necessary integrations with Chainlink Automation to automatically draw a winner when the time is right.
- When the time is right and after the Chainlink nodes perform the call then Chainlink VRF will provide the requested randomness inside `fulfillRandomWords`;
- The randomness is used to find out who won, the prize is sent, raffle is reset.

And that's all! Take a break, take a walk and come back for more fun activities. Next, we'll have deploying, testing and many refactorings!
