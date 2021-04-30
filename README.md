# Ajax ส่งค่า ID submit แล้ว alert

```javascript
$(document).on("click","#submit", function(e){
        e.preventDefault();
        alert("click");
    })
```

# Ajax ส่งค่า ID submit แล้ว alert

```javascript

$(document).on("click", "#package1", function(e) {
        e.preventDefault();

        var username = $("#username").val();
        var password = $("#password").val();

        $.ajax({
            url: "",
            type: "post",
            data: {
                username:username,
                password:password,
            },
        })

    })

```
