>[!IMPORTANT]
> An IPv4 address is a 32-bit address that uniquely and universally defines the connection of a device (for example, a computer or a router) to the Internet.

> [!NOTE]
> IP is the protocol that hides the underlying physical network by creating a virtual network view.
> It is an unreliable, best-effort, and connectionless packet delivery protocol.

#### Advantage of IPv4:
- Widely supported.
- Support of all OS.
- All Commonly used protocols are supported.
- Simplicity: it is simpler, easy to remember, require less memory.
- Familiarity: Millions of devices are already knowing it, existing infrastructure already support it .

#### IPv4 Standard:
- @ IPv4 standard that was adopted two decades ago as a robust, easily implemented standard. (IETF)
- @ IPv4 is being used successfully to support the communications systems in the emerging information society and has been updated to extend its useful life (e.g. [[#^e8d2fc|NAT]] mechanism, [[#^a17771|IPsec]] protocol, MPLS, Tunnelling).


#### IPv4 address:
- An IPv4 address is a 32-bit address that uniquely and universally defines the connection of a host or a router to the Internet.
- @ The address space of IPv4 is  2<sup>32</sup> or 4,294,967,296.
- @ IP addresses are usually written as: W . X . Y . Z/n  such that n mask   (e.g. 193.1.1.0/24)
- ? The network prefix identifies a network and the host number identifies a specific host


#### IPv4 Class:
| **Class** |      **Address Range**       |    **Network Bits**     | **Host Bits**  |  **Number of Networks**  | **Number of Hosts per Network** | **Default Subnet Mask** |
| :-------: | :--------------------------: | :---------------------: | :------------: | :----------------------: | :-----------------------------: | :---------------------: |
|   **A**   |     1.0.0.0 to 126.0.0.0     |         8 bits          |    24 bits     | 128 (0 and 127 reserved) |           16,777,214            |        255.0.0.0        |
|   **B**   |   128.0.0.0 to 191.255.0.0   |         16 bits         |    16 bits     |          16,384          |             65,534              |       255.255.0.0       |
|   **C**   |  192.0.0.0 to 223.255.255.0  |         24 bits         |     8 bits     |        2,097,152         |               254               |      255.255.255.0      |
|   **D**   | 224.0.0.0 to 239.255.255.255 |        Multicast        | Not applicable |      Not applicable      |    Used for multicast groups    |     Not applicable      |
|   **E**   | 240.0.0.0 to 255.255.255.255 | Reserved for Future Use | Not applicable |      Not applicable      |      Experimental use only      |     Not applicable      |

- IPv4 Private Address Range:

| **Class** |   **Private Address Range**    |    **Network Bits**     | **Host Bits**  |  **Number of Networks**  | **Number of Hosts per Network** | **Default Subnet Mask** |
| :-------: | :----------------------------: | :---------------------: | :------------: | :----------------------: | :-----------------------------: | :---------------------: |
|   **A**   |   10.0.0.0 to 10.255.255.255   |         8 bits          |    24 bits     | 128 (0 and 127 reserved) |           16,777,214            |        255.0.0.0        |
|   **B**   |  172.16.0.0 to 172.31.255.255  |         16 bits         |    16 bits     |          16,384          |             65,534              |       255.255.0.0       |
|   **C**   | 192.168.0.0 to 192.168.255.255 |         24 bits         |     8 bits     |        2,097,152         |               254               |      255.255.255.0      |
|   **D**   |              N/A               |        Multicast        | Not applicable |      Not applicable      |    Used for multicast groups    |     Not applicable      |
|   **E**   |              N/A               | Reserved for Future Use | Not applicable |      Not applicable      |      Experimental use only      |     Not applicable      |

#### 
> [!NOTE]
> In classful addressing, a large part of the available addresses were wasted.

> [!NOTE]
> Classful addressing, which is almost obsolete, is replaced with classless addressing.

> [!NOTE]
> In IPv4 addressing, a block of  addresses can be defined as x.y.z.t /n
> in which x.y.z.t defines one of the addresses and the /n defines the mask.

> [!NOTE]
> The first address in the block can be found by setting the rightmost 32 − n bits to 0s.
>> [!Example]
>> 205.16.37.39/28. What is the first address in the block?
>> - The binary representation of the given address is
>> - 11001101   00010000   00100101   00100111
>> - If we set 32−28 rightmost bits to 0, we get
>> - 11001101    00010000    00100101   0010000 or   205.16.37.32.

> [!NOTE]
> The last address in the block can be found by setting the rightmost  32 − n bits to 1s.
>> [!Example]
>> Find the last address for the block 205.16.37.39/28?
>> -  The binary representation of the given address is
>> - 11001101    00010000    00100101    00100111
>> - If we set 32 − 28 rightmost bits to 1, we get
>> - 11001101 00010000 00100101 00101111 or 205.16.37.47 . 

> [!NOTE]
> The number of addresses in the block can be found by using the formula  2<sup>32−n</sup>.
>> [!Example]
>> Find the number of addresses in 205.16.37.39/28 ?
>> - The value of n = 28, which means that number of addresses is 2<sup>32−28</sup> or 16.

>[!TIP]
>The first address in a block is normally not assigned to any device.
> it is used as the network address that represents the organization to the rest of the world.

> [!NOTE]
> Each address in the block can be considered as a two-level hierarchical structure: 
> the leftmost n bits (prefix) define the network;
> the rightmost 32 − n bits define the host.
#### Definitions:
1. **[[#^9304ef|IP]]:** *is the methods or rules used for transfer of data across the network.*
2. **[[#^e637af|NAT]]:** *is the process of mapping an internet protocol (IP) address to another by changing the header of IP packets while in transit via a router.* ^e8d2fc
3. **[[#^2eccfc|IPsec]]:** *Internet Protocol Security (IPsec) is a secure network protocol suite that authenticates and encrypts packets of data to provide secure encrypted communication between two computers over an Internet Protocol network*  ^a17771

#### Abbreviations:
1. **IP:** *Internet Protocol.* ^9304ef
2. **NAT:** *Network Address Translation.* ^e637af
3. **IPsec:** *Internet Protocol Security.* ^2eccfc