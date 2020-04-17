### `@TS`
##### 描述 

`spring` `@Transactional(rollbackFor = Exception.class)` 语句补全

##### 效果

```
@Transactional(rollbackFor = Exception.class)
```
##### 使用

输入`@TS`，然后 `Tab`

##### 模板

```
 @Transactional(rollbackFor = Exception.class $END$)
```

```
<template name="@TS" value=" @Transactional(rollbackFor = Exception.class $END$)" description="@Transactional" toReformat="false" toShortenFQNames="true" useStaticImport="true">
  <context>
    <option name="JAVA_CODE" value="true" />
  </context>
</template>
```