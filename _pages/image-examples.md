---
layout: single
title: "Image Scaling Examples"
permalink: /image-examples/
author_profile: true
---

## 이미지 크기 조정 예제

### 1. HTML 태그를 사용한 크기 조정

원본 이미지:
<img src="/images/IMG_8269.jpg" alt="Original Image">

너비 300px로 조정:
<img src="/images/IMG_8269.jpg" alt="Image resized to 300px width" width="300px">

너비 50%로 조정:
<img src="/images/IMG_8269.jpg" alt="Image resized to 50% width" width="50%">

너비와 높이 모두 조정:
<img src="/images/IMG_8269.jpg" alt="Image resized to 400x300" width="400px" height="300px">

### 2. Markdown에서 HTML 태그 사용

Markdown 문서 안에서도 HTML 태그를 사용할 수 있습니다:

```html
![대체 텍스트](/images/IMG_8269.jpg)

<img src="/images/IMG_8269.jpg" alt="Resized Image" width="300px">
```

### 3. CSS 스타일을 사용한 크기 조정

스타일 속성을 사용하여 보다 세밀한 조정이 가능합니다:

<img src="/images/IMG_8269.jpg" alt="Image with CSS styling" style="width: 400px; max-width: 100%; height: auto; border: 2px solid #ddd; border-radius: 8px; padding: 5px;">

### 4. 반응형 이미지 (권장)

화면 크기에 따라 자동으로 크기가 조정되는 반응형 이미지 설정:

<img src="/images/IMG_8269.jpg" alt="Responsive image" style="max-width: 100%; height: auto;">

### 5. 맞춤형 CSS 클래스 사용 예

웹사이트 전체에서 일관된 이미지 스타일을 적용하려면 CSS 클래스를 정의하는 것이 좋습니다. 예를 들어, `custom-styles.css`에 다음과 같은 클래스를 정의할 수 있습니다:

```css
.img-small {
  width: 200px;
  height: auto;
}

.img-medium {
  width: 400px;
  height: auto;
}

.img-large {
  width: 800px;
  height: auto;
}

.img-thumbnail {
  width: 150px;
  height: 150px;
  object-fit: cover;
  border-radius: 5px;
}
```

그런 다음 다음과 같이 사용할 수 있습니다:

```html
<img src="/images/IMG_8269.jpg" alt="Small image" class="img-small">
<img src="/images/IMG_8269.jpg" alt="Medium image" class="img-medium">
<img src="/images/IMG_8269.jpg" alt="Thumbnail" class="img-thumbnail">
``` 