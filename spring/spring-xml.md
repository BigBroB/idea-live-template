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
### `aut`
##### 描述

`spring` `@Autowired` 语句补全

##### 效果

```
@Autowired
private TestService testService;
```
##### 使用

复制类名，输入`aut`，然后 `Tab`

##### 模板

```
@Autowired
private $VAR$ $VAR_HUMP$$END$;
```

```
<template name="aut" value="@Autowired&#10;private $VAR$ $VAR_HUMP$$END$;" description="Autowired" toReformat="false" toShortenFQNames="true">
  <variable name="VAR" expression="clipboard()" defaultValue="" alwaysStopAt="true" />
  <variable name="VAR_HUMP" expression="camelCase(clipboard())" defaultValue="" alwaysStopAt="true" />
  <context>
    <option name="JAVA_CODE" value="true" />
  </context>
</template>
```
