<script>
    import Nav from "../components/Nav.svelte";
  import { user$ } from "../store";

    const logout = () => {
        user$.set(null);
        localStorage.removeItem("token");
    }
</script>

<div>나의당근</div>
<button>로그아웃</button>
<Nav location="my" />

<style>
    button{
        cursor: pointer;
        border: 1px solid rgba(0, 0, 0, 0.3);
    }
</style>