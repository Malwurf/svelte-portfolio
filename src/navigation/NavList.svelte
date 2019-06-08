<style lang="scss">
    section {
        align-items: flex-start;
        background-color: var(--feather-blue);
        box-sizing: border-box;
        display: flex;
        height: 100vh;
        justify-content: center;
        overflow-y: scroll;
        // transform: translateX(-330px);
        transition: transform var(--transition-time);
        width: 300px;
        z-index: 2;
    }
    ul {
        list-style: none;
        padding: 30px 0 30px;
        width: 100%;
        box-sizing: border-box;
        margin: 0;

        li {
            align-items: center;
            color: var(--bleachedsilk-white);
            cursor: pointer;
            display: flex;
            font-size: 1.2rem;
            height: 100px;
            justify-content: center;

            & + li,
            &:first-of-type {
                border-top: 2px solid red;
            }

            &:last-of-type {
                border-bottom: 2px solid red;
            }
        }
    }
</style>

<section>
    <ul class="navbar-list">
        <li class="item">link1</li>
        <li class="item">link2</li>
        <li class="item">link3</li>
        <li class="item">link4</li>
        <li class="item">link5</li>
        <li class="item">link6</li>
        <li class="item">link7</li>
        <li class="item">link8</li>
        <li class="item">link9</li>
        <li class="item">link10</li>
        <li class="item">link11</li>
        <li class="item">link12</li>
        <li class="item">link13</li>
    </ul>
</section>