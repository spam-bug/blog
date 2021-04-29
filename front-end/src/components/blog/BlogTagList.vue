<template>
  <div class="tags">
    <BlogTagListItem @select-tag="selectTag" :selectedTag="selectedTag" v-for="tag in tags" :key="tag.id" :tag="tag" />
  </div>
</template>

<script>
import { mapState } from 'vuex';
import BlogTagListItem from "./BlogTagListItem";
import AppLabel from "../ui/AppLabel";

export default {
  name: "BlogTagList",
  components: {
    BlogTagListItem,
    AppLabel
  },
  data() {
    return {
      selectedTag: 0
    }
  },
  computed: {
     ...mapState('blog', ['count', 'tags'])
  },
  methods: {
    selectTag(id) {
      return this.selectedTag = id;
    }
  }
}
</script>

<style scoped>
.tags {
  display: flex;
  margin-top: 10px;
}
</style>