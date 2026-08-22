# Learning Record 0012: Real-Time Data Pipelines & WebSockets

## Concept Overview
- **Angular Pattern**: RxJS `webSocket()` (`WebSocketSubject`), `retry()` operators, and piping streams directly into templates using the `| async` pipe with manual `ngOnDestroy` unsubscriptions.
- **React Pattern**: Composable custom hooks (`react-use-websocket` / `useEventSource`), state-driven connection lifecycles, automatic unmount cleanup, and integrating delta streams directly into the TanStack Query cache via `queryClient.setQueryData()`.

## Key Bridges & Translations
1. `WebSocketSubject<T>` &rarr; `const { lastJsonMessage, sendJsonMessage } = useWebSocket(url)`.
2. RxJS `retry()` operator &rarr; Configurable `reconnectInterval` and `shouldReconnect` options.
3. `messages$ | async` in template &rarr; Declarative JSX rendering from hook state.
4. Custom Subject state cache &rarr; Real-time patching of TanStack Query cache.

## Packages & References
- [`react-use-websocket`](https://www.npmjs.com/package/react-use-websocket) &bull; [react-use-websocket GitHub](https://github.com/robtaussig/react-use-websocket)
- [`@tanstack/react-query`](https://www.npmjs.com/package/@tanstack/react-query) &bull; [TanStack Query WebSockets Docs](https://tanstack.com/query/latest/docs/framework/react/community/websockets)
