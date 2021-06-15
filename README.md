
# Realtime อ่อนด๋อย
```javascript
<select id="list" onchange="getSelectValue();">
                            <option value="js">JavaScript</option>
                            <option value="php">PHP</option>
                            <option value="c#">Csharp</option>
                            <option value="java">Java</option>
                            <option value="node">Node.js</option>
                        </select>
                        <script>
                            function getSelectValue() {
                                var selectedValue = document.getElementById("list").value;
                                console.log(selectedValue);
                                document.getElementById("markno1").innerHTML = selectedValue;
                            }
                            getSelectValue();
                        </script>
                        <h1 id="markno1"></h1>

```

# Ajax ส่งค่าแล้วเช็ค Response
```javascript
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
