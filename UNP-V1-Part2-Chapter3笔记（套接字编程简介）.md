# UNP-Part2-Chapter3笔记（套接字编程简介）
- - -
IPv4套接字地址结构
```cpp
struct in_addr {
  in_addr_t         s_addr;        /* 32位 IPv4 地址, 网络字节序(大端) */
}
struct sockaddr_in {
  uint8_t           sin_len;       /* 结构体长度 */
  sa_family_t       sin_family;    /* AF_INET */
  in_port_t         sin_port;      /* 16-bit 端口号, 网络字节序(大端) */
  struct in_addr    sin_addr;      /* 32-bit IPv4 地址, 网络字节序(大端) */
  char              sin_zero[8];   /* unused */
}
```
