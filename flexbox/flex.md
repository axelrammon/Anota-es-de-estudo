## Flex direction

```css
.flex-container {
	display: flex;
}

.direction {
	flex-direction: row | row-reverse | column | column-reverse; 
}

/* 
	<div class="flex-container direction"></div> 
	Por padrão vem ROW
*/
```

![flex-direction](/home/axel/Workspace/anotacoes-de-estudo/imgs/flex-direction.png)

## Flex wrap

```css
.flex-container {
	display: flex;
}

.wrap {
	flex-wrap: nowrap | wrap | wrap-reverse;
}

/* 
	<div class="flex-container direction"></div> 
	Por padrão vem NOWRAP
*/
```

![flex-wrap](/home/axel/Workspace/anotacoes-de-estudo/imgs/flex-wrap.png)

## Flex flow

```css
.flex-container {
	display: flex;
}

.flow {
	flex-flow: row nowrap | row wrap | column nowrap | column wrap;
    /* flex-flow: flex-direction flex-wrap */
}

/* 
	<div class="flex-container direction"></div> 
	Por padrão vem NOWRAP
*/
```

