
# Technical Detail

<p align="center">
  <img src="./KakaoTalk_20251128_170553359.png" alt="ㅋㅋㅋ" width="900">
  </p>
<p align="center">
<img width="114" height="103" alt="ㅋㅋㅋ" src="https://github.com/user-attachments/assets/9e73feee-f64a-4120-b448-6e20676b34f4" />
</p>


> unreal material, scratch pad, hlsl 등을 이용하여 아트 퀄리티 개선, 최적화

## Tech 1
서로 다른 이미터에서 스폰되는 요소들이 각각 같은 random position 값을 가지도록 하는 scratch pad 제작
 - 공중에서 떨어지는 수십개의 화살을 하나의 나이아가라 시스템 내에서 구현하기 위함
 - 삼각함수를 이용하여 파티클 고유의 id마다 떨어질 위치를 직접 설정, 파티클의 id는 순서를 섞어주어 떨어지는 순서에도 랜덤성을 부여함
 - 여러개의 나이아가라 시스템을 스폰하지 않아도 되어 최적화에 도움
### Tech Demo
https://github.com/user-attachments/assets/32a904c9-f16e-44bc-bd3a-07c1bf6f305d

 > 활용된 결과
> 
https://github.com/user-attachments/assets/6275d816-2352-4b21-ab88-a251edd1d27e

## Tech 2
나이아가라 시스템 내에서 회오리 형태를 유지하며 x축 방향으로 이동하는 파티클을 구현하는 scratch pad 제작
 - 보스 스킬 제작 중 나이아가라 시스템 내에서 회오리가 이동하는것까지 구현해달라는 요청
 - 삼각함수를 이용하여 회오리 모형으로 파티클을 배치하고 랜덤값을 추가해서 vortex force가 적용된 이미터처럼 보이도록 제작
### Tech Demo
https://github.com/user-attachments/assets/6275d816-2352-4b21-ab88-a251edd1d27e

 > 활용된 결과

https://github.com/user-attachments/assets/6275d816-2352-4b21-ab88-a251edd1d27e

## Tech 3
점액질 느낌을 낼 수 있는 액체 머리티얼 제작
 - 보스가 소환하는 알이 깨질때 이펙트를 위해 신규 마스터 머티리얼 제작
 - 액체의 specular 강도나 형태를 아티스트가 직접 제어할 수 있도록 머티리얼의 specular 옵션을 켜지 않고 blinn reflection 방식을 머티리얼 내에서 구현
 - 액체를 표현하기 위한 opacity 텍스쳐 제작
 - 빛의 각도에 따라 결과물이 심하게 달라지는 것을 방지하기 위해 camera vector를 회전시키는 hlsl코드 작성
### Tech Demo
https://github.com/user-attachments/assets/6275d816-2352-4b21-ab88-a251edd1d27e

 > 활용된 결과

https://github.com/user-attachments/assets/6275d816-2352-4b21-ab88-a251edd1d27e

## Tech 4
크리스탈 계단을 표현하기 위한 머티리얼 제작
 - 계단에 흐르는 기운과 크리스탈 같은 반짝임을 표현하기 위해 신규 머티리얼 제작
 - World Position을 활용하여 휘어져있는 계단에 딱 맞게 흐르는 기운을 표현
### Tech Demo
https://github.com/user-attachments/assets/b2addd5e-6da3-465b-ae78-9925d5d2d278

 > 활용된 결과

https://github.com/user-attachments/assets/3048274a-f922-46f2-9f8c-346f9b795d48

## Tech 5
보스의 스킬 범위를 표시하는 장판 머티리얼 비쥬얼 개선
 - 장판이 커도 텍스쳐의 해상도를 유지하기 위해 직선 형태의 텍스쳐를 장판 범위에 두르는 형식으로 구현

 > 활용된 결과

https://github.com/user-attachments/assets/3048274a-f922-46f2-9f8c-346f9b795d48

## Tech 6
단일 머티리얼 내에서 두개의 월드포지션 사이에 부채꼴 형태의 마스크를 그리는 머티리얼 R&D(test)
 - 벡터연산과 삼각함수를 이용하여 특정 포지션을 향하는 부채꼴을 그릴 수 있음
### Tech Demo
https://github.com/user-attachments/assets/579ae8ac-2f83-442c-a4ad-5ad541b241c9



### unreal

> aasd


<p align="center">
  <img width="114" height="103" alt="ㅋㅋㅋ" src="https://github.com/user-attachments/assets/9e73feee-f64a-4120-b448-6e20676b34f4" />
</p>
<p align="center">
  <img width="114" height="103" alt="ㅋㅋㅋ" src="https://github.com/user-attachments/assets/9e73feee-f64a-4120-b448-6e20676b34f4" />
</p>





