---
layout: post
title: 지도 API의 대체 텍스트
---

![](https://31.media.tumblr.com/bf72936cc4591ef4a161dc6cdbfc0db1/tumblr_inline_ndhj1mgVeR1qg3tzb.png)

지도 API는 여러 개의 `<img>`를 타일 형태로 늘어놓는 식으로 구현이 된다.

여기서 각 이미지에 대체 텍스트를 다는 것은 바람직하지 않다. 왜냐하면, 각 이미지 타일에 해당 영역에 대한 정보를 각각 대체 텍스트로 제공한다면 그것은 지도 API를 통해 전달하고자 하는 정보와는 무관한 너무 많은 정보가 될 것이기 때문이다. 대신 `alt=""` 혹은 `aria-hidden="true"`와 같이 스크린리더가 무시하도록 `<img>`를 마크업하고 지도 기능을 통해 제공하고자 하는 정보(예를 들어 특정 위치를 찾아가는 방법이라면 그에 대한 정보)를 스크린리더가 접근할 수 있는 형태로 제공해야 한다.

위와 같은 경우라면 구글 지도 API에서 사용한 요소는 모두 스크린리더에서 무시하도록 처리하고 평촌역, 범계역 등에서 건축도시공간연구소를 찾아가는 방법을 서술한 대체 콘텐츠를 스크린리더에서 접근할 수 있는 형태로 제공하는 것이 바람직하겠다.

만약 지도 API가 아이프레임과 같은 형태로 제공된다면 스크린리더 사용자가 아이프레임 내부로 탐색할 필요가 없도록 `title="지도 API 프레임. 약도 설명은 하단 참조"`와 같이 프레임 제목을 제공하는 것이 좋겠다.