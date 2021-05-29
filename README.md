# Ajax ส่งค่าแล้วเช็ค Response
```
$(document).on("click", "#package7", function(e) {
        e.preventDefault();

        var uid = $("#uid").val();
        var package7 = $("#package7").val();

        $.ajax({
            url: "/include/api_ff.php?action=package7",
            type: "post",
            data: {
                uid: uid,
                package7: package7,
            },
            success: function(data) {
                if(data.status == "error"){
                    swal.fire('ขออภัยค่ะ' , data.message, data.status);
                }else if(data.status == "success"){
                    swal.fire('ทำรายการเรียบร้อย' , data.message, data.status);
                }
            }
        })

    })
```

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
