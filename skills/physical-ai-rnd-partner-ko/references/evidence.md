# 근거·실제 읽은 범위·적용 한계

검토일: 2026-11-01. 기존 준비 조사 21개와 생성 전 추가 확인 5개다. 아래는 원문 전체/선택 범위를 구별한 기록이며, 이번 추가 검토에서 기존 21개를 모두 다시 읽었다는 뜻은 아니다. 리뷰의 피인용 연구·저자 데이터·코드를 전부 재검증하거나 그래프를 이미지로 전수 판독하지 않았다.

이 스킬의 협업 규칙은 원문과 사용자 요구를 연결한 설계 판단이다. 연구·조직 지침·프레임워크 문서를 서로 구별한다. 서로 다른 연구의 결과를 합쳐 생산성·전문성·로봇 작업 효과가 검증됐다고 하지 않는다. 실제 사용하는 라이브러리/모델/서버 버전은 작업마다 확인한다.

## AI와 함께 문제를 탐색하고 판단하기

- **C1 [Grounded Copilot](https://shraddhabarke.github.io/raw/copilot.pdf)**: 본문 §§1–6,8(PDF1–22,23–24) 선택 독해; §7·부속 영상 제외. 20명 관찰과 grounded theory로 탐색/가속 사용을 구별했다. 초기 Copilot·학계 편중 표본의 정성 연구다. 불완전한 요청을 탐색의 출발점으로 삼되 최적 대화법의 인과 증거로 쓰지 않는다.
- **C2 [Shen & Tamkin, 2026](https://arxiv.org/html/2601.20245v1)**: §§3–7, 부록A–C 및 도입을 읽음; §2·그림 지시문 전체 제외. Python 경험자·Trio 미경험자52명의 무작위 채팅지원 비교에서 즉시 시험 성과와 작업 속도가 일치하지 않았다. 대화 패턴별 차이는 사후 관찰이다. 검토 이유·확인 방법을 제공하되 장기 성장 효과나 강제 퀴즈를 정당화하지 않는다.
- **C3 [METR early-2025 연구](https://metr.org/Early_2025_AI_Experienced_OS_Devs_Study-paper.pdf)**: 본문§§1–4, 부록B·C.3·D.1–4 선택 독해. 숙련 개발자16명의 익숙한 저장소246과제에서 당시 도구 허용이 완료시간을 늘렸다. 제한된 표본·과제·2025년 도구의 효과이며 현재 모든 AI에 일반화하지 않는다. 체감 속도와 실제 품질/시간을 구별한다.
- **C4 [METR 2026-02-24 후속](https://metr.org/blog/2026-02-24-uplift-update/)**: 기사 본문 전체, 연결 데이터 재분석 없음. 후속의 참여·과제 선택과 동시 agent 시간측정 문제 때문에 현행 효과를 신뢰할 만한 단일 추정으로 보기 어렵다고 설명한다. 생산성 비교에 시점·과제·품질·시간 정의가 필요하다.
- **C5 [METR 2026-05-11 설문](https://metr.org/blog/2026-05-11-ai-usage-survey/)**: 기사 본문 전체, 부록 일부. 기술직349명의 편의표본·자기보고다. 응답 일관성이 실제 반사실의 정확성을 보증하지 않는다. 생산성 배율의 인과 추정이나 앞선 RCT의 단순 반박으로 쓰지 않는다.

## ML 시스템의 연구개발과 유지보수

- **M1 [Hidden Technical Debt, 2015](https://papers.nips.cc/paper_files/paper/2015/file/86df7dcfd896fcaf2674f757a2463eba-Paper.pdf)**: §§1–9/PDF1–8 본문 전체. 운영 경험의 분석으로 데이터 의존·결합·숨은 소비자·설정·재현성 부채를 분류했다. 통제실험·정량적 투자수익 증거는 아니다. 변경의 시스템 영향과 복잡성 비용을 검토하는 근거다.
- **M2 [The ML Test Score, 2017](https://storage.googleapis.com/gweb-research2023-media/pubtools/4156.pdf)**: 공식10쪽 PDF §§I–VII-D 본문·표 전체. 운영 경험과36팀 인터뷰에서 데이터·모델·인프라·감시28항목을 제안했다. 장애 감소의 인과효과는 검증하지 않았고 TFX 예시는 가상 평가였다. 일반 코드 검사에 모델·데이터 평가를 더하되 PoC에 점수 할당량을 강제하지 않는다.
- **M3 [Software Engineering for ML, 2019](https://www.microsoft.com/en-us/research/wp-content/uploads/2019/03/amershi-icse-2019_Software_Engineering_for_Machine_Learning.pdf)**: §§I–IX/PDF1–10 본문 전체. Microsoft14명 인터뷰·551명 설문으로 반복 워크플로, 데이터·모델 계보와 결합 문제를 기술했다. 자기보고·단일조직·객관 성과 기준 부재가 한계다. 성숙도 상관을 특정 절차의 인과효과나 필수 단계로 옮기지 않는다.

## 실험과 재현성

- **R1 [Deep RL that Matters](https://arxiv.org/html/1709.06560)**: 본문 전체와 보충 Random Seeds·일부 방법/통계 문단. MuJoCo 알고리즘 실험에서 구현·환경·하이퍼파라미터·seed가 결과에 영향을 줬다. 검토한 과제에 한정되며 보편적 반복 횟수는 정하지 않는다. 행동 관찰·기준 재현·변경 기록을 연결한다.
- **R2 [Statistical Precipice](https://arxiv.org/html/2108.13264)**: 본문§§1–6, 부록A.4–A.5 및A.3 일부. 벤치마크 재평가·재표집으로 점추정·최댓값 선택의 불안정성을 분석했다. 소수 run의 단일 작업에는 정보가 부족하다. 불확실성·효과·표본 단위를 남기되 IQM·bootstrap·고정 seed 수를 일률 적용하지 않는다.
- **R3 [Good Enough Practices, 2017](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005510)**: Author summary와 Overview–Conclusion 본문 전체. 소규모 연구 경험 기반의 실천 권고이며 생산성 실험이 아니다. 원자료·처리·의존성·버전·알려진 입출력 확인을 연결한다. 큰 프로젝트 관행을 최소 목록에서 생략한 것이 자동화/리뷰가 불필요하다는 뜻은 아니다.

## 공학과 로봇 인터페이스

- **E1 [Google 코드 리뷰](https://google.github.io/eng-practices/review/reviewer/looking-for.html)**: 본문 전체. 조직 지침으로 설계·동작·복잡성·테스트 타당성·문서·맥락을 검토한다. AI 작성 테스트도 검토하며 복잡성을 정당화한다. 지침 자체가 효과 크기의 실험은 아니다.
- **E2 [Google Small CLs](https://google.github.io/eng-practices/review/developer/small-cls.html)**: 본문 전체. 목적 하나의 이해 가능한 변경과 관련 사용/검사를 연결한다. 줄 수보다 개념적 응집도와 복구 가능성을 참고한다. 조직의 테스트 정책을 모든 저영향 작업의 필수 할당량으로 복제하지 않는다.
- **E3 [Nygard ADR, 2011](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions)**: 글 전체. 중요한 선택의 상황·결정·상태·결과를 보존하는 초기 경험 보고다. 이유·불이익·재검토 조건을 기존 기록에 남기되 모든 변경에 새 문서를 만들지 않는다.
- **E4 [NIST OFAT](https://www.itl.nist.gov/div898/handbook/pri/section2/pri212.htm)**: 본문·수식·그림 설명 전체. 가상 모형으로 상호작용 누락을 설명하는 통계 지침이다. 작은 디버깅 변경과 효과 추정용 실험 설계를 구별한다. 모든 실험의 단일 변수/전체 조합을 강제하지 않는다.
- **E5 [NASA Verification, 5.3](https://www.nasa.gov/reference/5-3-product-verification/)**: 정의·입력·활동/조정·준비 부분(L257–306). 명세에 맞는지 확인하고 프로젝트에 맞춰 절차를 조정하는 공식 지침이다. 장 전체와 관련 표준을 읽었다고 하지 않는다.
- **E6 [NASA Validation, 5.4](https://www.nasa.gov/reference/5-4-product-validation/)**: 목적·입력·방법·준비/실행 부분(L256–316). 의도된 사용 조건의 사용자 기대를 확인한다. 앞의 명세 준수와 작업 목적을 구별하되 항공우주 인증 절차를 PoC에 도입하지 않는다.
- **E7 [ROS REP103](https://raw.githubusercontent.com/ros-infrastructure/rep/master/rep-0103.rst)**: 전문. 단위·body/optical 축·회전 표기의 공식 관례와 예외를 다룬다. 모든 SDK/정책이 같은 관례를 따른다고 가정하지 않고 양쪽 경계를 확인한다. ros.org 접근 거부 후 공식 저장소 원문 사용.
- **E8 [ROS2 Clock and Time](https://design.ros2.org/articles/clock_and_time.html)**: 본문 전체. 시스템·ROS·steady 시간과 SIM 정지/역행·통신 지연을 다룬 설계 문서다. 실제 버전 API 검증을 대신하지 않는다. 시각 도메인·최신성·replay/reset을 구별한다.
- **E9 [NVIDIA Simulation to Reality](https://docs.nvidia.com/learning/physical-ai/getting-started-with-isaac-lab/latest/robot-learning-fundamentals/08-simulation-to-reality.html)**: 본문 전체, 연결 논문/튜토리얼 전부는 제외. 인터페이스 오류와 물리 차이를 측정하고 대응을 고르는 공식 입문 지침이다. randomization이 잘못된 연결을 고치지 않으며 실물 전이는 실물 증거가 필요하다.
- **E10 [DORA 작은 변경](https://dora.dev/capabilities/working-in-small-batches/)**: 페이지 본문 전체, 연결 보고서 전체 제외. 소프트웨어 전달의 빠른 피드백과 리뷰 부담을 다루는 연구 기반 지침이다. 배포 빈도·체크인 횟수를 로봇 실험의 필수 빈도로 바꾸지 않는다.

## 생성 전 추가 확인

- **N1 [Human-AI Interaction, CHI2019](https://www.microsoft.com/en-us/research/wp-content/uploads/2019/01/Guidelines-for-Human-AI-Interaction-camera-ready.pdf)**: 표1·§§3–4·§5 일부·§§6–7·부록G9/G11/G16 선택 독해. 권고 통합·내부 검토 뒤 HCI 실무자49명의20제품 평가와 후속 전문가 검토로 명료성/적용 가능성을 조사했다. 공동판단의 성과 실험이 아니다. 사용자 정정 후 전제·계획·판정에 미친 변화를 반영하는 규칙으로 전이하되 장문 설명이나 상시 승인 절차를 강제하지 않는다.
- **N2 [Kapoor & Narayanan, arXiv v1](https://arxiv.org/pdf/2207.07048v1)**: 도입·§2.1·§2.4·§3.4·§4 일부. 오류 조사 종합과 내전예측 사례 분석으로 분할·전처리·의존성·분포 불일치를 다룬다. 체계적 모집단 메타분석/로봇 실증은 아니다. Patterns 최종본은 접근 차단되어 읽지 않았으며 판본별 수치를 섞지 않는다. 새 단위 일반화 주장에 맞는 원본 단위 분할과 정보 경로를 확인한다.
- **N3 [Farama Step API](https://farama.org/Gymnasium-Terminated-Truncated-Step-API)**: 본문 전체. 종료와 외부 truncation의 bootstrap 차이·유한 horizon 예외를 설명하는 공식 설계 근거다. 단순히 실행되는 코드도 다른 학습 의미를 가질 수 있다. 모든 timeout/API를 획일적으로 고치지 않고 작업 MDP·버전을 확인한다.
- **N4 [PyTorch Reproducibility](https://docs.pytorch.org/docs/2.15/notes/randomness.html)**: 본문 전체. 난수원·비결정성·DataLoader·성능 비용과 환경 간 비보장을 다룬 공식 문서다. seed만으로 재현을 확정하지 않는다. 확인한 문서 버전과 실제 실행 버전을 구별하며 결정성 옵션을 무조건 켜지 않는다.
- **N5 [PyTorch 모델 저장/로드](https://docs.pytorch.org/tutorials/beginner/saving_loading_models.html)**: state_dict/buffer, general checkpoint, train/eval, warm start 부분 선택 확인. 추론용 가중치·optimizer를 포함한 재개·부분 재사용의 차이를 다룬 공식 튜토리얼이다. 알고리즘별 RNG/replay/SIM 상태를 모두 저장한다는 보장은 없다. 저장 범위와 실제 재개를 확인한다.

## 검증을 해석하는 기준

원문 읽기는 근거 검토이고, 스킬 응답 검사는 지시 준수·정확성·작업 수행 범위를 확인하는 것이다. 실제 학습·생산성·유지보수 비용·로봇 작업 효과는 별도의 관측과 평가가 필요하다. 이 자료를 읽었다는 사실이나 여러 AI의 일치로 그 효과를 주장하지 않는다.
