## typescript_220601

# 1.3 TypeScript을 배워야 할 이유
  - JS + `Type Safety`
  - 향상된 Error Handling(타입 에러를 탐색함)
    - `[1,2,3,4,5]+False = '1,2,3,4,5False'`
  - Runtime Error(코드 실행 전에 에러를 방지함)


  * Runtime Error: 개발 완료 후 사용자가 보는 에러

# 1.4 TypeScript 요구사항
  - NodeJS
  - VSCODE(Auto-Complete)

# 2.0 TypeScript 사용 원리
  - TypeScript >> JavaScript
  - 컴파일 전에 에러 검열이 이뤄짐

# 2.1 타입 명시(explicit) vs. 타입 추론(implicit)
  1. 타입 명시
    - `: [데이터유형]`
    - `let b : boolean = false`
  2. 타입 추론
    - 타입을 명시하지 않으나 기존 타입과 다른 타입으로 값이 변경될 때 에러 발생함

  * 타입 명시를 최소화하고 TypeScript이 추론하도록 함.(효율성)
    - 추론이 어려운 경우에 타입 명시가 필수적임.
    - `let c: number[] = []`

# TypeScript의 다양한 타입 알아보기
  - optional `?` [TYPE] | undefined
  - Type Alias
  - argument, function type
  - readonly ~

  - undefined
  - null
  - any: disable typescript's protection
  
  - void: return 없는 function. 별도 설정하지 않아도 됨.
  - never: return 없이 error를 발생시킬 때 사용함. / 공집합 표현
  - unknown: Type이 확실하지 않을 때 if + typeof 으로 체크하기
  - void > unknown > never

# Tuple
  - const player: [string, number, boolean] = ...

# Call Signatures
- Function / Argument / Return의 타입을 명세하기
- `type [CALL_SIGNATURE] = ([ARG_TYPE]) => [RETURN_TYPE];`
- `type Add = { ([ARG_TYPE]) : [RETURN_TYPE]}`
- const [FUNCTION]:[CALL_SIG] = ~

# OverLoading
  - 외부 Package에서 많이 사용함.
  - 여러 call signatures를 보유한 function

# Polymorphism
  - concrete type
  - generic type
    - <[GENERIC]>~[GENERIC]
    - 입력된 타입에 따라 일관성 있게 타입을 판단함
