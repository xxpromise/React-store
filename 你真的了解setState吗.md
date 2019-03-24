# 你真的了解 React 中 setState 吗？
1. setState 只在合成事件和钩子函数中是“异步”的，在原生事件和 setTimeout 中都是同步的。
2. 如果需要获取’异步‘场景的 setState 的值  --> this.setState(partial, callback) 在callback中拿到最新的值
3. 如果要在'异步'场景更新多次 setState --> this.setState((prevState, props) => {return newState})
