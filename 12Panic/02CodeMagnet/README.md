# 코드 자석 문제 p356
다음 코드는 냉장고를 시뮬레이션 하는 Refrigerator라는 타입을 정의하고 있습니다. Refrigerator는 기본 타입으로 문자열 슬라이스를 사용하며 이 슬라이스에는 냉장고에 들어있는 음식들의 이름이 담깁니다. 이 타입은 문을 여는 행위를 시뮬레이션하는 Open메서드와 닫은 행위에 대한 Close메서드를 가지고 있습니다. FindFood 메서드는 Open메서드를 통해 문을 연 다음 Find 함수를 사용해 슬라이스 목록에서 특정 음식을 찾고 나면 다시 Close 메서드를 사용해 문을 닫습니다.

하지만 FindFood에는 문제가 하나 있습니다. 이 메서드는 찾는 음식이 없을 경우 에러 값을 반환하는데 에러가 반환되는 경우 Close가 호출되기 전에 함수가 먼저 종료되기 때문에 가상냉장고는 계속 열린 채로 방치될 것입니다!