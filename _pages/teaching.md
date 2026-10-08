---
title: "Roy Lab - Teaching"
layout: piclay
excerpt: "Teaching"
permalink: /teaching/
---

# Teaching Activities
Jump to: [Teaching Philosophy](#philosophy) [Courses](#courses) [Evaluation](#iotaevaluation)

# Philosophy
My teaching philosophy is grounded in a desire to provide students with a solid foundation in chemistry and the confidence to investigate scientific questions. As a teacher, I strive to **engage, challenge, and inspire** my students' growth. In chemistry, I want students to understand the physical meaning *behind an equation and connect it to the behavior of molecules and materials*. My teaching helps students progress from following procedures to reasoning independently through a combination of conceptual explanations, problem-solving, and constructive feedback.

# Courses
- Undergraduate:
  + Fall Semester
    * Chemistry I and II (CHEM 1411 and CHEM 1412)
    * Physical Chemistry I (CHEM 3421) with Lab
    * Senior Investigations (CHEM 4370)
    * Undergraduate Research (CHEM 4397)
  + Spring Semester
    * Chemistry I and II (CHEM 1411 and CHEM 1412)
    * Physical Chemistry II (CHEM 3422) with Lab
    * Senior Investigations (CHEM 4370)
    * Undergraduate Research (CHEM 4397)
- Graduate:
  + Fall Only  
    * Quantum Mechanics (CHEM 6350)

# IOTAEvaluation 

<!--
| Semester | Course Name | Enrolled Students | Response (%) | Avg. Score (4.0) | Department Avg. |
|:---|:---:|:---:|:---:|---:|---:|
| **Fall 2023** |CHEM 1411 | 68 | 63% | 2.49 | 3.35 |
| **Spring 2026** |CHEM 1411 | 50 | 70% | 3.00 | 3.42 |
| **Spring 2026** |CHEM 1412 | 50 | 70% | 3.00 | 3.42 |
-->


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>IOTA Evaluation Table</title>
  <style>
    table {
      width: 100%;
      border-collapse: collapse;
      font-family: Arial, sans-serif;
    }
    th, td {
      border: 1px solid #ccc;
      padding: 10px;
      text-align: center;
    }
    th {
      background-color: #f2f2f2;
    }
  </style>
</head>
<body>

<table id="iotaTable">
  <thead>
    <tr>
      <th>Semester</th>
      <th>Course Name</th>
      <th>Enrolled Students</th>
      <th>Response (%)</th>
      <th>Avg. Score (4.0)</th>
      <th>Department Avg.</th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

<script>
const data = [
  {
    semester: "Fall 2023",
    course: "CHEM 1411",
    enrolled: 68,
    response: 63,
    score: 2.49,
    department: 3.35
  },
  {
    semester: "Spring 2026",
    course: "CHEM 1411",
    enrolled: 50,
    response: 70,
    score: 3.00,
    department: 3.42
  },
  {
    semester: "Spring 2026",
    course: "CHEM 1412",
    enrolled: 50,
    response: 70,
    score: 3.00,
    department: 3.42
  }
];

function renderTable(data) {
  const tbody = document.querySelector(
    "#iotaTable tbody"
  );
  tbody.innerHTML = "";

  data.forEach((item, index) => {
    const tr = document.createElement("tr");

    // Automatically merge consecutive semesters
    if (index === 0 ||
        item.semester !== data[index - 1].semester) {

      let span = 1;

      while (
        index + span < data.length &&
        data[index + span].semester === item.semester
      ) {
        span++;
      }

      const td = document.createElement("td");
      td.rowSpan = span;
      const strong = document.createElement("strong");
      strong.textContent = item.semester;
      td.appendChild(strong);
      tr.appendChild(td);
    }

    const values = [
      item.course,
      item.enrolled,
      item.response + "%",
      item.score.toFixed(2),
      item.department.toFixed(2)
    ];

    values.forEach(value => {
      const td = document.createElement("td");
      td.textContent = value;
      tr.appendChild(td);
    });

    tbody.appendChild(tr);
  });
}

renderTable(data);
</script>

</body>
</html>




# Teaching Effectiveness
**Grade Distributions:** [Visit WTAMU](https://analytics.wtamu.edu/gradeDist/index.html)
