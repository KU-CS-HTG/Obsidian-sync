[[LDM]]
이미지에 사람은 감지하기 힘든 작은 노이즈(perturbation)를 추가하여 분류기의 성능을 낮추는 것으로, 악의적으로 사용되는 LDM의 Encoder, denoising 단계를 표적으로 삼아 공격하고 model의 학습 과정을 방해한다.

purification attack(생성 모델을 사용하여 perturbation을 제거)에 취약하다는 단점이 있고, perturbation이 들어간 패턴을 어느 정도 제거하여 방해를 무력화할 수도 있다.
