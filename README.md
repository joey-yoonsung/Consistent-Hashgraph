# Consistent-Hashgraph

이 프로젝트는 Hashgraph 단점인 consistency 를 어느 시점에 판단해야할지 기준을 알 수 없다는 문제를 해결하기 위한 연구를 진행할 wiki 프로젝트이다.

기존의 BFT 알고리즘에설 primary 를 지정해서 합의하는 방식의 아이디어를 적용시켜서 consistency 를 보장하는 방법을 테스트 결과 중심으로 연구할 계획이다.

첫번째 연구 목표는 Hashgraph 알고리즘에 어떻게 primary - non-primary 컨셉을 적용시킬지 논리적인 방법 설계이다.
현재 구상하고 있는 바로는 PBFT 와 같은 broadcast 방식과 BChain 과 같은 chaingng 방식을 적용했을 때 어떤 모델 설계가 가능한지, 논리적인 whole 은 없는지 검증을 할 계획이다.

두 번째 핵심 목표는 BChain 이 강조하고 있는 것 처럼 장애가 발생했을때 빠른 recovery 능력을 갖추는 것을 목표로 한다.
왜냐하면 HashGraph 방식은 이미 기존의 합의 알고리즘보다 빠른 처리 성능을 보여줄 수 있다는 것이 담보되어있기 때문이다.
장애 상황에서 어떻게 기존의 빠른 처리성능을 최대한 떨어뜨리지 않고, malicious primary 의 detection 과  and trasanction recovery 를 가능하게 할 것인가를 찾아내야 한다. 이 부분은 앞의 첫 번째 연구목표에서 어느 정도 논리적인 consistency 합의 타당성 결과가 나와야 agile 하게 아이디어를 내고 진행해볼 수 있을 것으로 예상한다.



실제 구현 프로젝트는 이름에 `-${language name}`을 붙여서 따로 만든다.
초기 구현 및 검증에 사용할 언어는 go 언어로 만들 계획이다.
프로젝트 이름은 우선 Consistet-Hashgraph 로 했는데 연구를 진행하면서 적합한 이름이 나오면 바꿀 수 있다.

함께 온/오프라인 토론 및 참여를 원하는 분은 언제든 sw.yoonsung@gmail.com 으로 메일을 보내주세요.
