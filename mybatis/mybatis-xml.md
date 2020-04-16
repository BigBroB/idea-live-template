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