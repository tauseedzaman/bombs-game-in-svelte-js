<script>
    export let user;
    console.log(user);
    let blog = `<table style="background:cyan; padding:10px;border:1px solid black">
        <thead style="border:1px solid green;background:lightgreen">
    <th>Name</th>
    <th>Age</th>
    <th>Address</th>
    <th>Job</th>
</thead>`;

    user.forEach((usr) => {
        blog += `<tr>
    <td>${usr.name}</td>
    <td>${usr.age}</td>
    <td>${usr.address}</td>
    <td>${usr.job}</td>
</tr>`;
    });
    blog += "</table>";
</script>

<h1 style="text-align:left">Users Details</h1>
<h3 style="text-align:left; ">
    {@html blog}
</h3>
