# 플러그인 사용 방법
 
 모든 플러그인 최신 가이드는 https://github.com/lilly1987/BepInPluginSample 를 참조  
 
 ## 1. BepInEx 설치 필요 

https://github.com/BepInEx/BepInEx/releases  
exe있는게임폴더에 압축 해제 (비트 버전은 알아서 맞출것. 최신은 어지간하면 64로 나옴)

아래 스샷처럼 넣기  
![2022-10-10 17 15 20](https://user-images.githubusercontent.com/20321215/194823924-fc419cab-27b1-4d11-a5e3-8e55c4b472e2.png)


## 2. 해당 게임의 플러그인 다운

![2022-10-10 17 22 27](https://user-images.githubusercontent.com/20321215/194825099-fff645e8-5fcb-4810-8408-dc5f3fdc100b.png)

![2022-10-10 17 23 00](https://user-images.githubusercontent.com/20321215/194825119-89f109fd-234a-4f91-97f6-fce69ca27abd.png)


## 3. 플러그인 dll 넣는 위치

exe있는게임폴더\BepInEx\plugins

아래 스샷처럼 넣기  
![2022-10-10 17 15 53](https://user-images.githubusercontent.com/20321215/194823986-a4ec5024-bd38-4ca1-81a8-335041293b4e.png)


# 비주얼 스튜디오로 플러그인 직접 수정할경우

## 비주얼 스튜디오 패키지 관리자 설정

"도구 - 패키지 관리자 - 설정 - 패키지 소스"에서 아래 링크 추가  
https://nuget.bepinex.dev/v3/index.json  


## dll 참조 추가

이게임에서 사용되는 mscorlib.dll버전(2.0)이 낮아서 높은 버전의 mscorlib.dll(4.0)를 'ATOMINE\Atomine_Data\Managed'에 덮어씌워야함.

게임명_Data\Managed\Assembly-CSharp.dll  
게임명_Data\Managed\UnityEngine.dll  

- 버전에 따라 아래 dll 도 추가해야 컴파일 가능  
  이건 직접 dnspy같은걸로 "게임명_Data\Managed"안의 dll 에서 어딧는지 찿아보는 수밖에

UnityEngine.CoreModule.dll  
UnityEngine.IMGUIModule.dll  
