<script lang="ts">
    import { Link } from "svelte-routing";
</script>

<header class="bg-orange-400">
    <div class="container mx-auto flex justify-between h-[60px] items-center">
        <h1>
            <Link to="/">漢字クイズアプリ</Link>
        </h1>
        <nav>
            <ul>
                <li>
                    <Link to="/help">遊び方</Link>
                </li>
            </ul>
        </nav>
    </div>
</header>