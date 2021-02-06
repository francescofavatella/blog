---
title: Bash script
---

## Arrays

```
#! /bin/bash

MY_ARRAY=(first second third)


for elem in ${MY_ARRAY[*]};
do
	echo $elem
done
```
