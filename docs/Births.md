---
id: Births
title: BIRTHS
sidebar_label: BIRTHS
---

<details style="padding: 3%; background: #6DB07F; color: white; border-radius: 4px">
<summary>GET - /births/</summary>


Parameters
```
Parameters          No parameters
```
Responses
```
code: 200

[BirthDetail {
id                  integer
                    title:  ID
                    readOnly:   true
sheep               string
                    title:  Sheep
                    readOnly:   true
                    minLength:  1

}]
```
</details>

<details style="padding: 3%; background: #5388B4; color: white; border-radius: 4px">
<summary>POST - /births/</summary>


Parameters
Data * required

object (body)
```
{
"sheep": 0,
"user": 0,
"date": "2020-10-22T18:18:53.932Z",
"newborns_quantity": 0
}

```
Reponses
```
[BirthDetail {
id	                integer
                    title:  ID
                    readOnly:   true
sheep*	            integer
                    title:  Sheep
user*	            integer
                    title:  User
date*	            string($date-time)
                    title:  Date
newborns_quantity*	integer
                    title:  Newborns quantity
                    maximum: 2147483647
                    minimum: -2147483648

}]
```
</details>

<details style="padding: 3%; background: #6DB07F; color: white; border-radius: 4px">
<summary>GET - /births/{id}/</summary>


Parameters

id * required
integer (path)
	
A unique integer value identifying this birth.
```
"id - A unique integer value identifying this birth."
```
Responses
```
code: 200

[BirthDetail {
id                  integer
                    title:  ID
                    readOnly:   true
sheep*	            integer
                    title:  Sheep
user*	            integer
                    title:  User
date*	            string($date-time)
                    title:  Date
newborns_quantity*	integer
                    title:  Newborns quantity
                    maximum:    2147483647
                    minimum:    -2147483648
}]
```
</details>
