# 1.이미지 데이터 제너레이터가 하는 역할과 코드 
이미지를 학습시킬 떄 학습데이터의 양이 적을 경우 학습데이터를 조금 변형시켜서 학습데이터의 양을 늘리는 방식중 하나입니다.
ex) train_datagen = ImageDataGenerator(
          rescale = 1./255,
          rotation_range = 40,
          width_shift_range = 0.2,
          height_shift_range=0.2,
          shear_range=0.2,
          zoom_range=0.2,
          horizontal_flip=True,
          fill_mode='nearest')

# 2. 이미지 증강기법
이미지 증강기법은 이미지의 크기,밝기,회전등을 통해 학습 등의 데이터를 부풀려주는 행동을 말한다.위에있는 ImageDataGenerator을 사용한다.
# 3. 타임시리즈 데이터 분석용 Prophet 라이브러리 사용법
Prophet은 합리적이고 정확한 예측을 훨씬 더 간단하게 만들고,값 유형, 기본값, 유효성 검사 논리, 모델 속성의 기타 기능을 설명합니다
ex)m=Prophet()
   m.fit(avocado_df_sample)
   future = m.make_future_dataframe(periods=365)
   forecast = m.predict(future)
   forecast
   m.plot(forecast)
   m.plot_components(forecast)
 
