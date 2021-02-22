image를 sharpening 하게 만들어 보기 / noise image를 만든 뒤 sliding window를 이용해 median filter로 denoising 해보기
=========================================================================================
   
### unsharp 라고 써놔서 헷갈릴 수도 있겠지만 사실 unsharp mask filter는 이미지를 날카롭게 만드는 방법 중 하나이다. 초기 이미지가 unsharp한, 날카롭지 않은 이미지를 사용하는 것이기 때문에 붙여진 이름이다.
    
    
> original image   

<img src="/lena.png" width="200px" height="300px" title="original" alt="original image"></img><br/>
    
    
> frequency domain filtering sharpening

    주파수 값을 이용한 필터링 방법. 이미지를 주파수 영역으로 변환한 뒤 필터링한 후 다시 주파수 영역을 이미지로 변환
  
#### after image
<img src="/frequency_unsharpening.jpg" width="200px" height="300px" title="frequency unsharpening" alt="frequency unsharpening image"></img><br/>

