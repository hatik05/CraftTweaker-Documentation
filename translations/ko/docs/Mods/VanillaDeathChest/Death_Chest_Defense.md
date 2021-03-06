# Death Chest Defense

## 패키지 임포트하기

`import mods.vanilladeathchest.DeathChestDefense;`

## Unlocker item

```zenscript
//DeathChestDefense.setUnlocker(string stage, IItemStack unlocker);
DeathChestDefense.setUnlocker("example_stage", <minecraft:diamond_axe> * 1000);
```

A consumption/damage amount can be set by specifying a stack size like above.

## Damage the unlocker item rather than consuming it

```zenscript
//DeathChestDefense.setDamageUnlockerInsteadOfConsume(string stage, bool flag);
DeathChestDefense.setDamageUnlockerInsteadOfConsume("example_stage", true);
```

## Unlock failed chat message

```zenscript
//DeathChestDefense.setUnlockFailedChatMessage(string stage, string message);
DeathChestDefense.setUnlockFailedChatMessage("example_stage", "You need to get a %2$s to unlock your chest!");
```

The string takes two arguments: the amount and display name of the required items.

## Defense entity

```zenscript
//DeathChestDefense.setDefenseEntity(string stage, IEntityDefinition defenseEntity);
DeathChestDefense.setDefenseEntity("example_stage", <entity:minecraft:zombie_pigman>);
```

## Defense entity NBT

```zenscript
//DeathChestDefense.setDefenseEntityNBT(string stage, IData nbt);
DeathChestDefense.setDefenseEntityNBT("example_stage", {
    HandItems: [
        {
            Count: 1,
            id: "minecraft:diamond_sword"
        }
    ]
});
```

`nbt` should be a [DataMap](/Vanilla/Data/DataMap/).

## Defense entity spawn count

```zenscript
//DeathChestDefense.setDefenseEntitySpawnCount(string stage, int count);
DeathChestDefense.setDefenseEntitySpawnCount("example_stage", 500);
```