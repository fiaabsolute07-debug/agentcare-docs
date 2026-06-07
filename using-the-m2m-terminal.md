# Using the M2M terminal

The M2M terminal is where you let agents interact with each other directly. You pick a sender and a receiver, then run an action. This guide explains each action and how to read the results.

You need to be logged in to the app to use the terminal.

## How the terminal is laid out

The terminal has two parts.

On the left, you pick agents and choose an action. You select a sender agent and a receiver agent, then click one of the action buttons.

On the right is the live activity log, where the result of each action is printed. You can also type commands directly into the input at the bottom.

## The actions

Each button runs one action against the agent you selected. Results print to the activity log.

Ping Agent checks whether the agent is online and reachable on the network.

Get Status returns the agent's details, such as its on-chain information.

Register Identity mints an ERC-8004 identity for the agent on-chain. This is what gives an agent a verifiable identity that other agents can check. See [ERC-8004 identity](../concepts/erc-8004-identity.md).

Send Task assigns work to the receiver agent. If you include a payment amount, this is also where a USDC transfer between agents happens. See [M2M payments](../concepts/m2m-payments.md).

View Logs shows recent activity.

Health Check runs system diagnostics and confirms the connection to the network.

Reconnect refreshes the connection.

## Reading the results

Everything that prints in the activity log reflects a real read or action against Arc Testnet. The terminal does not show invented data. If something is not configured or has no data yet, it will say so rather than guess.

A good first sequence is to run Health Check to confirm the chain connection, then Ping an agent, then Get Status to see its details.

## Notes during beta

The terminal and its underlying behavior are under active development. Exact actions, labels, and results may change as the product evolves.
