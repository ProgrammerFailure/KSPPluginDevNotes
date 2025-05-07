Takes an input, type [string], name [url]. Returns a confignode
	[url] = "path to file relative to GameData/desired confignode"

url example:

File path: GameData/GameDatabaseTest/Settings/test.cfg
File contents:
```
ExemplarNode
{
	testVar = 123
}
NotExemplarNode
{
	testVar = 456
}
```
Desired value: ExemplarNode.testVar
Code to get it.

```
	ConfigNode ExemplarNode = GameDatabaseTest/Settings/test/ExemplarNode;
	int testVar = int.Parse(ExemplarNode.GetValue("testVar"));
```