



# Stable Diffusion  기반 사진 I2I서비스 MVP 개발

------



## 프로젝트 개요

- 이어드림스쿨 3기 기업연계 프로젝트
- Stable Diffusion을 통해 User의 Image를 학습한 후, 개인화와 더불어 생성 Image의 포즈와 색감을 더한 AI 스튜디오 프로필 생성 팀 프로젝트

## 팀원

- DE
  - 남궁맑음 : DE 팀장, 전처리, 온프레미스 서버 환경 구축, Flask API 구축
  - 정양섭 : Github관리, Gradio를 사용한 Web page 구축, Flask API를 활용한 Data Serving, 
  - 김아진 : 데이터 수집 및 중간발표
- DS 
  - 박사무엘 : DS 팀장, base model code 구축, Stable Diffusion을 사용한 Model Module code구축, Image Concept에 맞는 Prompt Reasearch
  - 강동훈 : LoRA Reasearch, LoRA training
  - 지주영 : Base Prompt 구축 및 Reasearch

## 프로젝트 기간

- 2023.11. - 2023.12 (6주)

## 기술스텍

- Stable Diffusion Web UI A1111
- Flask
- Gradio
- Github

## 프로젝트 진행 단계

user 의 img를 받아 Image Generation 과정은 아래와 같다.

- Gradio를 Flask API를 이용해 Stdable Diffusion Web Ui 와 연동하여 프로세스한다.
- Graido를 통해 web의 Front로써 간단히 기능하게 된다.
- Stable Diffusion의 자체적인 API를 이용, 학습 및 추론을 수행한다.

1. 유저의 이미지 10장을 통해 Easy-Photo의 train 후 user의 LoRA 생성한다.
2. 생성된 LoRA를 프롬프트에 추가한다
3. Generation Inference start
4. T2I로 이미지의 뼈대와 포즈 및 유저의 얼굴 생성한다.
5. user의 LoRA 와 손 등을 후보정 수행한다.
6. T2I의 output을 I2I로 처리하여 이미지의 tone-filter 를 denoise 미화작업을 수행한다.
7. user의 LoRA 와 손 등을 다시 한번 더 후보정 수행한다. (이미지가 denoise를 통해 변한 부분을 변동없게 하기 위해서)
8. I2I를 다시 한번더 진행, 하지만 이번에는 Denoise를 낮게 주고, 해상도를 만을 높이면서 detail up을 목적으로 upscale 진행한다.
9. 최종적인 이미지를 생성후, Graido로 전송한다.
10. Gradio를 통해 user에게 출력하여 보여준다.

## 프로젝트 세부 과정

... 정리중

## 프로젝트 회고

... 정리중



- 문제 인식
- 설계 능력
- 구현 능력(코딩)
- 결과물(배포 링크, 동영상, GIF)

