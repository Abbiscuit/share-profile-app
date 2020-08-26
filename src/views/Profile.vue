<template>
  <div class="profile">
    <div class="card">
      <div class="cover">
        <img
          class="avatar"
          src="https://images.unsplash.com/photo-1596663095213-b660314b4da8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60"
          alt
        />
      </div>
      <div class="content">
        <h2 class="name">Jane Doe</h2>
        <p class="role">UI Developer</p>

        <div class="intro">
          <p>Jane is a designer and developer who loves JavaScript and CSS.</p>
        </div>

        <div class="socials">
          <router-link to="/" class="social twitter">
            <img src="@/assets/Twitter_Logo_Blue.png" alt />
          </router-link>
          <router-link to="/" class="social instagram">
            <img src="@/assets/instagram.png" alt />
          </router-link>
        </div>
      </div>
    </div>

    <div class="section">
      <h3 class="section-title">Courses from the author</h3>
      <div class="images">
        <div class="image">
          <img
            src="https://images.unsplash.com/photo-1595996285589-62fc8a1eade4?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60"
            alt
          />
        </div>
        <div class="image">
          <img
            src="https://images.unsplash.com/photo-1525909002-1b05e0c869d8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60"
            alt
          />
        </div>
        <div class="image">
          <img
            src="https://images.unsplash.com/photo-1546877625-cb8c71916608?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60"
            alt
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Profile",
};
</script>

<style lang="scss" scoped>
.profile {
  padding: 16px;
  border-top-left-radius: 8px;
  border-top-right-radius: 8px;
  height: 100%h;
  background-image: url("https://images.unsplash.com/photo-1579546928686-286c9fbde1ec?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=800&q=60");
  background-position: center;
  background-size: cover;

  .section {
    background-color: #fff;
    min-height: 100px;
    border-radius: 8px;
    padding: 24px 48px;

    max-width: 640px;
    margin: 0 auto;

    .section-title {
      font-size: 20px;
      font-weight: 400;
      color: #2c3e50;
      margin: 0 0 10px;
    }
    .images {
      display: flex;
      justify-content: space-around;

      .image {
        width: 72px;
        height: 72px;

        img {
          width: 72px;
          height: 72px;
          border-radius: 8px;
          box-shadow: 0 8px 20px rgba(0, 0, 0, 0.25);
          object-fit: cover;
        }
      }
    }
  }
}

.card {
  padding: 24px 48px;
  background-color: #fff;
  border-radius: 8px;
  box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.5);
  max-width: 640px;
  margin: 0 auto 24px;

  .cover {
    .avatar {
      width: 100%;
      width: 150px;
      height: 150px;
      object-fit: cover;
      border-radius: 100%;
    }
  }

  .content {
    .intro {
      padding: 16px 0;

      border-top: 1px solid rgba(0, 0, 0, 0.15);

      p {
        margin: 0;
      }
    }

    .socials {
      padding: 16px 0;
      border-top: 1px solid rgba(0, 0, 0, 0.15);
      display: flex;
      align-items: center;

      .social {
        width: 72px;
        height: 72px;

        img {
          width: 100%;
        }
      }

      display: flex;
      justify-content: space-around;
    }
  }
}
</style>