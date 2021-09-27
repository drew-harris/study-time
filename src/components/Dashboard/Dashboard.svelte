<script>
  import Card from "../Card/Card.svelte";
import SessionTimer from "../SessionTimer.svelte";
  
</script>
<div class="dashboard">
  <Card>
    <SessionTimer />
  </Card>


</div>

<style>
  .dashboard {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    padding: 15px;
  }
</style>
