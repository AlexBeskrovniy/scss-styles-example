<style lang="scss">
  $textColor: #A79EA4;

  .main {
    height: 100vh;
    color: $textColor;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .card {
    $cardColor: #231E39;
    $outlineColor: #03BFCB;

    height: auto;
    width: min(350px, 90vw);
    background: $cardColor;
    border-radius: 10px;
    box-shadow: 0px 5px 10px 2px #000;
    overflow: hidden;

    &-body {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1.5rem;
      padding: 2rem 3rem;
      position: relative;

      &-avatar {
        $size: 8rem;

        width: $size;
        height: $size;
        overflow: hidden;
        border-radius: 50%;
        border: 2px solid $outlineColor;
        
        & img {
          width: 100%;
          height: 100%;
          object-fit: cover;
        }
      }

      &-info {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        gap: .8rem;

        .name {
          font-size: 2rem;
        }

        .city {
          text-transform: uppercase;
          letter-spacing: .3rem;
        }

        .role {
          font-size: 1.3rem;
        }
      }

      &-contacts {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: .5rem;

        &-button {
          padding: .5rem 1.5rem;
          color: $cardColor;
          background: $outlineColor;
          border: 2px solid $outlineColor;
          border-radius: 3px;

          &:hover {
            opacity: .64;
          }
        }

        .outline-button {
          background: transparent;
          color: $outlineColor;
        }
      }

      &-badge {
        position: absolute;
        left: 1.5rem;
        top: 1.5rem;
        padding: .3rem;
        background: #FEBB0B;
        color: #000;
        text-transform: uppercase;
        border-radius: 3px;
        line-height: .5;
        font-weight: bold;
      }
    }

    &-footer {
      background: #1F1A36;
      padding: 1.5rem 1rem;
      border-top: 2px solid $outlineColor;

      &-title {
        text-transform: uppercase;
        margin-bottom: .5rem;
      }

      &-content {
        display: flex;
        flex-wrap: wrap;
        gap: .5rem;

        &-item {
          border: 1px solid $textColor;
          padding: .3rem;
        }
      }
    }
  }

</style>

<main class="main">

  <div class="card">
    <div class="card-body">
      <div class="card-body-avatar">
        <img src="/carbon.jpg" alt="helmet">
      </div>
      <div class="card-body-info">
        <h3 class="name">John Doe</h3>
        <h5 class="city">Tashkent</h5>
        <p class="role">Front-end developer and UI/UX designer</p>
      </div>
      <div class="card-body-contacts">
        <a href="mailto:" class="card-body-contacts-button">Message</a>
        <a href="https://facebook.com" class="card-body-contacts-button outline-button">Following</a>
      </div>
      <div class="card-body-badge">pro</div>
    </div>
    <div class="card-footer">
      <p class="card-footer-title">Skills</p>
      <div class="card-footer-content">
        <span class="card-footer-content-item">UI/UX</span>
        <span class="card-footer-content-item">Front-End</span>
        <span class="card-footer-content-item">HTML</span>
        <span class="card-footer-content-item">CSS</span>
        <span class="card-footer-content-item">SCSS</span>
        <span class="card-footer-content-item">JavaScript</span>
        <span class="card-footer-content-item">React</span>
        <span class="card-footer-content-item">Node</span>
      </div>
    </div>
  </div>

</main>
