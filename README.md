# order-receipt-2019-8-22-3-14-40-234
LineItem中的code smell
1.定义的几个变量不应为缩写，应改为：desc应为Description；p应为price；qty应为Quantity；返回的值也不应为缩写

order中的code smell
1.变量应定义为private；
2.不能将list集合直接返回

orderreceipt中的code smell
1. 在prints lineItems下的for循环中代码重复，可以改为
 for (LineItem lineItem : o.getLineItems()) {
     output.append(lineItem.getDescription()||lineItem.getPrice()||lineItem.getQuantity());
            output.append('\t');
            output.append(lineItem.totalAmount());
            output.append('\n');
