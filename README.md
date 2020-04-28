# pytorch初阶
## pytorch notes day 1
### 数据生成
torch.zeros((x, y))<br/>
torch.ones((x, y))<br/>
torch.full((x, y), 值)<br/>
torch.arange(low, high, step) 注意：high取不到<br/>
torch.linspace(low,high,值的数量)<br/>
torch.normal(mean, std) 注意：mean、std都是张量，作用：取得每一个元素对应的正态分布<br/>
torch.randint([, ), size=(生成tensor的维度))<br/>
torch.randperm(n)注意：得到的是0~n-1的打乱顺序的数组<br/>
torch.ones_like(tensor)<br/>
### tensor变换
torch.cat([需要拼接的序列]，dim=)注意：dim=哪个维度就会变化<br/>
torch.stack([需要拼接的序列]，dim=)注意：与torch=cat的区别在于：会出现新的维度<br/>
torch.chunk(需要拆开的tensor, dim=, chunks=拆开维度对应的元素大小，如果元素个数不能整除，那最后会取余)<br/>
torch.split(需要拆开的tensor, [需要拆开的维度的序列，要保证序列之和等于该dim的和]，dim=)<br/>
torch.index_select(需要选择的tensor, dim=, index=需要从dim选择出的序号构成的tensor)<br/>
torch.masked_select(需要选择的tensor, 与选择的tensor相同的布尔tensor)<br/>注意：最后得到的是一个一维数组
torch.reshape的内存地址与原来的tensor一样<br/>
torch.transpose(t, dim0=1, dim1=2)注意：c*h*w     c*w*h<br/>
### tensor比较总结
t.ge is mean greater than or equal<br/>
t.gt: greater than<br/>
t.le: less or equal<br/>
t.lt: less than<br/>
注意：得到的是以一个shape与t相同shape的tensor（元素是布尔类型）
