# idea-live-template
IDEA-live-template 一些好用的 IDEA 模板代码汇集

### `mybatis`
#### IFA 
##### 描述 

`mybatis` `<if>` 标签 

##### 效果


```
<if test="judgeFullName != null ">
    AND judge_full_name = #{judgeFullName}
</if>
```
##### 使用

输入代码 ，使用 `Ctrl + Alt + J`选中，选择 `IFA`

##### 模板

```
<if test="$SELECTION$ != null ">
   AND $VAR1$ $END$ = #{$SELECTION$}
</if>
```

```
<template name="IF" value="&lt;if test=&quot;$SELECTION$ != null &quot;&gt;&#10;   AND $VAR1$ $END$ = #{$SELECTION$}&#10;&lt;/if&gt;" description="if" toReformat="true" toShortenFQNames="true">
  <variable name="VAR1" expression="snakeCase(String)" defaultValue="$SELECTION$" alwaysStopAt="true" />
  <context>
    <option name="SQL" value="true" />
  </context>
</template>
```

#### FI
##### 描述 

`mybatis` `<foreach>` 标签 

##### 效果


```
<foreach item="item" collection="List" separator="," open="(" close=")" index="">
    #{item}
</foreach>
```
##### 使用

输入代码，使用 `Ctrl + Alt + J`选中，选择 `FI`

##### 模板

```
<foreach item="item" collection="$SELECTION$" separator="," open="(" close=")" index="">
    #{item}
</foreach>
```

```
<template name="FI" value="&lt;foreach item=&quot;item&quot; collection=&quot;$SELECTION$&quot; separator=&quot;,&quot; open=&quot;(&quot; close=&quot;)&quot; index=&quot;&quot;&gt;&#10;    #{item}&#10;&lt;/foreach&gt;" description="for earch in" toReformat="true" toShortenFQNames="true">
  <context>
    <option name="SQL" value="true" />
  </context>
</template>
```
#### LikeC
##### 描述 

`MYSQL` `LIKE CONCAT()` 语句补全

##### 效果


```
LIKE CONCAT('%',#{judge_full_name} ,'%' )
```
##### 使用

输入代码，使用 `Ctrl + Alt + J`选中，选择 `LikeC`

##### 模板

```
LIKE CONCAT('%',#{$SELECTION$} ,'%' )
```

```
<template name="LikeC" value="LIKE CONCAT('%',#{$SELECTION$} ,'%' )" description="Like Concat" toReformat="true" toShortenFQNames="true">
  <context>
    <option name="SQL" value="true" />
  </context>
</template>
```
### `spring`

#### `@TS`
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
#### `aut`
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

### `java`

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
