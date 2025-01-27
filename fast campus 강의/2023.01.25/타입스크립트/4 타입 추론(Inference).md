# 4. 타입 추론(Inference)

# 📌 타입 추론

<aside>
💡 추론? - **어떠한 판단을 근거삼아 다른 판단을 이끌어냄.**

</aside>

## 1. 초기화된 변수

```tsx
let num = 12
num 'Hello type!!' // 에러, num은 number 타입으로 명시되었기 때문에 string 형식으로 할당 불가
```

`num` 변수엔 타입이 없음 → 즉, 타입스크립트가 `num` 에 할당된 값을 보고 추론함

## 2. 기본값이 설정된 매개변수

`b` 는 **타입이 없어도 숫자가 들어갔기 때문에** 타입스크립트가 쉽게 추론함

## 3. 반환값이 있는 함수

```tsx
function add(a: number, b = 2) {
	return a + b;
}
```

`add()` 함수 반환값 명확 → 타입을 지정하지 않아도 쉽게 추론함