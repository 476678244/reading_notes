[从代码实现层面思考 Kubernetes 为什么会弃用对 Docker 的支持？](https://colstuwjx.github.io/2021/08/%E6%BA%90%E7%A0%81%E8%A7%A3%E8%AF%BB%E4%BB%8E%E4%BB%A3%E7%A0%81%E5%AE%9E%E7%8E%B0%E5%B1%82%E9%9D%A2%E6%80%9D%E8%80%83-kubernetes-%E4%B8%BA%E4%BB%80%E4%B9%88%E4%BC%9A%E5%BC%83%E7%94%A8%E5%AF%B9-docker-%E7%9A%84%E6%94%AF%E6%8C%81/)
>2020年底，在 Kubernetes v1.20 正式发布的同时，k8s 官方还搞了一个大动作：他们宣布将会逐步弃用对 Docker 容器运行时的支持。为了不让用户惊慌失措，官方还贴心地写了一篇博客文章，对此事进行了一番详细说明。K8s 为什么会弃用对 Docker 的支持呢？除了官方的这篇文章以外，很多科技媒体也做了相应的解读，比如 infoq 的这篇文章。但是，为什么一定要弃用 docker 呢？这方面的维护成本究竟有多高？为了得到一个明确的答案，笔者决定展开一次 k8s 源码的探索之旅，一探究竟。

所以k8s去除的并不是docker镜像 而是docker运行时环境
