# can_imx35
On IMX35 with kernel 5.4.84 or higher if the application is processing CAN messages slow or the CPU load is high then CAN messages are dropped due to queue length check added in rx-offload.c
This queue length is calculated based on NAPI weight and even though there is enough space in recieve buffer the packets will be dropped. To have the similar behavior as old kernel this patch can be used
