# order-receipt-2019-8-22-3-14-40-234
LineItem�е�code smell
1.����ļ���������ӦΪ��д��Ӧ��Ϊ��descӦΪDescription��pӦΪprice��qtyӦΪQuantity�����ص�ֵҲ��ӦΪ��д

order�е�code smell
1.����Ӧ����Ϊprivate��
2.���ܽ�list����ֱ�ӷ���

orderreceipt�е�code smell
1. ��prints lineItems�µ�forѭ���д����ظ������Ը�Ϊ
 for (LineItem lineItem : o.getLineItems()) {
     output.append(lineItem.getDescription()||lineItem.getPrice()||lineItem.getQuantity());
            output.append('\t');
            output.append(lineItem.totalAmount());
            output.append('\n');
