<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<title>Thời khóa biểu điện tử</title>
<style>
body {
    font-family: Arial, sans-serif;
    margin: 20px;
}
h1 { margin-bottom: 10px; }
table {
    width: 100%;
    border-collapse: collapse;
}
th, td {
    border: 1px solid #ccc;
    padding: 6px;
    vertical-align: top;
}
th {
    background: #f2f2f2;
    text-align: center;
}
.subject {
    border-bottom: 1px dashed #aaa;
    margin-bottom: 4px;
    padding-bottom: 4px;
}
.subject:last-child { border-bottom: none; }
.subject b { color: red; }
.subject span { color: blue; font-size: 13px; }

#loginBox, #adminBox {
    margin-bottom: 20px;
}
input, select, button {
    padding: 5px;
    margin: 3px 0;
}
.hidden { display: none; }
</style>
</head>

<body>

<h1>Thời khóa biểu</h1>

<!-- ĐĂNG NHẬP -->
<div id="loginBox">
    <b>Đăng nhập giáo vụ</b><br>
    <input id="user" placeholder="Tài khoản"><br>
    <input id="pass" type="password" placeholder="Mật khẩu"><br>
    <button onclick="login()">Đăng nhập</button>
</div>

<!-- QUẢN LÝ -->
<div id="adminBox" class="hidden">
    <b>Thêm môn học</b><br>
    Tháng: <input type="month" id="month"><br>
    Phòng:
    <select id="room">
        <option>LVS, B.101</option>
        <option>ADV, A.103</option>
        <option>ADV, A.104</option>
    </select><br>
    Thứ:
    <select id="day">
        <option value="2">Thứ 2</option>
        <option value="3">Thứ 3</option>
        <option value="4">Thứ 4</option>
        <option value="5">Thứ 5</option>
        <option value="6">Thứ 6</option>
        <option value="7">Thứ 7</option>
    </select><br>
    Tên môn: <input id="name"><br>
    Thời gian: <input id="time"><br>
    Giảng viên: <input id="teacher"><br>
    <button onclick="addSubject()">Thêm</button>
    <button onclick="logout()">Đăng xuất</button>
</div>

<hr>

<input type="month" id="viewMonth" onchange="render()" />

<table>
<thead>
<tr>
    <th>Phòng</th>
    <th>Thứ 2</th>
    <th>Thứ 3</th>
    <th>Thứ 4</th>
    <th>Thứ 5</th>
    <th>Thứ 6</th>
    <th>Thứ 7</th>
</tr>
</thead>
<tbody id="tkb"></tbody>
</table>

<script>
const rooms = ["LVS, B.101", "ADV, A.103", "ADV, A.104"];
const USER = "admin";
const PASS = "123";

function getData() {
    return JSON.parse(localStorage.getItem("tkb") || "{}");
}
function saveData(data) {
    localStorage.setItem("tkb", JSON.stringify(data));
}

function login() {
    if (user.value === USER && pass.value === PASS) {
        loginBox.classList.add("hidden");
        adminBox.classList.remove("hidden");
    } else {
        alert("Sai tài khoản hoặc mật khẩu");
    }
}
function logout() {
    adminBox.classList.add("hidden");
    loginBox.classList.remove("hidden");
}

function addSubject() {
    const m = month.value;
    if (!m) return alert("Chọn tháng");

    const data = getData();
    data[m] = data[m] || {};
    data[m][room.value] = data[m][room.value] || {};
    data[m][room.value][day.value] = data[m][room.value][day.value] || [];

    // cảnh báo trùng
    const exists = data[m][room.value][day.value]
        .some(s => s.time === time.value);
    if (exists) {
        alert("⚠️ Trùng thời gian!");
        return;
    }

    data[m][room.value][day.value].push({
        name: name.value,
        time: time.value,
        teacher: teacher.value
    });

    saveData(data);
    render();
}

function render() {
    const m = viewMonth.value;
    const body = document.getElementById("tkb");
    body.innerHTML = "";

    if (!m) return;
    const data = getData()[m] || {};

    rooms.forEach(r => {
        let hasSubject = false;
        for (let d = 2; d <= 7; d++) {
            if (data[r]?.[d]?.length) {
                hasSubject = true;
                break;
            }
        }
        if (!hasSubject) return; // ❌ không hiện phòng trống

        const tr = document.createElement("tr");
        const tdRoom = document.createElement("td");
        tdRoom.textContent = r;
        tr.appendChild(tdRoom);

        for (let d = 2; d <= 7; d++) {
            const td = document.createElement("td");
            (data[r]?.[d] || []).forEach(s => {
                const div = document.createElement("div");
                div.className = "subject";
                div.innerHTML = `<b>${s.name}</b><br>${s.time}<br><span>${s.teacher}</span>`;
                td.appendChild(div);
            });
            tr.appendChild(td);
        }
        body.appendChild(tr);
    });
}
</script>

</body>
</html>
