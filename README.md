<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ECE Result Portal | Panjab University Chandigarh</title>

<style>
*{box-sizing:border-box;margin:0;padding:0}

:root{
--orange:#ef7d22;
--orange2:#d96712;
--teal:#173f3f;
--teal2:#285b5b;
--cream:#f7f0e5;
--white:#fffdf9;
--line:#e8dfd2;
--muted:#737373;
--red:#c62828;
--green:#2e7d32;
}

body{
font-family:Arial,Helvetica,sans-serif;
background:var(--cream);
color:#222;
}

button,input,select,textarea{font:inherit}
button{cursor:pointer}
.hidden{display:none!important}

/* LOGIN */

.login-page{
min-height:100vh;
display:flex;
align-items:center;
justify-content:center;
padding:22px;
background:linear-gradient(135deg,#f07d22,#f5bc68);
}

.login-card{
width:100%;
max-width:440px;
background:var(--white);
padding:34px;
border-radius:22px;
box-shadow:0 18px 55px #0003;
}

.logo{
width:86px;
height:86px;
border-radius:50%;
margin:0 auto 15px;
background:var(--orange);
border:6px solid #f8d8af;
color:#fff;
display:flex;
align-items:center;
justify-content:center;
font-size:25px;
font-weight:800;
}

.login-card h1{
text-align:center;
color:var(--teal);
font-size:25px;
}

.login-card .sub{
text-align:center;
color:var(--muted);
margin:7px 0 25px;
}

.form-group{margin-bottom:15px}

label{
display:block;
font-weight:700;
margin-bottom:7px;
font-size:14px;
}

input,select,textarea{
width:100%;
padding:12px 13px;
border:1px solid #d9d2c8;
border-radius:9px;
background:#fff;
outline:none;
}

input:focus,select:focus,textarea:focus{
border-color:var(--orange);
box-shadow:0 0 0 2px #ef7d2220;
}

textarea{
min-height:90px;
resize:vertical;
}

.login-btn,.primary{
width:100%;
border:0;
background:var(--orange);
color:#fff;
padding:13px 18px;
border-radius:9px;
font-weight:800;
}

.login-btn:hover,.primary:hover{
background:var(--orange2);
}

.login-msg{
text-align:center;
min-height:22px;
margin-top:12px;
color:var(--red);
font-size:14px;
}

/* HEADER */

.header{
height:72px;
position:fixed;
top:0;
left:0;
right:0;
z-index:1000;
background:var(--teal);
color:#fff;
display:flex;
align-items:center;
padding:0 18px;
}

.menu-btn{
width:44px;
height:44px;
border:0;
background:transparent;
color:#fff;
font-size:27px;
border-radius:8px;
}

.menu-btn:hover{background:#ffffff18}

.header-title{margin-left:12px}

.header-title h2{font-size:19px}

.header-title p{
font-size:11px;
color:#d7e6e6;
margin-top:3px;
}

.header-user{
margin-left:auto;
font-size:14px;
}

/* SIDEBAR */

.sidebar{
position:fixed;
z-index:1100;
top:72px;
bottom:0;
left:0;
width:275px;
background:var(--white);
box-shadow:5px 0 20px #0002;
transform:translateX(-105%);
transition:.25s;
overflow:auto;
}

.sidebar.open{transform:translateX(0)}

.side-head{
padding:22px;
border-bottom:1px solid var(--line);
color:var(--teal);
}

.nav{padding:14px}

.nav button{
display:block;
width:100%;
border:0;
background:transparent;
text-align:left;
padding:13px 14px;
border-radius:9px;
margin-bottom:5px;
color:#333;
}

.nav button:hover{background:#f8e6d2}

.nav button.active{
background:var(--orange);
color:#fff;
}

.nav .logout{
color:var(--red);
margin-top:14px;
}

.overlay{
position:fixed;
z-index:1050;
inset:72px 0 0;
background:#0005;
display:none;
}

.overlay.show{display:block}

/* MAIN */

.main{
padding:100px 25px 35px;
min-height:100vh;
}

.container{
max-width:1200px;
margin:auto;
}

.page-title{
color:var(--teal);
font-size:28px;
margin-bottom:6px;
}

.page-sub{
color:var(--muted);
margin-bottom:22px;
}

.welcome{
background:linear-gradient(135deg,var(--teal),var(--teal2));
color:#fff;
padding:27px;
border-radius:17px;
margin-bottom:22px;
}

.welcome h2{margin-bottom:8px}

.welcome p{color:#dce8e8}

.grid4{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:16px;
}

.stat,.card{
background:#fff;
border-radius:15px;
padding:21px;
box-shadow:0 5px 18px #0000000d;
}

.stat h3{
color:var(--orange);
font-size:28px;
margin-bottom:5px;
}

.stat p{color:#777}

.card{margin-bottom:20px}

.card h3{
color:var(--teal);
margin-bottom:16px;
}

.profile-grid{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:14px;
}

.info{
background:#faf7f1;
border:1px solid var(--line);
padding:15px;
border-radius:10px;
}

.info small{
display:block;
color:#888;
margin-bottom:5px;
}

.form-grid{
display:grid;
grid-template-columns:repeat(2,1fr);
gap:15px;
}

.full{grid-column:1/-1}

.actions{
display:flex;
gap:9px;
flex-wrap:wrap;
margin-top:8px;
}

.primary{width:auto}

.secondary{
border:0;
background:var(--teal);
color:#fff;
padding:11px 17px;
border-radius:9px;
font-weight:700;
}

.danger{
border:0;
background:var(--red);
color:#fff;
padding:8px 12px;
border-radius:7px;
}

.edit{
border:0;
background:var(--teal);
color:#fff;
padding:8px 12px;
border-radius:7px;
margin-right:5px;
}

/* TABLE */

.table-wrap{
overflow-x:auto;
}

table{
width:100%;
border-collapse:collapse;
background:#fff;
}

th,td{
padding:12px;
border-bottom:1px solid #eee;
text-align:left;
white-space:nowrap;
}

thead{
background:var(--teal);
color:#fff;
}

.badge{
display:inline-block;
padding:5px 9px;
border-radius:5px;
font-size:12px;
font-weight:700;
}

.theory{
background:#e6f0f7;
color:#235578;
}

.practical{
background:#f8e5d2;
color:#9b4f10;
}

.grade{
background:#edf4e9;
color:#315f2d;
}

.grade-f{
background:#f8dddd;
color:#a32626;
}

/* RESULTS */

.result-controls{
display:flex;
gap:12px;
align-items:end;
flex-wrap:wrap;
}

.result-controls .form-group{
min-width:210px;
margin:0;
}

.result-summary{
display:grid;
grid-template-columns:repeat(4,1fr);
gap:14px;
margin-top:18px;
}

.summary{
background:#fbefe0;
border-radius:12px;
padding:18px;
text-align:center;
}

.summary strong{
display:block;
color:var(--orange);
font-size:26px;
margin-top:5px;
}

.result-head{
background:#fff;
border-radius:15px;
padding:22px;
margin-bottom:15px;
}

.result-meta{
display:grid;
grid-template-columns:repeat(3,1fr);
gap:13px;
margin-top:16px;
}

.meta{
padding:12px;
background:#faf7f1;
border-radius:9px;
}

.meta small{
display:block;
color:#888;
margin-bottom:4px;
}

/* SEMESTERS */

.sem-section{margin-bottom:20px}

.sem-head{
background:var(--teal);
color:#fff;
padding:13px 17px;
border-radius:11px 11px 0 0;
display:flex;
justify-content:space-between;
align-items:center;
}

.sem-head h3{
margin:0;
color:#fff;
}

.count{
background:var(--orange);
padding:4px 9px;
border-radius:20px;
font-size:12px;
}

.empty{
background:#fff;
padding:20px;
color:#777;
border:1px solid var(--line);
border-top:0;
border-radius:0 0 11px 11px;
}

/* MODAL */

.modal{
display:none;
position:fixed;
z-index:2000;
inset:0;
background:#0006;
padding:20px;
overflow:auto;
}

.modal.show{
display:flex;
justify-content:center;
align-items:flex-start;
}

.modal-card{
width:100%;
max-width:720px;
background:var(--white);
border-radius:17px;
padding:24px;
margin-top:35px;
}

.modal-head{
display:flex;
justify-content:space-between;
align-items:center;
margin-bottom:18px;
}

.modal-head h3{color:var(--teal)}

.close{
border:0;
background:transparent;
font-size:27px;
}

.notice{
padding:13px;
background:#eef6f2;
border:1px solid #d9ebe3;
color:#315b4c;
border-radius:9px;
margin-bottom:15px;
}

/* MOBILE */

@media(max-width:900px){

.grid4{
grid-template-columns:repeat(2,1fr);
}

.result-summary{
grid-template-columns:repeat(2,1fr);
}

}

@media(max-width:650px){

.header{height:65px}

.sidebar{top:65px}

.overlay{inset:65px 0 0}

.header-title h2{font-size:15px}

.header-title p,
.header-user{
display:none;
}

.main{
padding:85px 14px 25px;
}

.grid4{
grid-template-columns:1fr 1fr;
gap:10px;
}

.profile-grid,
.form-grid,
.result-meta{
grid-template-columns:1fr;
}

.full{grid-column:auto}

.result-summary{
grid-template-columns:1fr 1fr;
}

}

@media print{

.header,
.sidebar,
.overlay,
.no-print{
display:none!important;
}

.main{padding:0}

body{background:#fff}

.card{
box-shadow:none;
}

}
</style>
</head>

<body>

<!-- ================= LOGIN ================= -->

<div id="loginPage" class="login-page">

<div class="login-card">

<div class="logo">ECE</div>

<h1>ECE Student Result Portal</h1>

<div class="sub">
Panjab University, Chandigarh
</div>

<div class="form-group">
<label>Username</label>
<input id="loginUser" placeholder="Enter username">
</div>

<div class="form-group">
<label>Password</label>
<input id="loginPass" type="password" placeholder="Enter password">
</div>

<div class="form-group">
<label>Login As</label>

<select id="loginRole">
<option value="">Select Role</option>
<option value="student">Student</option>
<option value="faculty">Faculty</option>
</select>

</div>

<button class="login-btn" id="loginBtn">
LOGIN
</button>

<div id="loginMsg" class="login-msg"></div>

</div>
</div>


<!-- ================= PORTAL ================= -->

<div id="portal" class="hidden">

<header class="header">

<button id="menuBtn" class="menu-btn">
☰
</button>

<div class="header-title">
<h2>ECE Result Portal</h2>
<p>Panjab University, Chandigarh</p>
</div>

<div id="headerUser" class="header-user"></div>

</header>

<div id="overlay" class="overlay"></div>

<aside id="sidebar" class="sidebar">

<div class="side-head">
<strong id="sideUser">ECE Portal</strong>
</div>

<nav id="nav" class="nav">

<button data-page="dashboard">
Dashboard
</button>

<button data-page="students" data-faculty>
Students
</button>

<button data-page="subjects" data-faculty>
Subjects
</button>

<button data-page="addResult" data-faculty>
Add Result
</button>

<button data-page="result">
Result
</button>

<button data-page="profile">
Profile
</button>

<button data-page="syllabus">
Syllabus
</button>

<button id="logoutBtn" class="logout">
Logout
</button>

</nav>

</aside>

<main id="main" class="main"></main>

</div>


<!-- ================= STUDENT MODAL ================= -->

<div id="studentModal" class="modal">

<div class="modal-card">

<div class="modal-head">
<h3 id="studentModalTitle">Add Student</h3>
<button class="close" data-close="studentModal">×</button>
</div>

<input type="hidden" id="editStudentId">

<div class="form-grid">

<div class="form-group">
<label>Name</label>
<input id="sName">
</div>

<div class="form-group">
<label>Roll Number</label>
<input id="sRoll">
</div>

<div class="form-group">
<label>Username</label>
<input id="sUsername">
</div>

<div class="form-group">
<label>Password</label>
<input id="sPassword">
</div>

<div class="form-group">
<label>Father Name</label>
<input id="sFather">
</div>

<div class="form-group">
<label>Mother Name</label>
<input id="sMother">
</div>

<div class="form-group">
<label>Email</label>
<input id="sEmail" type="email">
</div>

<div class="form-group">
<label>Contact Number</label>
<input id="sPhone">
</div>

<div class="form-group">
<label>Date of Birth</label>
<input id="sDob" type="date">
</div>

<div class="form-group">
<label>Gender</label>

<select id="sGender">
<option>Female</option>
<option>Male</option>
<option>Other</option>
</select>

</div>

<div class="form-group full">
<label>Address</label>
<textarea id="sAddress"></textarea>
</div>

</div>

<div class="actions">

<button id="saveStudent" class="primary">
Save Student
</button>

<button class="secondary" data-close="studentModal">
Cancel
</button>

</div>

</div>
</div>


<!-- ================= SUBJECT MODAL ================= -->

<div id="subjectModal" class="modal">

<div class="modal-card">

<div class="modal-head">

<h3 id="subjectModalTitle">
Add Subject
</h3>

<button class="close" data-close="subjectModal">
×
</button>

</div>

<input type="hidden" id="editSubjectId">

<div class="form-grid">

<div class="form-group">
<label>Subject Name</label>
<input id="subName">
</div>

<div class="form-group">
<label>Subject Code</label>
<input id="subCode">
</div>

<div class="form-group">
<label>Type</label>

<select id="subType">
<option>Theory</option>
<option>Practical</option>
</select>

</div>

<div class="form-group">
<label>Credits</label>
<input id="subCredits" type="number" min="0" max="10">
</div>

<div class="form-group">
<label>Semester</label>

<select id="subSemester">
<option value="1">Semester 1</option>
<option value="2">Semester 2</option>
<option value="3">Semester 3</option>
<option value="4">Semester 4</option>
<option value="5">Semester 5</option>
<option value="6">Semester 6</option>
<option value="7">Semester 7</option>
<option value="8">Semester 8</option>
</select>

</div>

</div>

<div class="actions">

<button id="saveSubject" class="primary">
Save Subject
</button>

<button class="secondary" data-close="subjectModal">
Cancel
</button>

</div>

</div>
</div>


<!-- ================= RESULT MODAL ================= -->

<div id="resultModal" class="modal">

<div class="modal-card">

<div class="modal-head">

<h3 id="resultModalTitle">
Add Result
</h3>

<button class="close" data-close="resultModal">
×
</button>

</div>

<input type="hidden" id="editResultId">

<div class="form-grid">

<div class="form-group">
<label>Student</label>
<select id="rStudent"></select>
</div>

<div class="form-group">

<label>Semester</label>

<select id="rSemester">
<option value="1">Semester 1</option>
<option value="2">Semester 2</option>
<option value="3">Semester 3</option>
<option value="4">Semester 4</option>
<option value="5">Semester 5</option>
<option value="6">Semester 6</option>
<option value="7">Semester 7</option>
<option value="8">Semester 8</option>
</select>

</div>

<div class="form-group">

<label>Subject</label>

<select id="rSubject"></select>

</div>

<div class="form-group">

<label>Grade</label>

<select id="rGrade">
<option>A+</option>
<option>A</option>
<option>B+</option>
<option>B</option>
<option>C+</option>
<option>C</option>
<option>D</option>
<option>F</option>
<option>S</option>
</select>

</div>

</div>

<div class="actions">

<button id="saveResult" class="primary">
Save Result
</button>

<button class="secondary" data-close="resultModal">
Cancel
</button>

</div>

</div>
</div>


<script>

/* =========================================================
   DATABASE
========================================================= */

/*
 IMPORTANT:
 The old dummy subject/result database has been replaced
 with the subjects and grades from the supplied screenshots.

 Student and faculty login are kept.
*/

const defaultStudents = [

{
id:"student1",
username:"gunjita",
password:"GUN2007",
name:"Gunjita",
father:"Vinod Kumar",
mother:"Babli",
email:"gunjita@example.com",
phone:"9876543210",
dob:"2007-07-02",
gender:"Female",
address:"Chandigarh, Punjab",
roll:"ECE2026/001"
}

];


/* =========================================================
   SUBJECTS - SEMESTER 1
========================================================= */

const defaultSubjects = [

/* SEMESTER 1 */

{
id:"s1_1",
code:"ASCX01",
name:"Applied Chemistry",
credits:4,
semester:1,
type:"Theory"
},

{
id:"s1_2",
code:"ASCX51",
name:"Applied Chemistry",
credits:1,
semester:1,
type:"Practical"
},

{
id:"s1_3",
code:"EECX01",
name:"Basic Electrical and Electronics Engineering",
credits:3,
semester:1,
type:"Theory"
},

{
id:"s1_4",
code:"EECX51",
name:"Basic Electrical and Electronics Engineering",
credits:1,
semester:1,
type:"Practical"
},

{
id:"s1_5",
code:"ASM101",
name:"Calculus",
credits:4,
semester:1,
type:"Theory"
},

{
id:"s1_6",
code:"ESCX04",
name:"Engineering Graphics",
credits:1,
semester:1,
type:"Theory"
},

{
id:"s1_7",
code:"ESCX54",
name:"Engineering Graphics",
credits:1,
semester:1,
type:"Practical"
},

{
id:"s1_8",
code:"EVSX01",
name:"Environment Science",
credits:0,
semester:1,
type:"Theory"
},

{
id:"s1_9",
code:"ESCX01",
name:"Programming Fundamentals",
credits:3,
semester:1,
type:"Theory"
},

{
id:"s1_10",
code:"ESCX51",
name:"Programming Fundamentals",
credits:1,
semester:1,
type:"Practical"
},


/* SEMESTER 2 */

{
id:"s2_1",
code:"ASPX01",
name:"Applied Physics",
credits:4,
semester:2,
type:"Theory"
},

{
id:"s2_2",
code:"ASPX51",
name:"Applied Physics",
credits:1,
semester:2,
type:"Practical"
},

{
id:"s2_3",
code:"ASM201",
name:"Differential Equation and Transforms",
credits:4,
semester:2,
type:"Theory"
},

{
id:"s2_4",
code:"EC203",
name:"Digital Design",
credits:3,
semester:2,
type:"Theory"
},

{
id:"s2_5",
code:"EC253",
name:"Digital Design",
credits:1,
semester:2,
type:"Practical"
},

{
id:"s2_6",
code:"ST251",
name:"Product Re-engineering and Innovation",
credits:0,
semester:2,
type:"Practical"
},

{
id:"s2_7",
code:"HSMCX01",
name:"Professional Communication",
credits:2,
semester:2,
type:"Theory"
},

{
id:"s2_8",
code:"HSMCX51",
name:"Professional Communication",
credits:1,
semester:2,
type:"Practical"
},

{
id:"s2_9",
code:"UHV01",
name:"Universal Human Values",
credits:0,
semester:2,
type:"Theory"
},

{
id:"s2_10",
code:"ESCX53",
name:"Workshop",
credits:2,
semester:2,
type:"Practical"
},


/* SEMESTER 3 */

{
id:"s3_1",
code:"HSS-301",
name:"Economics",
credits:3,
semester:3,
type:"Theory"
},

{
id:"s3_2",
code:"EC-307",
name:"Electronic Devices and Circuits",
credits:0,
semester:3,
type:"Theory"
},

{
id:"s3_3",
code:"EC-307",
name:"Electronic Devices and Circuits",
credits:1,
semester:3,
type:"Practical"
},

{
id:"s3_4",
code:"EC306",
name:"Electronic Measurements & Instrumentation",
credits:3,
semester:3,
type:"Theory"
},

{
id:"s3_5",
code:"EC306",
name:"Electronic Measurements & Instrumentation",
credits:1,
semester:3,
type:"Practical"
},

{
id:"s3_6",
code:"MATHS-301",
name:"Linear Algebra & Complex Analysis",
credits:0,
semester:3,
type:"Theory"
},

{
id:"s3_7",
code:"EC304",
name:"Microprocessor and Microcontrollers",
credits:4,
semester:3,
type:"Theory"
},

{
id:"s3_8",
code:"EC304",
name:"Microprocessor and Microcontrollers",
credits:1,
semester:3,
type:"Practical"
},

{
id:"s3_9",
code:"EC302",
name:"Signals and Systems",
credits:0,
semester:3,
type:"Theory"
},


/* SEMESTER 4 */

{
id:"s4_1",
code:"EC402",
name:"Advanced Microcontrollers & Applications",
credits:3,
semester:4,
type:"Theory"
},

{
id:"s4_2",
code:"EC402",
name:"Advanced Microcontrollers & Applications",
credits:1,
semester:4,
type:"Practical"
},

{
id:"s4_3",
code:"EC406",
name:"Analog Electronics Circuits",
credits:3,
semester:4,
type:"Theory"
},

{
id:"s4_4",
code:"EC406",
name:"Analog Electronics Circuits",
credits:1,
semester:4,
type:"Practical"
},

{
id:"s4_5",
code:"EC401",
name:"Communication Engineering",
credits:3,
semester:4,
type:"Theory"
},

{
id:"s4_6",
code:"EC401",
name:"Communication Engineering",
credits:1,
semester:4,
type:"Practical"
},

{
id:"s4_7",
code:"EC-408",
name:"Electromagnetic Theory",
credits:3,
semester:4,
type:"Theory"
},

{
id:"s4_8",
code:"EC409",
name:"Network Analysis",
credits:3,
semester:4,
type:"Theory"
},

{
id:"s4_9",
code:"EC409",
name:"Network Analysis",
credits:1,
semester:4,
type:"Practical"
},

{
id:"s4_10",
code:"EC407",
name:"Probability and Random Processes",
credits:3,
semester:4,
type:"Theory"
}

];


/* =========================================================
   RESULTS FROM SCREENSHOTS
========================================================= */

const defaultResults = [

/* SEMESTER 1 */

{
id:"r1",
student:"gunjita",
semester:1,
subjectId:"s1_1",
grade:"C+"
},

{
id:"r2",
student:"gunjita",
semester:1,
subjectId:"s1_2",
grade:"C+"
},

{
id:"r3",
student:"gunjita",
semester:1,
subjectId:"s1_3",
grade:"B+"
},

{
id:"r4",
student:"gunjita",
semester:1,
subjectId:"s1_4",
grade:"B"
},

{
id:"r5",
student:"gunjita",
semester:1,
subjectId:"s1_5",
grade:"F"
},

{
id:"r6",
student:"gunjita",
semester:1,
subjectId:"s1_6",
grade:"C+"
},

{
id:"r7",
student:"gunjita",
semester:1,
subjectId:"s1_7",
grade:"D"
},

{
id:"r8",
student:"gunjita",
semester:1,
subjectId:"s1_8",
grade:"S"
},

{
id:"r9",
student:"gunjita",
semester:1,
subjectId:"s1_9",
grade:"C+"
},

{
id:"r10",
student:"gunjita",
semester:1,
subjectId:"s1_10",
grade:"B"
},


/* SEMESTER 2 */

{
id:"r11",
student:"gunjita",
semester:2,
subjectId:"s2_1",
grade:"B"
},

{
id:"r12",
student:"gunjita",
semester:2,
subjectId:"s2_2",
grade:"D"
},

{
id:"r13",
student:"gunjita",
semester:2,
subjectId:"s2_3",
grade:"F"
},

{
id:"r14",
student:"gunjita",
semester:2,
subjectId:"s2_4",
grade:"C"
},

{
id:"r15",
student:"gunjita",
semester:2,
subjectId:"s2_5",
grade:"B"
},

{
id:"r16",
student:"gunjita",
semester:2,
subjectId:"s2_6",
grade:"S"
},

{
id:"r17",
student:"gunjita",
semester:2,
subjectId:"s2_7",
grade:"A"
},

{
id:"r18",
student:"gunjita",
semester:2,
subjectId:"s2_8",
grade:"A"
},

{
id:"r19",
student:"gunjita",
semester:2,
subjectId:"s2_9",
grade:"S"
},

{
id:"r20",
student:"gunjita",
semester:2,
subjectId:"s2_10",
grade:"B"
},


/* SEMESTER 3 */

{
id:"r21",
student:"gunjita",
semester:3,
subjectId:"s3_1",
grade:"B+"
},

{
id:"r22",
student:"gunjita",
semester:3,
subjectId:"s3_2",
grade:"F"
},

{
id:"r23",
student:"gunjita",
semester:3,
subjectId:"s3_3",
grade:"C+"
},

{
id:"r24",
student:"gunjita",
semester:3,
subjectId:"s3_4",
grade:"C+"
},

{
id:"r25",
student:"gunjita",
semester:3,
subjectId:"s3_5",
grade:"B+"
},

{
id:"r26",
student:"gunjita",
semester:3,
subjectId:"s3_6",
grade:"F"
},

{
id:"r27",
student:"gunjita",
semester:3,
subjectId:"s3_7",
grade:"D"
},

{
id:"r28",
student:"gunjita",
semester:3,
subjectId:"s3_8",
grade:"A"
},

{
id:"r29",
student:"gunjita",
semester:3,
subjectId:"s3_9",
grade:"F"
},


/* SEMESTER 4 */

{
id:"r30",
student:"gunjita",
semester:4,
subjectId:"s4_1",
grade:"C+"
},

{
id:"r31",
student:"gunjita",
semester:4,
subjectId:"s4_2",
grade:"A+"
},

{
id:"r32",
student:"gunjita",
semester:4,
subjectId:"s4_3",
grade:"D"
},

{
id:"r33",
student:"gunjita",
semester:4,
subjectId:"s4_4",
grade:"A"
},

{
id:"r34",
student:"gunjita",
semester:4,
subjectId:"s4_5",
grade:"C+"
},

{
id:"r35",
student:"gunjita",
semester:4,
subjectId:"s4_6",
grade:"B+"
},

{
id:"r36",
student:"gunjita",
semester:4,
subjectId:"s4_7",
grade:"B+"
},

{
id:"r37",
student:"gunjita",
semester:4,
subjectId:"s4_8",
grade:"C+"
},

{
id:"r38",
student:"gunjita",
semester:4,
subjectId:"s4_9",
grade:"A"
},

{
id:"r39",
student:"gunjita",
semester:4,
subjectId:"s4_10",
grade:"B"
}

];


/* =========================================================
   LOCAL STORAGE
========================================================= */

const DATA_VERSION = "ece_screenshot_data_v1";

let students;
let subjects;
let results;

if(localStorage.getItem("ece_data_version") !== DATA_VERSION){

students = defaultStudents;
subjects = defaultSubjects;
results = defaultResults;

localStorage.setItem(
"ece_students",
JSON.stringify(students)
);

localStorage.setItem(
"ece_subjects",
JSON.stringify(subjects)
);

localStorage.setItem(
"ece_results",
JSON.stringify(results)
);

localStorage.setItem(
"ece_data_version",
DATA_VERSION
);

}else{

students =
JSON.parse(localStorage.getItem("ece_students") || "[]");

subjects =
JSON.parse(localStorage.getItem("ece_subjects") || "[]");

results =
JSON.parse(localStorage.getItem("ece_results") || "[]");

}


let currentUser = null;
let currentRole = null;
let currentPage = "dashboard";


/* =========================================================
   HELPERS
========================================================= */

function saveDatabase(){

localStorage.setItem(
"ece_students",
JSON.stringify(students)
);

localStorage.setItem(
"ece_subjects",
JSON.stringify(subjects)
);

localStorage.setItem(
"ece_results",
JSON.stringify(results)
);

}


function makeId(){

return Date.now().toString(36) +
Math.random().toString(36).slice(2);

}


function escapeHTML(value){

return String(value ?? "")
.replace(/&/g,"&amp;")
.replace(/</g,"&lt;")
.replace(/>/g,"&gt;")
.replace(/"/g,"&quot;")
.replace(/'/g,"&#039;");

}


function findStudent(username){

return students.find(
student => student.username === username
);

}


/* =========================================================
   GRADE POINTS
========================================================= */

const gradePoints = {

"A+":10,
"A":9,
"B+":8,
"B":7,
"C+":6,
"C":5,
"D":4,
"F":0

};


/*
 S = satisfactory/non-GPA grade.
 It is intentionally excluded from GPA calculations.
*/


/* =========================================================
   RESULTS
========================================================= */

function getStudentResults(student,semester=null){

return results.filter(result => {

return result.student === student.username &&
(
semester === null ||
Number(result.semester) === Number(semester)
);

});

}


/*
 Standard credit-weighted SGPA.

 F = 0 points but attempted credits remain
 in the denominator.

 S = excluded from GPA.
*/

function calculateGPA(resultList){

if(!resultList.length){
return "—";
}

let totalPoints = 0;
let totalCredits = 0;

resultList.forEach(result => {

const subject =
subjects.find(
subject => subject.id === result.subjectId
);

if(!subject)return;

if(result.grade === "S")return;

const credits =
Number(subject.credits) || 0;

const point =
gradePoints[result.grade];

if(point === undefined)return;

totalPoints += point * credits;

totalCredits += credits;

});

if(totalCredits === 0){
return "—";
}

return (totalPoints / totalCredits).toFixed(2);

}


/*
 Overall CGPA from all non-S results.
 It is NOT an average of SGPAs.
*/

function calculateCGPA(student){

const resultList =
getStudentResults(student);

if(!resultList.length){
return "—";
}

let totalPoints = 0;
let totalCredits = 0;

resultList.forEach(result => {

const subject =
subjects.find(
subject => subject.id === result.subjectId
);

if(!subject)return;

if(result.grade === "S")return;

const credits =
Number(subject.credits) || 0;

const point =
gradePoints[result.grade];

if(point === undefined)return;

totalPoints += point * credits;
totalCredits += credits;

});

if(totalCredits === 0){
return "—";
}

return (totalPoints / totalCredits).toFixed(2);

}


function getSemesterCredits(student,semester){

const list =
getStudentResults(student,semester);

let credits = 0;

list.forEach(result => {

const subject =
subjects.find(
subject => subject.id === result.subjectId
);

if(subject && result.grade !== "S"){
credits += Number(subject.credits) || 0;
}

});

return credits;

}


function getAllAttemptedCredits(student){

const list =
getStudentResults(student);

let credits = 0;

list.forEach(result => {

const subject =
subjects.find(
subject => subject.id === result.subjectId
);

if(subject && result.grade !== "S"){
credits += Number(subject.credits) || 0;
}

});

return credits;

}


/* =========================================================
   MODALS
========================================================= */

function openModal(id){

document.getElementById(id).classList.add("show");

}


function closeModal(id){

document.getElementById(id).classList.remove("show");

}


/* =========================================================
   MENU
========================================================= */

function toggleMenu(){

document
.getElementById("sidebar")
.classList.toggle("open");

document
.getElementById("overlay")
.classList.toggle("show");

}


function closeMenu(){

document
.getElementById("sidebar")
.classList.remove("open");

document
.getElementById("overlay")
.classList.remove("show");

}


/* =========================================================
   LOGIN
========================================================= */

function login(){

const username =
document.getElementById("loginUser").value.trim();

const password =
document.getElementById("loginPass").value;

const role =
document.getElementById("loginRole").value;

let success = false;


if(
role === "faculty" &&
username === "ankush" &&
password === "2005"
){

currentUser = {
username:"ankush",
name:"Ankush",
role:"faculty"
};

currentRole = "faculty";

success = true;

}


if(role === "student"){

const student =
findStudent(username);

if(
student &&
student.password === password
){

currentUser = student;
currentRole = "student";

success = true;

}

}


if(!success){

document.getElementById("loginMsg")
.textContent =
"Invalid username, password, or role.";

return;

}


document.getElementById("loginMsg")
.textContent = "";

document
.getElementById("loginPage")
.classList.add("hidden");

document
.getElementById("portal")
.classList.remove("hidden");

document.getElementById("headerUser")
.textContent =
`${currentUser.name} • ${currentRole}`;

document.getElementById("sideUser")
.textContent =
`${currentUser.name} (${currentRole})`;


document
.querySelectorAll("[data-faculty]")
.forEach(button => {

button.classList.toggle(
"hidden",
currentRole !== "faculty"
);

});


renderPage("dashboard");

}


function logout(){

currentUser = null;
currentRole = null;

document
.getElementById("portal")
.classList.add("hidden");

document
.getElementById("loginPage")
.classList.remove("hidden");

document.getElementById("loginUser").value = "";
document.getElementById("loginPass").value = "";
document.getElementById("loginRole").value = "";

closeMenu();

}


/* =========================================================
   PAGE ROUTER
========================================================= */

function renderPage(page){

if(
currentRole !== "faculty" &&
["students","subjects","addResult"].includes(page)
){

page = "dashboard";

}

currentPage = page;

document
.querySelectorAll("#nav button[data-page]")
.forEach(button => {

button.classList.toggle(
"active",
button.dataset.page === page
);

});

document.getElementById("main").innerHTML =
pageTemplates[page]();

closeMenu();

if(page === "result"){
updateResultView();
}

if(page === "subjects"){
renderSubjectsTable();
}

if(page === "students"){
renderStudentsTable();
}

if(page === "addResult"){
prepareResultModal();
}

}


/* =========================================================
   PAGE TEMPLATES
========================================================= */

const pageTemplates = {


/* ================= DASHBOARD ================= */

dashboard(){

const student =
currentRole === "student"
? currentUser
: students[0];

if(currentRole === "faculty"){

return `

<div class="container">

<h1 class="page-title">
Faculty Dashboard
</h1>

<p class="page-sub">
Manage ECE students, subjects and results.
</p>

<div class="welcome">

<h2>
Welcome, ${escapeHTML(currentUser.name)}
</h2>

<p>
ECE Student Result Portal — Panjab University, Chandigarh
</p>

</div>

<div class="grid4">

<div class="stat">
<h3>${students.length}</h3>
<p>Total Students</p>
</div>

<div class="stat">
<h3>${subjects.length}</h3>
<p>Total Subjects</p>
</div>

<div class="stat">
<h3>${results.length}</h3>
<p>Total Results</p>
</div>

<div class="stat">
<h3>4</h3>
<p>Semesters Added</p>
</div>

</div>

<div class="card">

<h3>Quick Actions</h3>

<div class="actions">

<button class="primary"
onclick="openStudentModal()">
Add Student
</button>

<button class="secondary"
onclick="openSubjectModal()">
Add Subject
</button>

<button class="secondary"
onclick="openResultModal()">
Add Result
</button>

</div>

</div>

</div>

`;

}


const studentResults =
getStudentResults(student);

const cgpa =
calculateCGPA(student);

const credits =
getAllAttemptedCredits(student);

return `

<div class="container">

<h1 class="page-title">
Student Dashboard
</h1>

<p class="page-sub">
Academic performance overview
</p>

<div class="welcome">

<h2>
Welcome, ${escapeHTML(student.name)}
</h2>

<p>
ECE Student Result Portal — Panjab University, Chandigarh
</p>

</div>

<div class="grid4">

<div class="stat">
<h3>${cgpa}</h3>
<p>CGPA</p>
</div>

<div class="stat">
<h3>${credits}</h3>
<p>Credits Considered</p>
</div>

<div class="stat">
<h3>${studentResults.length}</h3>
<p>Results</p>
</div>

<div class="stat">
<h3>4</h3>
<p>Semesters</p>
</div>

</div>

<div class="card">

<h3>Semester Performance</h3>

<div class="table-wrap">

<table>

<thead>
<tr>
<th>Semester</th>
<th>SGPA</th>
<th>Credits</th>
</tr>
</thead>

<tbody>

${[1,2,3,4].map(sem => {

const sgpa =
calculateGPA(
getStudentResults(student,sem)
);

const cr =
getSemesterCredits(student,sem);

return `

<tr>
<td>Semester ${sem}</td>
<td>
<span class="badge grade">${sgpa}</span>
</td>
<td>${cr}</td>
</tr>

`;

}).join("")}

</tbody>

</table>

</div>

</div>

</div>

`;

},


/* ================= STUDENTS ================= */

students(){

return `

<div class="container">

<h1 class="page-title">
Students
</h1>

<p class="page-sub">
Manage registered ECE students.
</p>

<div class="card">

<div class="actions">

<button class="primary"
onclick="openStudentModal()">
+ Add Student
</button>

</div>

<div class="table-wrap">

<table>

<thead>

<tr>
<th>Name</th>
<th>Roll Number</th>
<th>Username</th>
<th>Email</th>
<th>Phone</th>
<th>Actions</th>
</tr>

</thead>

<tbody id="studentsTableBody"></tbody>

</table>

</div>

</div>

</div>

`;

},


/* ================= SUBJECTS ================= */

subjects(){

return `

<div class="container">

<h1 class="page-title">
Subjects
</h1>

<p class="page-sub">
ECE subjects and credits.
</p>

<div class="card">

<div class="actions">

<button class="primary"
onclick="openSubjectModal()">
+ Add Subject
</button>

</div>

<div class="table-wrap">

<table>

<thead>

<tr>
<th>Semester</th>
<th>Code</th>
<th>Subject</th>
<th>Type</th>
<th>Credits</th>
<th>Actions</th>
</tr>

</thead>

<tbody id="subjectsTableBody"></tbody>

</table>

</div>

</div>

</div>

`;

},


/* ================= ADD RESULT ================= */

addResult(){

return `

<div class="container">

<h1 class="page-title">
Add / Manage Results
</h1>

<p class="page-sub">
Enter or edit student grades.
</p>

<div class="card">

<div class="actions">

<button class="primary"
onclick="openResultModal()">
+ Add Result
</button>

</div>

<div class="table-wrap">

<table>

<thead>

<tr>
<th>Student</th>
<th>Semester</th>
<th>Subject</th>
<th>Grade</th>
<th>Credits</th>
<th>Actions</th>
</tr>

</thead>

<tbody id="resultsTableBody"></tbody>

</table>

</div>

</div>

</div>

`;

},


/* ================= RESULT ================= */

result(){

const student =
currentRole === "student"
? currentUser
: students[0];

return `

<div class="container">

<h1 class="page-title">
Academic Result
</h1>

<p class="page-sub">
Semester-wise result and CGPA.
</p>

<div class="result-head">

<h2>
${escapeHTML(student.name)}
</h2>

<div class="result-meta">

<div class="meta">
<small>Roll Number</small>
<strong>${escapeHTML(student.roll)}</strong>
</div>

<div class="meta">
<small>Programme</small>
<strong>Electronics & Communication Engineering</strong>
</div>

<div class="meta">
<small>University</small>
<strong>Panjab University</strong>
</div>

</div>

</div>

<div class="card no-print">

<div class="result-controls">

<div class="form-group">

<label>Semester</label>

<select id="resultSemester"
onchange="updateResultView()">

<option value="all">
All Semesters
</option>

<option value="1">Semester 1</option>
<option value="2">Semester 2</option>
<option value="3">Semester 3</option>
<option value="4">Semester 4</option>

</select>

</div>

<button class="secondary"
onclick="window.print()">
Print Result
</button>

</div>

</div>

<div id="resultContent"></div>

</div>

`;

},


/* ================= PROFILE ================= */

profile(){

const student =
currentRole === "student"
? currentUser
: students[0];

return `

<div class="container">

<h1 class="page-title">
Profile
</h1>

<p class="page-sub">
Student information.
</p>

<div class="card">

<div class="profile-grid">

<div class="info">
<small>Name</small>
<strong>${escapeHTML(student.name)}</strong>
</div>

<div class="info">
<small>Roll Number</small>
<strong>${escapeHTML(student.roll)}</strong>
</div>

<div class="info">
<small>Username</small>
<strong>${escapeHTML(student.username)}</strong>
</div>

<div class="info">
<small>Father Name</small>
<strong>${escapeHTML(student.father)}</strong>
</div>

<div class="info">
<small>Mother Name</small>
<strong>${escapeHTML(student.mother)}</strong>
</div>

<div class="info">
<small>Email</small>
<strong>${escapeHTML(student.email)}</strong>
</div>

<div class="info">
<small>Phone</small>
<strong>${escapeHTML(student.phone)}</strong>
</div>

<div class="info">
<small>Date of Birth</small>
<strong>${escapeHTML(student.dob)}</strong>
</div>

<div class="info">
<small>Gender</small>
<strong>${escapeHTML(student.gender)}</strong>
</div>

<div class="info full">
<small>Address</small>
<strong>${escapeHTML(student.address)}</strong>
</div>

</div>

</div>

</div>

`;

},


/* ================= SYLLABUS ================= */

syllabus(){

return `

<div class="container">

<h1 class="page-title">
ECE Syllabus
</h1>

<p class="page-sub">
Subjects currently entered in the portal.
</p>

${[1,2,3,4].map(sem => {

const list =
subjects.filter(
subject => Number(subject.semester) === sem
);

return `

<div class="card">

<h3>
Semester ${sem}
</h3>

<div class="table-wrap">

<table>

<thead>

<tr>
<th>Code</th>
<th>Subject</th>
<th>Type</th>
<th>Credits</th>
</tr>

</thead>

<tbody>

${list.map(subject => `

<tr>

<td>${escapeHTML(subject.code)}</td>

<td>${escapeHTML(subject.name)}</td>

<td>

<span class="badge ${
subject.type === "Theory"
? "theory"
: "practical"
}">
${escapeHTML(subject.type)}
</span>

</td>

<td>${subject.credits || "—"}</td>

</tr>

`).join("")}

</tbody>

</table>

</div>

</div>

`;

}).join("")}

</div>

`;

}

};


/* =========================================================
   RESULT VIEW
========================================================= */

function updateResultView(){

const student =
currentRole === "student"
? currentUser
: students[0];

const select =
document.getElementById("resultSemester");

if(!select)return;

const selected =
select.value;

let semesters =
selected === "all"
? [1,2,3,4]
: [Number(selected)];

let html = "";


/* Overall summary */

html += `

<div class="result-summary">

<div class="summary">
<span>CGPA</span>
<strong>${calculateCGPA(student)}</strong>
</div>

<div class="summary">
<span>Total Credits</span>
<strong>${getAllAttemptedCredits(student)}</strong>
</div>

<div class="summary">
<span>Semesters</span>
<strong>4</strong>
</div>

<div class="summary">
<span>Subjects</span>
<strong>${getStudentResults(student).length}</strong>
</div>

</div>

`;


semesters.forEach(semester => {

const list =
getStudentResults(student,semester);

const sgpa =
calculateGPA(list);

const credits =
getSemesterCredits(student,semester);

html += `

<div class="card sem-section">

<div class="sem-head">

<h3>
Semester ${semester}
</h3>

<span class="count">
${list.length} Subjects
</span>

</div>

<div class="table-wrap">

<table>

<thead>

<tr>
<th>Subject Code</th>
<th>Subject</th>
<th>Type</th>
<th>Grade</th>
<th>Earned Credit</th>
</tr>

</thead>

<tbody>

`;

list.forEach(result => {

const subject =
subjects.find(
subject => subject.id === result.subjectId
);

if(!subject)return;

const gradeClass =
result.grade === "F"
? "grade-f"
: "grade";

html += `

<tr>

<td>
${escapeHTML(subject.code)}
</td>

<td>
${escapeHTML(subject.name)}
</td>

<td>

<span class="badge ${
subject.type === "Theory"
? "theory"
: "practical"
}">
${escapeHTML(subject.type)}
</span>

</td>

<td>

<span class="badge ${gradeClass}">
${escapeHTML(result.grade)}
</span>

</td>

<td>
${
result.grade === "S" || Number(subject.credits) === 0
? "—"
: subject.credits
}
</td>

</tr>

`;

});

html += `

</tbody>

</table>

</div>

<div class="result-summary">

<div class="summary">

<span>Semester SGPA</span>

<strong>${sgpa}</strong>

</div>

<div class="summary">

<span>Earned / Considered Credits</span>

<strong>${credits}</strong>

</div>

</div>

</div>

`;

});


document.getElementById("resultContent").innerHTML =
html;

}


/* =========================================================
   STUDENT MANAGEMENT
========================================================= */

function openStudentModal(id=null){

document.getElementById("editStudentId").value =
id || "";

if(id){

const student =
students.find(
student => student.id === id
);

if(!student)return;

document.getElementById("studentModalTitle")
.textContent = "Edit Student";

document.getElementById("sName").value =
student.name;

document.getElementById("sRoll").value =
student.roll;

document.getElementById("sUsername").value =
student.username;

document.getElementById("sPassword").value =
student.password;

document.getElementById("sFather").value =
student.father;

document.getElementById("sMother").value =
student.mother;

document.getElementById("sEmail").value =
student.email;

document.getElementById("sPhone").value =
student.phone;

document.getElementById("sDob").value =
student.dob;

document.getElementById("sGender").value =
student.gender;

document.getElementById("sAddress").value =
student.address;

}else{

document.getElementById("studentModalTitle")
.textContent = "Add Student";

[
"sName",
"sRoll",
"sUsername",
"sPassword",
"sFather",
"sMother",
"sEmail",
"sPhone",
"sDob",
"sAddress"
].forEach(id => {

document.getElementById(id).value = "";

});

document.getElementById("sGender").value =
"Female";

}

openModal("studentModal");

}


function saveStudent(){

const id =
document.getElementById("editStudentId").value;

const data = {

name:document.getElementById("sName").value.trim(),

roll:document.getElementById("sRoll").value.trim(),

username:document.getElementById("sUsername").value.trim(),

password:document.getElementById("sPassword").value,

father:document.getElementById("sFather").value.trim(),

mother:document.getElementById("sMother").value.trim(),

email:document.getElementById("sEmail").value.trim(),

phone:document.getElementById("sPhone").value.trim(),

dob:document.getElementById("sDob").value,

gender:document.getElementById("sGender").value,

address:document.getElementById("sAddress").value.trim()

};


if(!data.name || !data.username || !data.password){

alert("Name, username and password are required.");

return;

}


if(id){

const index =
students.findIndex(
student => student.id === id
);

if(index !== -1){

students[index] = {
...students[index],
...data
};

}

}else{

students.push({
id:makeId(),
...data
});

}


saveDatabase();

closeModal("studentModal");

renderPage("students");

}


function editStudent(id){

openStudentModal(id);

}


function deleteStudent(id){

const student =
students.find(
student => student.id === id
);

if(!student)return;

if(!confirm(
`Delete ${student.name}?`
))return;

students =
students.filter(
student => student.id !== id
);

results =
results.filter(
result => result.student !== student.username
);

saveDatabase();

renderPage("students");

}


function renderStudentsTable(){

const body =
document.getElementById("studentsTableBody");

if(!body)return;

if(!students.length){

body.innerHTML = `

<tr>
<td colspan="6">
No students found.
</td>
</tr>

`;

return;

}

body.innerHTML =
students.map(student => `

<tr>

<td>${escapeHTML(student.name)}</td>

<td>${escapeHTML(student.roll)}</td>

<td>${escapeHTML(student.username)}</td>

<td>${escapeHTML(student.email)}</td>

<td>${escapeHTML(student.phone)}</td>

<td>

<button class="edit"
onclick="editStudent('${student.id}')">
Edit
</button>

<button class="danger"
onclick="deleteStudent('${student.id}')">
Delete
</button>

</td>

</tr>

`).join("");

}


/* =========================================================
   SUBJECT MANAGEMENT
========================================================= */

function openSubjectModal(id=null){

document.getElementById("editSubjectId").value =
id || "";

if(id){

const subject =
subjects.find(
subject => subject.id === id
);

if(!subject)return;

document.getElementById("subjectModalTitle")
.textContent = "Edit Subject";

document.getElementById("subName").value =
subject.name;

document.getElementById("subCode").value =
subject.code;

document.getElementById("subType").value =
subject.type;

document.getElementById("subCredits").value =
subject.credits;

document.getElementById("subSemester").value =
subject.semester;

}else{

document.getElementById("subjectModalTitle")
.textContent = "Add Subject";

document.getElementById("subName").value = "";
document.getElementById("subCode").value = "";
document.getElementById("subType").value = "Theory";
document.getElementById("subCredits").value = "";
document.getElementById("subSemester").value = "1";

}

openModal("subjectModal");

}


function saveSubject(){

const id =
document.getElementById("editSubjectId").value;

const data = {

name:document.getElementById("subName").value.trim(),

code:document.getElementById("subCode").value.trim(),

type:document.getElementById("subType").value,

credits:Number(
document.getElementById("subCredits").value
),

semester:Number(
document.getElementById("subSemester").value
)

};


if(!data.name || !data.code){

alert("Subject name and code are required.");

return;

}


if(id){

const index =
subjects.findIndex(
subject => subject.id === id
);

if(index !== -1){

subjects[index] = {
...subjects[index],
...data
};

}

}else{

subjects.push({
id:makeId(),
...data
});

}


saveDatabase();

closeModal("subjectModal");

renderPage("subjects");

}


function editSubject(id){

openSubjectModal(id);

}


function deleteSubject(id){

const subject =
subjects.find(
subject => subject.id === id
);

if(!subject)return;

if(!confirm(
`Delete ${subject.name}?`
))return;

subjects =
subjects.filter(
subject => subject.id !== id
);

results =
results.filter(
result => result.subjectId !== id
);

saveDatabase();

renderPage("subjects");

}


function renderSubjectsTable(){

const body =
document.getElementById("subjectsTableBody");

if(!body)return;

if(!subjects.length){

body.innerHTML = `

<tr>
<td colspan="6">
No subjects found.
</td>
</tr>

`;

return;

}

const sorted =
[...subjects].sort(
(a,b) =>
Number(a.semester)-Number(b.semester)
);

body.innerHTML =
sorted.map(subject => `

<tr>

<td>
Semester ${subject.semester}
</td>

<td>
${escapeHTML(subject.code)}
</td>

<td>
${escapeHTML(subject.name)}
</td>

<td>

<span class="badge ${
subject.type === "Theory"
? "theory"
: "practical"
}">
${escapeHTML(subject.type)}
</span>

</td>

<td>
${subject.credits || "—"}
</td>

<td>

<button class="edit"
onclick="editSubject('${subject.id}')">
Edit
</button>

<button class="danger"
onclick="deleteSubject('${subject.id}')">
Delete
</button>

</td>

</tr>

`).join("");

}


/* =========================================================
   RESULT MANAGEMENT
========================================================= */

function prepareResultModal(){

const studentSelect =
document.getElementById("rStudent");

if(!studentSelect)return;

studentSelect.innerHTML =
students.map(student => `

<option value="${escapeHTML(student.username)}">
${escapeHTML(student.name)}
</option>

`).join("");

updateResultSubjectOptions();

renderResultsTable();

}


function updateResultSubjectOptions(){

const semester =
Number(
document.getElementById("rSemester").value
);

const subjectSelect =
document.getElementById("rSubject");

if(!subjectSelect)return;

const list =
subjects.filter(
subject =>
Number(subject.semester) === semester
);

subjectSelect.innerHTML =
list.map(subject => `

<option value="${subject.id}">
${escapeHTML(subject.code)} — ${escapeHTML(subject.name)}
</option>

`).join("");

}


function openResultModal(id=null){

document.getElementById("editResultId").value =
id || "";

const studentSelect =
document.getElementById("rStudent");

studentSelect.innerHTML =
students.map(student => `

<option value="${escapeHTML(student.username)}">
${escapeHTML(student.name)}
</option>

`).join("");

if(id){

const result =
results.find(
result => result.id === id
);

if(!result)return;

document.getElementById("resultModalTitle")
.textContent = "Edit Result";

document.getElementById("rStudent").value =
result.student;

document.getElementById("rSemester").value =
result.semester;

updateResultSubjectOptions();

document.getElementById("rSubject").value =
result.subjectId;

document.getElementById("rGrade").value =
result.grade;

}else{

document.getElementById("resultModalTitle")
.textContent = "Add Result";

document.getElementById("rSemester").value =
"1";

updateResultSubjectOptions();

document.getElementById("rGrade").value =
"A+";

}

openModal("resultModal");

}


function saveResult(){

const id =
document.getElementById("editResultId").value;

const student =
document.getElementById("rStudent").value;

const semester =
Number(
document.getElementById("rSemester").value
);

const subjectId =
document.getElementById("rSubject").value;

const grade =
document.getElementById("rGrade").value;


if(!student || !subjectId || !grade){

alert("Please complete all result fields.");

return;

}


const duplicate =
results.find(result =>

result.student === student &&
Number(result.semester) === semester &&
result.subjectId === subjectId &&
result.id !== id

);

if(duplicate){

alert("A result already exists for this subject.");

return;

}


if(id){

const index =
results.findIndex(
result => result.id === id
);

if(index !== -1){

results[index] = {

...results[index],

student,
semester,
subjectId,
grade

};

}

}else{

results.push({

id:makeId(),
student,
semester,
subjectId,
grade

});

}


saveDatabase();

closeModal("resultModal");

renderPage("addResult");

}


function editResult(id){

openResultModal(id);

}


function deleteResult(id){

if(!confirm("Delete this result?"))return;

results =
results.filter(
result => result.id !== id
);

saveDatabase();

renderPage("addResult");

}


function renderResultsTable(){

const body =
document.getElementById("resultsTableBody");

if(!body)return;

const rows =
[...results].sort(
(a,b) =>
Number(a.semester)-Number(b.semester)
);

body.innerHTML =
rows.map(result => {

const student =
students.find(
student => student.username === result.student
);

const subject =
subjects.find(
subject => subject.id === result.subjectId
);

if(!subject)return "";

return `

<tr>

<td>
${escapeHTML(student?.name || result.student)}
</td>

<td>
Semester ${result.semester}
</td>

<td>
${escapeHTML(subject.name)}
</td>

<td>

<span class="badge ${
result.grade === "F"
? "grade-f"
: "grade"
}">
${escapeHTML(result.grade)}
</span>

</td>

<td>
${
result.grade === "S" ||
Number(subject.credits) === 0
? "—"
: subject.credits
}
</td>

<td>

<button class="edit"
onclick="editResult('${result.id}')">
Edit
</button>

<button class="danger"
onclick="deleteResult('${result.id}')">
Delete
</button>

</td>

</tr>

`;

}).join("");

}


/* =========================================================
   EVENTS
========================================================= */

document.getElementById("loginBtn")
.addEventListener("click",login);


document.getElementById("loginPass")
.addEventListener("keydown",event => {

if(event.key === "Enter"){
login();
}

});


document.getElementById("menuBtn")
.addEventListener("click",toggleMenu);


document.getElementById("overlay")
.addEventListener("click",closeMenu);


document.getElementById("logoutBtn")
.addEventListener("click",logout);


document
.querySelectorAll("#nav button[data-page]")
.forEach(button => {

button.addEventListener("click",() => {

renderPage(button.dataset.page);

});

});


document
.querySelectorAll("[data-close]")
.forEach(button => {

button.addEventListener("click",() => {

closeModal(
button.dataset.close
);

});

});


document.getElementById("saveStudent")
.addEventListener(
"click",
saveStudent
);


document.getElementById("saveSubject")
.addEventListener(
"click",
saveSubject
);


document.getElementById("saveResult")
.addEventListener(
"click",
saveResult
);


document.getElementById("rSemester")
.addEventListener(
"change",
updateResultSubjectOptions
);


/* Close modal by clicking outside */

document
.querySelectorAll(".modal")
.forEach(modal => {

modal.addEventListener("click",event => {

if(event.target === modal){
modal.classList.remove("show");
}

});

});


/* Initial state */

document
.getElementById("loginUser")
.focus();

</script>

</body>
</html>
