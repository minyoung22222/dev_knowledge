# useCallback

```jsx
const memoizedCallback = useCallback(() => {
    doSomething(a, b);
}, [a, b]);
```

-   메모화된 콜백함수를 반환 (Returns a memoized callback)
-   컴포넌트가 렌더링 될 때마다 내부에 선언되어 있던 표현식도 매번 다시 선언된다.
    → 첫 마운트 될 때 함수를 한 번만 선언해놓고 재사용해서 사용하고 싶을 때 사용한다.
-   하위 컴포넌트가 React.memo()로 최적화 되어 있고 하위 컴포넌트에게 callback함수를 props로 넘길 때 상위 컴포넌트에서 useCallback으로 함수를 선언하는 것이 유용하다.
-   함수 안에서 사용하는 상태 혹은 props를 의존성 배열에 포함시켜야 합니다.

> -   리액트의 렌더링 성능 최적화를 위한 hook (불필요한 동작 or 렌더링을 막아 최적화)
> -   특정 함수를 새로 만들지 않고 재사용하고 싶을 때 사용

컴포넌트가 렌더링 되는지 React Dev Tools의 Profiler로 확인하기

https://codesandbox.io/embed/runtime-cdn-7lgu2h?fontsize=14&hidenavigation=1&theme=dark
