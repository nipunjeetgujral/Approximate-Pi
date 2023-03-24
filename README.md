# Approximate-Pi
Using Various Methods to Approximate Pi


## Table of Contents


0. [Define Problem](#0.-Define-Problem)
1. [Import Libraries](#)
2. [Estimate $\pi$ using Monte Carlo Simulation](#)
3. [Estimate $\pi$ using Taylor Series Expansion](#) 
4. [Estimate $\pi$ using Quantum Accelerated Monte Carlo Simulation](#) 
    * Generate Random 8-bit Numbers
    * Normalize Random Numbers Between [0,1]
    * Measure Circle vs. Square Ratio
5. [Analysis of Performance](#)
    * Accuracy
    * Speed
6. [Conclusion - Which is better?](#)


### 0. Define Problem


![thing](https://learn-us-east-1-prod-fleet02-xythos.content.blackboardcdn.com/5df7f1d815fec/7431027?X-Blackboard-S3-Bucket=learn-us-east-1-prod-fleet01-xythos&X-Blackboard-Expiration=1679648400000&X-Blackboard-Signature=k%2Byny7ZoOXH4cxUAYxwyHjR%2B3a7geeC9XX9Jue10y8A%3D&X-Blackboard-Client-Id=103873&X-Blackboard-S3-Region=us-east-1&response-cache-control=private%2C%20max-age%3D21600&response-content-disposition=inline%3B%20filename%2A%3DUTF-8%27%27monte.gif&response-content-type=image%2Fgif&X-Amz-Security-Token=IQoJb3JpZ2luX2VjEAQaCXVzLWVhc3QtMSJIMEYCIQD8gD6vshZG3CKiF76ITNIxo6%2FJyRGGjMDZReBQvCqh2AIhAMUUZ1g2Xm2QTZ5z3%2FOwdQpft9G4vi74GdzYviTXghJ0KrsFCM3%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQAxoMNjM1NTY3OTI0MTgzIgwimQAPk6GaCkOwCkAqjwVQdJtijlrp%2F8nrK3bMrM2id9lAc3nTFx1XzszMhkgm5VJcD%2BoeoJkJfIQsWCZVyxxhIUJl64NyhRyrucNvPZqkwQWq5QN2v2tzDJ%2FRtjPnQoSafPHYVmOHEiFp0TOkzdcjvf6l3UZ3Jb%2FaCdNLSCjISXXaNWqHfN9q5%2BGM173MUsefBHAu7hRknceziPyWEk4JbSojxzkBk719ZtXCJpHxxI1jlIaA8j9qJhsqhOP10wMVxKBpeFUvHC0ehnXl7pa3lk7c3WLHTHYIotjBn6%2FTuiKaNy52aqy3pKP386aydsNSmOwlP1sinw6yLAF7%2BUy8b8sZWlHymgOaZ2xNE7z8lIvKjvTSXykFxddF4fpgnkc5ue7coCu2ouT%2FV8v6WA7JNUKJJ22S7JUa%2BM9fTPZUzZjeJAN55WiYHEQjAMMsNLoZwRSKR8H98Q0N4xWvqTsfpuLUaV6iKqB4p0svId2q%2Fke3rwOd0KaYnn3kZNZlu7MqInH14tw5TiAfjCj9%2BENgXWfmXtrCp3FRRKVEOu507wIvkt9yiPDeSwayK5J98x58yLr55yBIlG4j5NhZpjLXWt9RPa9%2FKQgNZVve%2FDNs%2BjH8OMSrrzwccVBnXKyx1QYciuG6M8UfVJeUWF9fcoT5tB1WHyYMivHGBhFG%2B%2FplNDMcDK967HGEZNi5VsAL6Ek7uv73isDfkn3naU7cpCstceHRbaNEiOqtZ1ZtC0C2Fc9QTUViEOsw6ak6QcwrrE96F5BTQW99T%2Fl%2BbQlr0S2leK8qva71A1yMoF9GxW3fTMUbYappyySoKYBSOblpZ4pyFyJY0%2FldWxNWX3EoJfYQFVRnNZMtbDwYpm%2BqLpcE95piQgUkfQY6tkJRsn3WMIK39KAGOrABEZJgmpOkp%2FPLclAIrjMExKW1qyS2cJrLJkpIRe6dPhCa4nCmE%2F8d%2Bz5Mw%2BTMKLFeLGZKQUuXVqZjTw54c%2FwujsAYEiKBp1h3ec%2FORn4ImW05Mck1xtoVZ2Khk46VUJy7cbHJ9keQpflhikgER3zkq5J%2BtU5BXsiiVy2UzwG3f8HLThd3UQQu12PfSyEdwUqGRw124U6szIcND16MAP6IY7qG%2Bt4S0xVMTGThhGlyNEs%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20230324T030000Z&X-Amz-SignedHeaders=host&X-Amz-Expires=21600&X-Amz-Credential=ASIAZH6WM4PLRPKROC45%2F20230324%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=7b0080df5709130bf0bcd5e65bbef986482eb54504dca7728f5e2b12cdc05be1)
