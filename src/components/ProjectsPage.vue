<template>
  <div class="prj-body">
    <div>
    </div>
    <div>
    </div>
  </div>
</template>

<script>
import { Octokit } from "octokit";

export default {
  name: 'ProjectsPage',
  setup() {
    // Test Comment for push
    const octokit = new Octokit({
    })
  }
}
</script>

<style>
.prj-body {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}
</style>
