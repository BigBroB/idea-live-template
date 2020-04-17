
#### `ps`
##### 描述 

根据剪贴板生成实体`String`字段

##### 效果

```
/**
 * 
 */
private String test;
```
##### 使用

输入`ps`，然后 `Tab`

##### 模板

```
 /**
 * $DESC$
 */
private String $VAR$$END$;
```

```
<template name="ps" value="/**&#10; * $DESC$&#10; */&#10;private String $VAR$$END$;" description="private String" toReformat="false" toShortenFQNames="true">
  <variable name="DESC" expression="" defaultValue="" alwaysStopAt="true" />
  <variable name="VAR" expression="clipboard()" defaultValue="" alwaysStopAt="true" />
  <context>
    <option name="JAVA_CODE" value="true" />
  </context>
</template>
```

#### `pi`
##### 描述 

根据剪贴板生成实体`String`字段

##### 效果

```
/**
 * 
 */
private Integer test;
```
##### 使用

输入`pi`，然后 `Tab`

##### 模板

```
/**
 * $DESC$
 */
private Integer $VAR$$END$;
```

```
<template name="pi" value="/**&#10; * $DESC$&#10; */&#10;private Integer $VAR$$END$;" description="private Integer" toReformat="false" toShortenFQNames="true">
  <variable name="DESC" expression="" defaultValue="" alwaysStopAt="true" />
  <variable name="VAR" expression="clipboard()" defaultValue="" alwaysStopAt="true" />
  <context>
    <option name="JAVA_CODE" value="true" />
  </context>
</template>
```