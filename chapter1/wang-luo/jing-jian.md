为了便于实现，需要对一些事情进行简化。由于模拟blockchain网络需要许多机器，然而我们无法找到那么多机器。一个解决方法是通过虚拟机或者Docker进行仿真，但是这将使我们不得不处理许多关于虚拟路或者Docker的问题，从而使实现变得更加困难。因此，我们打算用单台机器运行多个节点的方式来模拟blockchain网络。为了达到此目的，将不再使用IP作为节点标识，而是使用端口号作为节点标识，例如节点地址为127.0.0.1:3001、127.0.0.1:3002、127.0.0.1:3003等。此时，我们使用NODE\_ID环境变量保存端口号，用来标识一个节点。这样可以打开不同的终端，设置不同的NODE\_ID，这样就拥有了多个节点。

节点采用端口号作为标识，这使得每个节点的blockchain和钱包文件也不相同，文件名需要和端口号对应起来，例如，**blockchain\_3000.db**, **blockchain\_30001.db** and **wallet\_3000.db**, **wallet\_30001.db**等等。

