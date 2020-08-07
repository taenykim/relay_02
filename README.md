# Skylove (스카이러브)

스카이러브 채팅 웹사이트입니다. 
LINK: http://49.50.162.241:3000

## 스크린샷

|로그인 화면|
|:--:|
|![index](https://user-images.githubusercontent.com/48251136/89639539-b4780c00-d8e8-11ea-8a19-f71b99cad83b.png)<br>|
|로비 채팅 룸|
|![chat](https://user-images.githubusercontent.com/48251136/89639536-b346df00-d8e8-11ea-8476-b8894b345aec.png)<br>|
|1대1 매칭 채팅 룸|
|![match](https://user-images.githubusercontent.com/48251136/89639540-b510a280-d8e8-11ea-9d2f-2933ca1353e3.png)<br>|


## 시나리오

- [ ] 0. 회원가입을 합니다. (선택)
- [x] 1. ID, PW를 입력하여 로그인을 합니다. (필수 - 기능 A)
- [ ] 2. 왼쪽에 프로필 사진을 추가합니다. (필수 - 기능 B) 프로필 설정을 수정할 수도 있어요. (필수 - 기능 C)
- [x] 3. 가운데 공간에서 스카이러브가 상대를 추천해줍니다. (필수 - 기능 A, C)
- [ ] 4. 왼쪽의 사람(리스트)를 클릭하면, 오른쪽에 상대방의 프로필이 나옵니다. (필수 - 기능 A, C / 선택 - 기능 B, 프로필 이미지 가리기 기능)
- [ ] 5. 상대방의 프로필 설명에는 스카이러브의 추천 이유가 포함됩니다. (선택 - 기능 C)
- [x] 6. *추천 리스트에 있는 상대를 클릭하고*, 들어가기 버튼(Match Room)을 누르면 채팅방으로 입장합니다.  (필수 - 기능 A) -> **Match Room을 통해 자동 입장으로 변경**
- [x] 7. 채팅이 이루어지고 나면, 언행점수가 변화합니다. (필수 - 기능 A) 채팅을 통해 얻은 자연어를 기반으로 단어 파싱을 진행하여 & 긍정/부정을 인식을 통해 사용자의 성향을 파악합니다.  -> **사용자 점수만 현재 추출(NLP), 추후 DB에 추가 필요**
- [x] 8. 채팅에서 나가려면 나가기 버튼을 클릭합니다. (필수 - 기능 A)


## 기획서

#### [Link](https://github.com/boostcamp-2020/relay_02/blob/master/%EA%B8%B0%ED%9A%8D%EC%84%9C.md)

## 1. DB
DB 확인용 스크립트
```
cd chatapp
node db/dbtest.js # 반드시 위치여야합니다!
```

### Wiki: [Link로 이동하기](https://github.com/boostcamp-2020/relay_02/wiki/DB-%EA%B0%80%EC%9D%B4%EB%93%9C)


## 2. Chat App

### 설치 및 실행

```bash
cd chatapp
npm install # express moment socket.io sqlite3

npm run dev # start dev-server
npm start # start server
```

### Documentation

|Filename|Desc|Docs|
|--|--|--|
|`server.js`|서버 파일| https://github.com/boostcamp-2020/relay_02/issues/6|
|`main.js`|채팅 클라이언트 파일|https://github.com/boostcamp-2020/relay_02/issues/7|
|`index.html` `chat.html` | 웹사이트 파일 |https://github.com/boostcamp-2020/relay_02/issues/8|


## 3. 기능 A. 대화 패턴 긍정도 분석
> 링크: https://github.com/boostcamp-2020/relay_02/tree/master/NLP

### 설치 및 실행

```
python --version # 3 이상
pip install jupyter
jupyter notebook #jupyter 속에서 NLP/NLP.ipynb 파일 실행
```

필요 라이브러리

|Library|Desc|
|--|--|
|jupyter notebook| jupyter notebook 뷰어 및 편집기 (jupyter-lab 도 가능)|
|konlpy|한국어 정보처리를 위한 파이썬 패키지. Okt를 사용하여 형태소를 분석한국어 정보처리|
|nltk|데이터 전처리 과정을 위한 라이브러리|
|tensorflow|머신러닝 오픈소스|
|matplotlib|시각화 도구|
|numpy|수학 연산(배열, 통계, 행렬)을 위한 패키지|


## 4. 기능 B. 동물상 기반 추천 기능(필수)



## 5. 기능 C. 회원 정보 기반 이성 추천 기능(필수)



## Contributing
네이버 커넥트재단 부스트캠프에 참여하신 모든 분들의 참여 기다립니다.



## License
[MIT](https://choosealicense.com/licenses/mit/)
