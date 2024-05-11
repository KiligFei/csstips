# React Devtools

### 安装

打开 chrome 网上商店，搜索 react devtools ,可能需要科学上网

chrome 中右键点击检查，打开调试器，然后发现在调试器的 tab 栏末尾有最后两栏比较特殊的 tab，分别是 ⚛️ Components 和 ⚛️ Profiler，这两个就是 react devtools 的功能入口了

### Profiler 面板介绍

在 React 的官方文档中有介绍到 Profiler API 添加在 React 组件树中的任何地方来测量组件树中这部分渲染所带来的开销。

```tsx
<Profiler
  id="Navigation"
  onRender={(
    id, // 发生提交的 Profiler 树的 “id”
    phase, // "mount" （如果组件树刚加载） 或者 "update" （如果它重渲染了）之一
    actualDuration, // 本次更新 committed 花费的渲染时间
    baseDuration, // 估计不使用 memoization 的情况下渲染整棵子树需要的时间
    startTime, // 本次更新中 React 开始渲染的时间
    commitTime, // 本次更新中 React committed 的时间
    interactions // 属于本次更新的 interactions 的集合
  ) => {}}
>
  <div>
    <h2>Yay! Welcome to umi!</h2>

    {loading ? (
      <Spin />
    ) : (
      <>
        <Button
          onClick={() =>
            KiligModal.open(PromiseResolveModal, { title: "Nate" })
          }
        >
          Promise成功
        </Button>
        <Button onClick={() => clickUseOpen()}>useOpen</Button>
      </>
    )}
  </div>
</Profiler>
```
