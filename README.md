
# Technical Detail
> scratch pad, hlsl, material, Blueprint 활용하여 아트 퀄리티 개선, 최적화, 편의성 개선





R2 Origin Project Reel
https://youtu.be/pVQydDmTgOg

Tech2, Tech3의 보스 스킬은 본인 작업물이 아닙니다.(필요한 모듈만 제작)

# blueprint script

## Tech 1
네이밍 기반 몬스터 자동 호출&배치 블루프린트 제작
 - 몬스터 번호만 입력한 후 자동으로 몬스터 배치, 원하는 애니메이션 재생
 - 수백개의 몬스터 애셋을 빠르게 확인 가능

# scratch pad

## Tech 2
서로 다른 이미터에서 스폰되는 요소들이 각각 같은 random position 값을 가지도록 하는 scratch pad 제작
 - 공중에서 떨어지는 수십개의 화살을 하나의 나이아가라 시스템 내에서 구현하기 위함
 - Particle id 기반 Hash random값을 추출하고 삼각함수를 이용하여 떨어질 위치를 설정
 - 각 이미터에서 n번째로 생성되는 파티클들은 동일한 위치값을 가짐
### Tech Demo
https://github.com/user-attachments/assets/b9ecb9aa-f86f-4b28-a2bc-e5717f3cb85d

> 활용된 결과

https://github.com/user-attachments/assets/1f681ab3-53fa-4b4d-8355-b8d88f145ef9

 > 활용된 결과(본인 작업X)

https://github.com/user-attachments/assets/06a7348a-96da-410f-bdbe-aaf688165244

## Tech 3
나이아가라 시스템 내에서 회오리 형태를 유지하며 특정 방향으로 이동하는 파티클을 구현하는 scratch pad 제작
 - 보스 스킬 제작 중 나이아가라 시스템 내에서 회오리가 이동하는것까지 구현해달라는 요청
 - 삼각함수를 이용하여 회오리 모형으로 파티클을 배치하고 랜덤값을 추가해서 vortex force가 적용된 이미터처럼 보이도록 제작
### Tech Demo
https://github.com/user-attachments/assets/32a904c9-f16e-44bc-bd3a-07c1bf6f305d

 > 활용된 결과(본인 작업X)

https://github.com/user-attachments/assets/aac4d79c-a496-47e0-b772-c3a71f42497a

# material

## Tech 4
점액질 느낌을 낼 수 있는 액체 머리티얼 제작
 - 보스가 소환하는 알이 깨질때 이펙트를 위해 신규 마스터 머티리얼 제작
 - 액체의 specular 강도나 형태를 아티스트가 직접 제어할 수 있도록 머티리얼의 specular 옵션을 켜지 않고 blinn reflection 방식을 머티리얼 내에서 구현
 - 액체를 표현하기 위한 opacity 텍스쳐 제작
 - 빛의 각도에 따라 결과물이 심하게 달라지는 것을 방지하기 위해 camera vector를 회전시키는 hlsl코드 작성

 > 활용된 결과

https://github.com/user-attachments/assets/a7e51a16-16f9-478d-8dc3-677822fddb2b

## Tech 5
크리스탈 계단을 표현하기 위한 머티리얼 제작
 - 계단에 흐르는 기운과 크리스탈 같은 반짝임을 표현하기 위해 신규 머티리얼 제작
 - World Position을 활용하여 휘어져있는 계단에 딱 맞게 흐르는 기운을 표현

 > 활용된 결과

https://github.com/user-attachments/assets/3048274a-f922-46f2-9f8c-346f9b795d48

## Tech 6
보스의 스킬 범위를 표시하는 장판 머티리얼 비쥬얼 개선
 - 장판이 커도 텍스쳐의 해상도를 유지하기 위해 직선 형태의 텍스쳐를 장판 범위에 두르는 형식으로 구현

 > 활용된 결과

https://github.com/user-attachments/assets/3551f76b-fdf7-40c2-a8cc-eb8ddc48124c

## Tech 7
데칼 액터의 transform 속성을 worldposition에 투영시켜 UV를 생성
 - translucent 오브젝트 위에도 데칼이 찍히는 것처럼 구현 가능

### Tech Demo
https://github.com/user-attachments/assets/d7171439-594f-4d7c-93f4-25664778b98e

https://github.com/user-attachments/assets/16637e98-1a83-4756-8467-6467a56e3eeb

## Tech 8
단일 머티리얼 내에서 두개의 월드포지션 사이에 부채꼴 형태의 마스크를 그리는 머티리얼 R&D(test)
 - 벡터연산과 삼각함수를 이용하여 특정 포지션을 향하는 부채꼴을 그릴 수 있음
### Tech Demo
https://github.com/user-attachments/assets/579ae8ac-2f83-442c-a4ad-5ad541b241c9

# optimization

## Tech 9
이미터 최적화
 - 부채꼴 형태로 배치해야 하는 파티클들을 최적화와 수정에 용이하도록 하나의 이미터로 제작
### Tech Demo
https://github.com/user-attachments/assets/d7968bee-0f20-4757-9f23-2b98e5c12b6f

 > 활용된 결과

https://github.com/user-attachments/assets/3368fd7d-0018-4c8d-9b3c-544f02a20e46






