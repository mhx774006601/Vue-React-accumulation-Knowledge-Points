之前带will的生命周期都没有了，是因为react16推出的Fiber是异步渲染，在render函数之前的所有函数，都有可能被执行多次。
React v16.0中的生命周期
componentWillMount,
componentWilllReceiveProps,
shouldComponentUpdate,
componentWillUpdate
以上几个在render前执行的生命周期。
如果开发者开了async rendering,而且又在以上这些render前执行的生命周期做ajax请求的话，那么ajax将被无谓的多次调用。

React16.0中有个生命周期componentDidCatch 叫错误捕获

react是单向数据流。
    父组件向子组件通信用props
    react中 子组件向父组件通信：在父组件中定义回调方法，然后把回调传给子组件，子组件通过调用父级的回调，来告知父级信息。
	  父级把这个回调传给子集，子组件调用子集。
    
    memo是高阶组件 :意思是我接收一个组件，将来再返回一个全新组件。
    就像上面的comment组件，它被返回了，就会拥有PureComponent这个组件的能力。
    React.memo适用于v16.6.0之后的版本。
    高阶组件是一个函数，它返回一个全新的组件，可以重写生命周期。
    
    装饰器只能用于class组件
    
    副作用钩子-effect Hook
    做的这个状态对UI会有影响，这就叫‘副作用’
    副作用钩子会在每次渲染时都执行。
    把它理解为生命周期的一个复合。
