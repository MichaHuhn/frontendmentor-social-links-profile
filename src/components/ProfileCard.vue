<template>
  <div class="profile-card max-width-wrapper">
    <img src="@/assets/images/avatar.jpeg" alt="Profile picture of Jessica Randall" class="profile-picture">
    
    <div class="name-and-location">
      <p class="name">Jessica Randall</p>
      <p class="location">London, United Kingdom</p>
    </div>
    
    <q class="bio">Front-end developer and avid reader.</q>
    
    <nav>
      <ul class="social-media-link-list">
        <li>
          <a href="#github" class="social-media-link">GitHub</a>
        </li>
        <li>
          <a href="#frontend-mentor" class="social-media-link">Frontend Mentor</a>
        </li>
        <li>
          <a href="#linkedin" class="social-media-link">LinkedIn</a>
        </li>
        <li>
          <a href="#twitter" class="social-media-link">Twitter</a>
        </li>
        <li>
          <a href="#instagram" class="social-media-link">Instagram</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<style scoped lang="scss">
@import '@/styles/base/typography';
@import '@/styles/base/media-queries';

.profile-card {
  padding: var(--spacing-300);
  text-align: center;
  background-color: var(--color-gray-800);
  border-radius: 12px;
  display: grid;
  gap: var(--spacing-300);
  
  @media #{$tablet-and-up} {
    padding: var(--spacing-500);
  }
  
  .profile-picture {
    width: 5.5rem;
    margin-inline: auto;
    border-radius: 100vmax;
  }
  
  .name-and-location {
    display: grid;
    gap: var(--spacing-50);
    
    .name {
      @extend %typography-text-preset-1;
    }
    
    .location {
      color: var(--color-green);
      @extend %typography-text-preset-2-bold;
    }
  }
  
  .bio {
    @extend %typography-text-preset-2;
  }
  
  .social-media-link-list {
    padding: 0;
    list-style: none;
    display: grid;
    gap: var(--spacing-200);
    
    .social-media-link {
      padding: var(--spacing-150);
      color: inherit;
      background-color: var(--color-gray-700);
      text-decoration: none;
      @extend %typography-text-preset-2-bold;
      border-radius: 8px;
      display: block;
      
      &:hover, &:focus-visible {
        color: var(--color-gray-700);
        background-color: var(--color-green);
      }
    }
  }
}

.max-width-wrapper {
  --content-max-width: 24rem;
  --spacing-inline: var(--spacing-300);
  
  width: min(var(--content-max-width), 100% - (var(--spacing-inline) * 2));
  margin-inline: auto;
}
</style>
