# Foundry AP

[Foundry Docs](https://book.getfoundry.sh/)

[PC YouTube](https://www.youtube.com/watch?v=umepbfKp5rI&t=0s)

## Testing

- **Unit Tests** - testing a specific part of our code
- **Integration Tests** - testing how different parts of our code work together
- **Forked Tests** - testing how our code works on a simulated real environment
- **Staging Tests** - testing how our code works on a real environment

This is an example of running a test on a specific function on a forked environment... in this case using our Alchemy node. Remember to check alchemy, where the API calls will be stored.

- `forge test --match-test testPriceFeedVersionAccurate -vvv --fork-url $SEPOLIA_RPC_URL`

## Modularity

- **Modularity** - the degree to which a system's components may be separated and recombined. For instance, originally in `FundMe.sol` we have a priceFeed that is hard coded to Sepolia. We can make this modular by creating a `PriceFeed.sol` contract that can be used by any contract that needs a price feed. This is a good example of how we can make our code more modular and reusable. This is alos an example of **refactoring** our code. Refactoring is the process of restructuring existing computer code—changing the factoring—without changing its external behavior. Refactoring improves nonfunctional attributes of the software. Advantages include improved code readability and reduced complexity; these can improve source-code maintainability and create a more expressive internal architecture or object model to improve extensibility.
