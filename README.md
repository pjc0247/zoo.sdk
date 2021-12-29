# zoo.sdk

## concept.Auth

```tsx
const { user } = useMe();

return <div>{!!user ? "안녕하세요" : "로그인해주세요"}</div>;
```

**sign-in**

```tsx
const { signIn } = useMe();

await signIn("pjc0247@naver.com", "password");
```

```tsx
const { signInWithFacebook, signInWithGoogle, signInWithKakao } = useMe();

await signInWithFacebook(fbAccessToken);
await signInWithGoogle(googleToken);
await signInWithKakao(kakaoToken);
```

## concept.Board

```tsx
const { totalPage, posts } = usePosts("자유게시판");
```

**pagination**

```tsx
const { totalPage, posts } = usePosts("자유게시판", {
  page: 1,
  pageSize: 20,
});
```

**search**

```tsx
// search with query
const { posts } = usePosts("자유게시판", {
  q: "검색어",
});

// complex search
const { posts } = usePosts("자유게시판", {
  q: {
    author: { exact: "pmnxis" },
  },
});
```
