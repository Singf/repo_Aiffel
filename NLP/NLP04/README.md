# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 지승환
- 리뷰어 : 노용욱


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - 중요! 해당 조건을 만족하는 부분을 캡쳐해 근거로 첨부
        - <img width="517" height="152" alt="image" src="https://github.com/user-attachments/assets/7ea01cb2-693f-42d3-bc11-aa4f8cb2e6d2" />

    
- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - <img width="854" height="346" alt="image" src="https://github.com/user-attachments/assets/83b2fecd-a906-41d9-ab04-45c3e71ebba8" />

        
- [x]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - <img width="716" height="258" alt="image" src="https://github.com/user-attachments/assets/9568d89a-beec-4e65-bb18-c4a7467909f3" />

        
- [x]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - <img width="1010" height="504" alt="image" src="https://github.com/user-attachments/assets/49f9efa5-c42a-47e7-a4cd-3485021bbc93" />

        
- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - 중요! 잘 작성되었다고 생각되는 부분을 캡쳐해 근거로 첨부
        - <img width="811" height="304" alt="image" src="https://github.com/user-attachments/assets/18fcfe30-1308-4ecb-973a-9ccbb5db645e" />



# 프로젝트 개요
- 과제명: Seq2Seq 실습 — 한국어 번역기 만들기
- 날짜: 2026-09-08
- 사용 기술: PyTorch, SentencePiece, GRU + Attention
- 제출 노트북: [`seq2seq.ipynb`](./seq2seq.ipynb)

한영 병렬 코퍼스로 **Attentional Seq2Seq** 번역기를 구현했습니다.
데이터 로드 → 전처리/코퍼스 구축 → SentencePiece 토크나이저 → Encoder/Attention/AttnDecoder → 학습 루프 → greedy decoding 추론까지 한 노트북에 들어 있습니다.

핵심 포인트:
- `AttnDecoder.forward`의 teacher forcing에서 `random` import가 빠져 `NameError`가 나던 부분을 수정
- 학습 중단 시 가중치가 날아가지 않도록 `./Seq2seq/checkpoint.pt` 체크포인트 저장/재개 추가
- 매 epoch 종료 후 K1~K4 예문을 바로 번역해 품질 변화를 확인


# 회고(참고 링크 및 코드 개선)
```
수제 코드를 이렇게 볼 수 있어서 너무 좋습니다.
더 좋은 성능을 만들어 내기 위해 많은 고민 하신 것이 느껴집니다.
지금의 노력이 꼭 더 큰 과실로 돌아 올 것이라 응원합니다. 
```
