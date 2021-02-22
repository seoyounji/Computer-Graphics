image를 sharpening 하게 만들어 보기 / noise image를 만든 뒤 sliding window를 이용해 median filter로 denoising 해보기
=========================================================================================

### unsharp 라고 써놔서 이미지를 블러 처리하는 것처럼 생각할 수도 있겠지만 사실 unsharp mask filter는 이미지를 날카롭게 만드는 방법 중 하나이다. 초기 이미지가 unsharp한, 날카롭지 않은 이미지를 사용하는 것이기 때문에 붙여진 이름이다.

***

#### original image   

<img src="/lena.png" width="200px" height="300px" title="original" alt="original image"></img><br/>
    
***

> frequency domain filtering sharpening

    주파수 값을 이용한 필터링 방법.   
    이미지를 주파수 영역으로 변환한 뒤 필터링한 후 다시 주파수 영역을 이미지로 변환

#### after image
<img src="/frequency_unsharpening.jpg" width="200px" height="300px" title="frequency unsharpening" alt="frequency unsharpening image"></img><br/>

***

* spatial domain filtering sharpening

    이미지의 픽셀 값을 직접 이용한 필터링 방법.     주로 마스크(커널이나 윈도우라고 하기도 함) 연산을 이용해 대상 좌표의 픽셀과 주변 픽셀 값을 바꿈

#### after image
<img src="/spatial_unsharpening.jpg" width="200px" height="300px" title="spatial unsharpening" alt="spatial unsharpening image"></img><br/>

***

* salt and pepper noise image

    denoising을 하기 위해 일부러 noise 있는 이미지를 만들어 봄. 가장 기본적인 salt and pepper 방식으로 진행함.     이 방식의 경우 이미지에 소금이랑 후추를 친 것 같다고 해서 salt and pepper 방식이라고 불린다.

#### after image
<img src="/noise_image.jpg" width="200px" height="300px" title="noise image" alt="noise image"></img><br/>
