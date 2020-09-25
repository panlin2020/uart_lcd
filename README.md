# uart_lcd
uart lcd display module
> UartSend (“CLR(0);SBC(3);DC16(0,0,'Uart显示屏',1);DC24(0,20,'Uart显示屏',1);DC32(0,48,'Uart显示屏',1);DCV16(0,84,'Uart显示屏',1);DCV24(0,104,'Uart显示屏',1);DCV32(0,132,'Uart显示屏',1);PL(0,170,175,170,1);BOXF(110,180,170,210,1);CIR(50,195,20,1);\r\n”);
Delay_ms(100);



#
>double v=0.12;
>char buf[128];
>char i;
>for(;;)
>{  v=0;
 > for(i=0;i<50;i++)
>  {
>sprintf(buf,"CLR(15);DC48(80,180,'%3.1f',1);\r\n",v);	
>    v=v+1.2;
>   UartSend(buf);
>    delay_ms(10);
>   }
>}
