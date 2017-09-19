NOTE: This project was previously stored privately, because it contained sensitive account information. I am publishing it now after stripping away all of that information. This is why there is a lack of change history. This project was created by me back in 2014, and is no longer actively maintained.

This project interfaces with five different exchanges to automatically detect and leverage arbitrage opportunities. It consists of slaves that gather market data (these should all be at different IPs), and a master that spawns slaves, analyzes market data, detects arbitrage, and executes trades. The purpose of the slaves is to bypass QPS limitations. For instance, with a 10 second per query limit and 5 slaves, we can (theoretically) achieve close to 2 seconds per update. It automatically detects and adjusts for new or dead slaves via a DNS server (this can be adjusted in the code to suit your needs).
