# Bitcoin Core Block Height Query

This simple script helps you query the current block height using Bitcoin Core.

## Install Bitcoin Core

First, make sure you have Bitcoin Core installed. You can find installation instructions for your operating system on the [official Bitcoin Core website](https://bitcoin.org/en/download).

## Query Block Height with Bitcoin Core

Once Bitcoin Core is installed, you can follow these steps to query the current block height:

1. Start the Bitcoin Core client.

2. Wait for the client to fully synchronize with the blockchain (this may take some time).

3. Open a terminal or command prompt.

4. Use the following command to query the current block height:

   ```bash
   bitcoin-cli getblockcount

Sample Code
If you want to integrate the block height query functionality into your project, you can use the following Python sample code:

   ```base
   import subprocess

def get_block_height():
    try:
        # Call the bitcoin-cli command to get the block height
        result = subprocess.run(["bitcoin-cli", "getblockcount"], stdout=subprocess.PIPE)
        block_height = int(result.stdout.strip())
        return block_height
    except Exception as e:
        print(f"Error: {e}")
        return None

if __name__ == "__main__":
    height = get_block_height()
    if height is not None:
        print(f"Current Block Height: {height}")
   ```

This sample code uses the subprocess module to run the bitcoin-cli command and retrieve the block height.

Notes
Ensure that the Bitcoin Core client is running and has fully synchronized with the blockchain, or the query results may be inaccurate.
Bitcoin Core client must be installed locally to run these commands and sample code.
I hope this simple tutorial is helpful to you! If you have any questions or concerns, feel free to ask.

