# GroupService2
Welcome to GroupService2. A new roblox module built with more functions and easy use with roblox-lua-promises.

# Documentation
Ensure you require GroupService2 at the top of your code.

As standard most of the time, functions called will return a ``GroupObject`` type which can be found at ``GroupService2.types.GroupObject``. Some functions have the option to disable this and return a standard table containing usual properties.

## Getting a ``GroupObject``

Run this as standard: ``GroupService2:GetGroup(GroupId: number, GroupObjectSettings(optional))``
This will return an object with lots of feature rich functions!

``local GroupLoadedBoolean, Group = GroupService2:GetGroup(GroupId: number, GroupObjectSettings(optional)):await()``

### Getting a Group Member (PARAMETERS: USERID OR USERNAME)
``Group:GetMember(UserIdentifier: string or number)``
Returns:
```
{
  ["HeadshotThumbnail"] = "rbxthumb://type=AvatarHeadShot&id=654872648&w=60&h=60",
  ["IsPrimary"] = true,
  ["Name"] = "dayflare",
  ["Rank"] = 250,
  ["Role"] = "Vice President",
  ["UserId"] = 654872648
}
```

### Getting Ingame Group Members
``Group:GetIngameMembers()``
Returns:
```
{
  {
    Player = Player,
    Rank = Rank,
    Role = Role
  }
}
```

### Getting Allies (PARAMETERS: RETURN AS GROUP OBJECT [TRUE/FALSE], UPDATECACHE: [TRUE/FALSE] (default false)
``Group:GetAllies(ReturnGroupObject: boolean, UpdateCacheBoolean: boolean)``

### Getting Enemies (PARAMETERS: RETURN AS GROUP OBJECT [TRUE/FALSE], UPDATECACHE: [TRUE/FALSE] (default false)
``Group:GetEnemies(ReturnGroupObject: boolean, UpdateCacheBoolean: boolean)``

### Checking Group Ally (PARAMETERS: GROUPID, CHECKCACHE: BOOLEAN)
``Group.IsAllyOf(QueryAllyId: number, OptionCheckCache: boolean)``
Returns: ``true/false``

### Checking Group Enemy (PARAMETERS: GROUPID, CHECKCACHE: BOOLEAN)
``Group.IsEnemyOf(QueryAllyId: number, OptionCheckCache: boolean)``
Returns: ``true/false``

### Checking If Player is Ally (PARAMETERS: PLAYER: PLAYER)
``local Role, GroupId = Group.IsPlayerAlly(Player: Player)``
Returns:
```
AllyRole, AllyGroupId
```
(Returns ``false, false`` if not an ally)

### Checking If Player is Enemy (PARAMETERS: PLAYER: PLAYER)
``local Role, GroupId = Group.IsPlayerEnemy(Player: Player)``
Returns:
```
EnemyRole, EnemyGroupId
```
(Returns ``false, false`` if not an enemy)

## Events
Ensure ``Events`` is enabled when getting your ``GroupObject`` (default true)

### Special Member Joined Game:
``Group.Data.SpecialPlayerJoined:Connect(function(Player, Mode, GroupId, GroupRole) end``

### Special Member Left Game:
``Group.Data.SpecialPlayerLeft:Connect(function(Player, Mode, GroupId, GroupRole) end``

### Modes:

> Ally
> Enemy
> Member

Any questions, message my portfolio server.
[Discord Server](https://discord.gg/AUxEh8mGTx)

More features will be added soon such as an ranking system etc.
