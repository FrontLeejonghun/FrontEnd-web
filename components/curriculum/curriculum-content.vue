<template>
  <div id="curriculum_content">
    <div class="content_wrap">
      <div class="video_area">
        <img
          :src="curriculumContentLink"
          :alt="curriculumContentLink"
          style="width: 100%;height: 100%;"
        />
      </div>
      <div class="video_title_area">
        <p>{{ curriculumContentTitle }}</p>
      </div>
      <div class="video_like_area">
        <div class="icon_content">
          <font-awesome-icon icon="play" />
          <span>{{ curriculumContentView }}</span>
        </div>
        <div class="icon_content">
          <font-awesome-icon icon="heart" />
          <span>{{ curriculumContentLike }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'curriculum-content',
  props: {
    curriculumContentLink: String,
    curriculumContentTitle: String,
    curriculumContentView: String,
    curriculumContentLike: String,
  },
};
</script>

<style lang="scss" scoped>
#curriculum_content {
  margin-top: 30px;
  height: 400px;

  .content_wrap {
    background: #ffffff 0 0 no-repeat padding-box;
    border: 1px solid #dfdfdf;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    box-sizing: border-box;
    width: 100%;

    .video_area {
      width: 100%;
      height: 249px;
      background: #484747;
    }
    .video_title_area {
      padding: 30px 0 20px 20px;
      font-size: 1.15rem;

      p {
        padding-bottom: 30px;
        border-bottom: 1px solid #dfdfdf;
      }
    }

    .video_like_area {
      padding: 0 20px 20px 20px;
      color: #b6b6b6;
      display: flex;
      justify-content: flex-start;

      .icon_content {
        margin-right: 15px;
      }
    }
  }
}
</style>
