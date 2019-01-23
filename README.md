# DiceBot
DiceBot is a Discord bot for tabletop gaming written in Python

# Features
  - Roll dice using formulas
  - Supports fudge dice with `ndf`

# Usage
You can roll dice using formulas.
Examples:
`/roll 1d20`
```markdown
Result: 5, Individual Rolls: [5]
```
`/roll 3df`
```markdown
Result: 2, Individual Rolls: [+,-,+]
```
`/roll 2d10`
```markdown
Result: 7, Individual Rolls: [3,4]
```
Arithmetic operators (+,-,*,/,^) and parenthesis are supported. Order of operations is respected.
Examples:
`/roll 1d20 + 10`
```markdown
Result: 18, Individual Rolls: [8]
```
`/roll (1d2*3) + (1d3*4)`
```markdown
Result: 14, Individual Rolls: [2,2]
```
You can even mix regular dice and fudge dice.
Examples:
`/roll 10df + 1d10`
```markdown
Result: 5, Individual Rolls: [-, -, +, +, ., ., -, +, +, +, 3]
```
Who even needs dice? DiceBot is content just to do math.
Examples:
`/roll 5 + 10`
```markdown
Result: 15
```
# Planned Features
  - Flip a coin
  - Percent chance without dice
  - Rock Paper Scissors

# Possible Features
  - Greater control from users with `GameMaster` role
  - Import and persist character json from Mythweavers character sheets for rolls like `/roll gandalf attack staff` 
  - Suggest other features by creating an [issue](https://github.com/TravisAGengler/DiceBot/issues) and giving it the label `enhancement`

# config.json
If you want to run your own DiceBot, you'll need to create a `config.json` file to store your Bot's token. Here is a sample `config.json`:
```json
{
	"bot_token" : "MY_SUPER_SECRET_TOKEN"
}
```
Pass the path to this file as the first argument to your invocation of `DiceBot.py`. By default, DiceBot looks for `./config.json`
