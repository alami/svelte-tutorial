<ul>
    {#each profiles as profile}
        <li>{profile.name}: {profile.role}</li>
    {/each}
</ul>

<script>
    const profiles = [
        {name: 'Wes Bos', role: 'React extraordinaire'},
        {name: 'Chris Coyier', role: 'Father of CodePen'},
        {name: 'Cassidy Williams', role: 'Letting you know it\'s pi time'}
    ];
</script>