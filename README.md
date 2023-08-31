# jest

- 조건: input value가 number type인지 확인

## 정상
![image](https://github.com/software92/jest-test/assets/95457388/409d4a78-1246-445b-9a25-bd4a1a3f7862)
![image](https://github.com/software92/jest-test/assets/95457388/880a98bd-2672-4a4f-a2e0-d7136bd9b18b)

- input의 value가 number일 때, 정상 동작


## 에러

![image](https://github.com/software92/jest-test/assets/95457388/7909ba5e-fad2-49cb-a876-d04872a54e68)
![image](https://github.com/software92/jest-test/assets/95457388/5781c5cd-f0a3-484a-84ad-45b4286b69b2)


- input의 value가 string일 때, error




## jest 정리
- CRA 사용 시 제공(npm test)
- 전체 검사를 하지 않으면, 마지막 커밋 이후 변화된 코드와 관련된 테스트만 실행
- __test__ 디렉터리 안이나 *.test.js 파일을 테스트 파일로 인식

```example
// test([문자열 설명(에러가 났을 때 콘솔에서 확인할 수 있는 테스트 이름], () => {
test('input value is number', () => {
  const inputValue = 123;
  const inputValueType = typeof inputValue;

  // expect: 테스트 전역 메소드, 테스트 환경에서 사용하는 함수?
  // expect([테스타할 대상/변수/함수..]).[매처: 대상이 조건과 일치하는 지 확인하는 함수];
  expect(inputValueType === 'number').toBeTruthy();
});
```
