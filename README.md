# Grafana Dashboards for Bosch/Buderus heat pumps

Grafana dashboards for Bosch Compress 5800/6800i & Buderus Logatherm WLW176/186 heat pumps

![Circuits](/images/Grafana-circuits.png)
![Circuits](/images/Grafana-circuits_light.png)

## Images of indoor and outdoor unit

<img src="/images/indoor-unit_black.svg" width="25%" />
<img src="/images/outdoor-unit_black.svg" width="25%" />

<details>
<summary>Base64 Indoor Unit</summary>

```
data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgdmlld0JveD0iMCAwIDI0MS4zMTMyNTU1MDYxOTg4NiAzMDguMzMyOTkxNTMzNjg3NCIgd2lkdGg9IjQ4Mi42MjY1MTEwMTIzOTc3IiBoZWlnaHQ9IjYxNi42NjU5ODMwNjczNzQ4Ij4KICA8IS0tIHN2Zy1zb3VyY2U6ZXhjYWxpZHJhdyAtLT4KICAKICA8ZGVmcz4KICAgIDxzdHlsZSBjbGFzcz0ic3R5bGUtZm9udHMiPgogICAgICAKICAgIDwvc3R5bGU+CiAgICAKICA8L2RlZnM+CiAgPGcgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMCAxMCkgcm90YXRlKDAgMTEwLjY1NjYyNzc1MzA5OTQzIDE0NC4xNjY0OTU3NjY4NDM3KSI+PHBhdGggZD0iTTMyIDAgQzY3LjI5IDAsIDEwMi41NyAwLCAxODkuMzEgMCBNMzIgMCBDODEuOTMgMCwgMTMxLjg1IDAsIDE4OS4zMSAwIE0xODkuMzEgMCBDMjEwLjY1IDAsIDIyMS4zMSAxMC42NywgMjIxLjMxIDMyIE0xODkuMzEgMCBDMjEwLjY1IDAsIDIyMS4zMSAxMC42NywgMjIxLjMxIDMyIE0yMjEuMzEgMzIgQzIyMS4zMSAxMTcuNTQsIDIyMS4zMSAyMDMuMDcsIDIyMS4zMSAyNTYuMzMgTTIyMS4zMSAzMiBDMjIxLjMxIDEwNi42NCwgMjIxLjMxIDE4MS4yOCwgMjIxLjMxIDI1Ni4zMyBNMjIxLjMxIDI1Ni4zMyBDMjIxLjMxIDI3Ny42NywgMjEwLjY1IDI4OC4zMywgMTg5LjMxIDI4OC4zMyBNMjIxLjMxIDI1Ni4zMyBDMjIxLjMxIDI3Ny42NywgMjEwLjY1IDI4OC4zMywgMTg5LjMxIDI4OC4zMyBNMTg5LjMxIDI4OC4zMyBDMTUxLjc5IDI4OC4zMywgMTE0LjI3IDI4OC4zMywgMzIgMjg4LjMzIE0xODkuMzEgMjg4LjMzIEMxNDAuODMgMjg4LjMzLCA5Mi4zNCAyODguMzMsIDMyIDI4OC4zMyBNMzIgMjg4LjMzIEMxMC42NyAyODguMzMsIDAgMjc3LjY3LCAwIDI1Ni4zMyBNMzIgMjg4LjMzIEMxMC42NyAyODguMzMsIDAgMjc3LjY3LCAwIDI1Ni4zMyBNMCAyNTYuMzMgQzAgMTgzLjksIDAgMTExLjQ3LCAwIDMyIE0wIDI1Ni4zMyBDMCAxOTIuMDIsIDAgMTI3LjcxLCAwIDMyIE0wIDMyIEMwIDEwLjY3LCAxMC42NyAwLCAzMiAwIE0wIDMyIEMwIDEwLjY3LCAxMC42NyAwLCAzMiAwIiBzdHJva2U9IiMxZTFlMWUiIHN0cm9rZS13aWR0aD0iNCIgZmlsbD0ibm9uZSI+PC9wYXRoPjwvZz48ZyBzdHJva2UtbGluZWNhcD0icm91bmQiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDk1LjE0NTU5Njk3NTY1MzQ2IDU5LjA1MTA3MDY3MTI2ODY5KSByb3RhdGUoMCAyNC44MTU3NDI1ODIzMDI2MiAyNC44MTU3NDI1ODIzMDI4NDYpIj48cGF0aCBkPSJNNDkuNjMgMjQuODIgQzQ5LjYzIDI2LjI1LCA0OS41IDI3LjcxLCA0OS4yNSAyOS4xMiBDNDkuMDEgMzAuNTQsIDQ4LjYzIDMxLjk1LCA0OC4xMyAzMy4zIEM0Ny42NCAzNC42NSwgNDcuMDMgMzUuOTgsIDQ2LjMxIDM3LjIyIEM0NS41OSAzOC40NywgNDQuNzUgMzkuNjcsIDQzLjgzIDQwLjc3IEM0Mi45IDQxLjg3LCA0MS44NyA0Mi45LCA0MC43NyA0My44MyBDMzkuNjcgNDQuNzUsIDM4LjQ3IDQ1LjU5LCAzNy4yMiA0Ni4zMSBDMzUuOTggNDcuMDMsIDM0LjY1IDQ3LjY0LCAzMy4zIDQ4LjEzIEMzMS45NSA0OC42MywgMzAuNTQgNDkuMDEsIDI5LjEyIDQ5LjI1IEMyNy43MSA0OS41LCAyNi4yNSA0OS42MywgMjQuODIgNDkuNjMgQzIzLjM4IDQ5LjYzLCAyMS45MiA0OS41LCAyMC41MSA0OS4yNSBDMTkuMDkgNDkuMDEsIDE3LjY4IDQ4LjYzLCAxNi4zMyA0OC4xMyBDMTQuOTggNDcuNjQsIDEzLjY1IDQ3LjAzLCAxMi40MSA0Ni4zMSBDMTEuMTYgNDUuNTksIDkuOTYgNDQuNzUsIDguODYgNDMuODMgQzcuNzYgNDIuOSwgNi43MyA0MS44NywgNS44MSA0MC43NyBDNC44OCAzOS42NywgNC4wNCAzOC40NywgMy4zMiAzNy4yMiBDMi42MSAzNS45OCwgMS45OSAzNC42NSwgMS41IDMzLjMgQzEuMDEgMzEuOTUsIDAuNjMgMzAuNTQsIDAuMzggMjkuMTIgQzAuMTMgMjcuNzEsIDAgMjYuMjUsIDAgMjQuODIgQzAgMjMuMzgsIDAuMTMgMjEuOTIsIDAuMzggMjAuNTEgQzAuNjMgMTkuMDksIDEuMDEgMTcuNjgsIDEuNSAxNi4zMyBDMS45OSAxNC45OCwgMi42MSAxMy42NSwgMy4zMiAxMi40MSBDNC4wNCAxMS4xNiwgNC44OCA5Ljk2LCA1LjgxIDguODYgQzYuNzMgNy43NiwgNy43NiA2LjczLCA4Ljg2IDUuODEgQzkuOTYgNC44OCwgMTEuMTYgNC4wNCwgMTIuNDEgMy4zMiBDMTMuNjUgMi42MSwgMTQuOTggMS45OSwgMTYuMzMgMS41IEMxNy42OCAxLjAxLCAxOS4wOSAwLjYzLCAyMC41MSAwLjM4IEMyMS45MiAwLjEzLCAyMy4zOCAwLCAyNC44MiAwIEMyNi4yNSAwLCAyNy43MSAwLjEzLCAyOS4xMiAwLjM4IEMzMC41NCAwLjYzLCAzMS45NSAxLjAxLCAzMy4zIDEuNSBDMzQuNjUgMS45OSwgMzUuOTggMi42MSwgMzcuMjIgMy4zMiBDMzguNDcgNC4wNCwgMzkuNjcgNC44OCwgNDAuNzcgNS44MSBDNDEuODcgNi43MywgNDIuOSA3Ljc2LCA0My44MyA4Ljg2IEM0NC43NSA5Ljk2LCA0NS41OSAxMS4xNiwgNDYuMzEgMTIuNDEgQzQ3LjAzIDEzLjY1LCA0Ny42NCAxNC45OCwgNDguMTMgMTYuMzMgQzQ4LjYzIDE3LjY4LCA0OS4wMSAxOS4wOSwgNDkuMjUgMjAuNTEgQzQ5LjUgMjEuOTIsIDQ5LjU3IDI0LjEsIDQ5LjYzIDI0LjgyIEM0OS42OSAyNS41MywgNDkuNjkgMjQuMSwgNDkuNjMgMjQuODIiIHN0cm9rZT0iIzFlMWUxZSIgc3Ryb2tlLXdpZHRoPSI0IiBmaWxsPSJub25lIj48L3BhdGg+PC9nPjwvc3ZnPg==
```

</details>

<details>
<summary>Base64 Outdoor Unit</summary>

```
data:image/svg+xml;base64,PHN2ZyB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgdmlld0JveD0iMCAwIDI5My4zNjkxODAzNzczNDY3NyAyMTQuMTA2MzI2MTMxMDM0NjIiIHdpZHRoPSI1ODYuNzM4MzYwNzU0NjkzNSIgaGVpZ2h0PSI0MjguMjEyNjUyMjYyMDY5MjQiPgogIDwhLS0gc3ZnLXNvdXJjZTpleGNhbGlkcmF3IC0tPgogIAogIDxkZWZzPgogICAgPHN0eWxlIGNsYXNzPSJzdHlsZS1mb250cyI+CiAgICAgIAogICAgPC9zdHlsZT4KICAgIAogIDwvZGVmcz4KICA8ZyBzdHJva2UtbGluZWNhcD0icm91bmQiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEwIDEwKSByb3RhdGUoMCAxMzYuNjg0NTkwMTg4NjczMzggOTcuMDUzMTYzMDY1NTE3MzEpIj48cGF0aCBkPSJNMzIgMCBDMTA5LjY4IDAsIDE4Ny4zNiAwLCAyNDEuMzcgMCBNMzIgMCBDOTAuMTggMCwgMTQ4LjM2IDAsIDI0MS4zNyAwIE0yNDEuMzcgMCBDMjYyLjcgMCwgMjczLjM3IDEwLjY3LCAyNzMuMzcgMzIgTTI0MS4zNyAwIEMyNjIuNyAwLCAyNzMuMzcgMTAuNjcsIDI3My4zNyAzMiBNMjczLjM3IDMyIEMyNzMuMzcgODEuMjMsIDI3My4zNyAxMzAuNDYsIDI3My4zNyAxNjIuMTEgTTI3My4zNyAzMiBDMjczLjM3IDgwLjM1LCAyNzMuMzcgMTI4LjcxLCAyNzMuMzcgMTYyLjExIE0yNzMuMzcgMTYyLjExIEMyNzMuMzcgMTgzLjQ0LCAyNjIuNyAxOTQuMTEsIDI0MS4zNyAxOTQuMTEgTTI3My4zNyAxNjIuMTEgQzI3My4zNyAxODMuNDQsIDI2Mi43IDE5NC4xMSwgMjQxLjM3IDE5NC4xMSBNMjQxLjM3IDE5NC4xMSBDMTg3Ljc2IDE5NC4xMSwgMTM0LjE0IDE5NC4xMSwgMzIgMTk0LjExIE0yNDEuMzcgMTk0LjExIEMxODYuMjggMTk0LjExLCAxMzEuMTkgMTk0LjExLCAzMiAxOTQuMTEgTTMyIDE5NC4xMSBDMTAuNjcgMTk0LjExLCAwIDE4My40NCwgMCAxNjIuMTEgTTMyIDE5NC4xMSBDMTAuNjcgMTk0LjExLCAwIDE4My40NCwgMCAxNjIuMTEgTTAgMTYyLjExIEMwIDEyMi41NiwgMCA4My4wMiwgMCAzMiBNMCAxNjIuMTEgQzAgMTM1LjIxLCAwIDEwOC4zMiwgMCAzMiBNMCAzMiBDMCAxMC42NywgMTAuNjcgMCwgMzIgMCBNMCAzMiBDMCAxMC42NywgMTAuNjcgMCwgMzIgMCIgc3Ryb2tlPSIjMWUxZTFlIiBzdHJva2Utd2lkdGg9IjQiIGZpbGw9Im5vbmUiPjwvcGF0aD48L2c+PGcgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzNS41MDgwMDc3ODUyOTM1NiAzOS43ODI1MTg2ODkzNDY5NDQpIHJvdGF0ZSgwIDY1Ljc1MzEwMjMxNTQ2NyA2NS43NTMxMDIzMTU0NjcpIj48cGF0aCBkPSJNMTMxLjUxIDY1Ljc1IEMxMzEuNTEgNjguMzksIDEzMS4zNSA3MS4wNiwgMTMxLjAzIDczLjY4IEMxMzAuNzEgNzYuMywgMTMwLjIzIDc4LjkyLCAxMjkuNiA4MS40OSBDMTI4Ljk2IDg0LjA1LCAxMjguMTcgODYuNiwgMTI3LjIzIDg5LjA3IEMxMjYuMyA5MS41NCwgMTI1LjIgOTMuOTcsIDEyMy45NyA5Ni4zMSBDMTIyLjc1IDk4LjY1LCAxMjEuMzcgMTAwLjkzLCAxMTkuODcgMTAzLjExIEMxMTguMzcgMTA1LjI4LCAxMTYuNzIgMTA3LjM4LCAxMTQuOTcgMTA5LjM2IEMxMTMuMjIgMTExLjMzLCAxMTEuMzMgMTEzLjIyLCAxMDkuMzYgMTE0Ljk3IEMxMDcuMzggMTE2LjcyLCAxMDUuMjggMTE4LjM3LCAxMDMuMTEgMTE5Ljg3IEMxMDAuOTMgMTIxLjM3LCA5OC42NSAxMjIuNzUsIDk2LjMxIDEyMy45NyBDOTMuOTcgMTI1LjIsIDkxLjU0IDEyNi4zLCA4OS4wNyAxMjcuMjMgQzg2LjYgMTI4LjE3LCA4NC4wNSAxMjguOTYsIDgxLjQ5IDEyOS42IEM3OC45MiAxMzAuMjMsIDc2LjMgMTMwLjcxLCA3My42OCAxMzEuMDMgQzcxLjA2IDEzMS4zNSwgNjguMzkgMTMxLjUxLCA2NS43NSAxMzEuNTEgQzYzLjExIDEzMS41MSwgNjAuNDUgMTMxLjM1LCA1Ny44MyAxMzEuMDMgQzU1LjIgMTMwLjcxLCA1Mi41OCAxMzAuMjMsIDUwLjAyIDEyOS42IEM0Ny40NSAxMjguOTYsIDQ0LjkxIDEyOC4xNywgNDIuNDQgMTI3LjIzIEMzOS45NyAxMjYuMywgMzcuNTQgMTI1LjIsIDM1LjIgMTIzLjk3IEMzMi44NiAxMjIuNzUsIDMwLjU4IDEyMS4zNywgMjguNCAxMTkuODcgQzI2LjIzIDExOC4zNywgMjQuMTMgMTE2LjcyLCAyMi4xNSAxMTQuOTcgQzIwLjE3IDExMy4yMiwgMTguMjkgMTExLjMzLCAxNi41NCAxMDkuMzYgQzE0Ljc4IDEwNy4zOCwgMTMuMTQgMTA1LjI4LCAxMS42NCAxMDMuMTEgQzEwLjE0IDEwMC45MywgOC43NiA5OC42NSwgNy41MyA5Ni4zMSBDNi4zIDkzLjk3LCA1LjIxIDkxLjU0LCA0LjI3IDg5LjA3IEMzLjM0IDg2LjYsIDIuNTQgODQuMDUsIDEuOTEgODEuNDkgQzEuMjggNzguOTIsIDAuOCA3Ni4zLCAwLjQ4IDczLjY4IEMwLjE2IDcxLjA2LCAwIDY4LjM5LCAwIDY1Ljc1IEMwIDYzLjExLCAwLjE2IDYwLjQ1LCAwLjQ4IDU3LjgzIEMwLjggNTUuMiwgMS4yOCA1Mi41OCwgMS45MSA1MC4wMiBDMi41NCA0Ny40NSwgMy4zNCA0NC45MSwgNC4yNyA0Mi40NCBDNS4yMSAzOS45NywgNi4zIDM3LjU0LCA3LjUzIDM1LjIgQzguNzYgMzIuODYsIDEwLjE0IDMwLjU4LCAxMS42NCAyOC40IEMxMy4xNCAyNi4yMywgMTQuNzggMjQuMTMsIDE2LjU0IDIyLjE1IEMxOC4yOSAyMC4xNywgMjAuMTcgMTguMjksIDIyLjE1IDE2LjU0IEMyNC4xMyAxNC43OCwgMjYuMjMgMTMuMTQsIDI4LjQgMTEuNjQgQzMwLjU4IDEwLjE0LCAzMi44NiA4Ljc2LCAzNS4yIDcuNTMgQzM3LjU0IDYuMywgMzkuOTcgNS4yMSwgNDIuNDQgNC4yNyBDNDQuOTEgMy4zNCwgNDcuNDUgMi41NCwgNTAuMDIgMS45MSBDNTIuNTggMS4yOCwgNTUuMiAwLjgsIDU3LjgzIDAuNDggQzYwLjQ1IDAuMTYsIDYzLjExIDAsIDY1Ljc1IDAgQzY4LjM5IDAsIDcxLjA2IDAuMTYsIDczLjY4IDAuNDggQzc2LjMgMC44LCA3OC45MiAxLjI4LCA4MS40OSAxLjkxIEM4NC4wNSAyLjU0LCA4Ni42IDMuMzQsIDg5LjA3IDQuMjcgQzkxLjU0IDUuMjEsIDkzLjk3IDYuMywgOTYuMzEgNy41MyBDOTguNjUgOC43NiwgMTAwLjkzIDEwLjE0LCAxMDMuMTEgMTEuNjQgQzEwNS4yOCAxMy4xNCwgMTA3LjM4IDE0Ljc4LCAxMDkuMzYgMTYuNTQgQzExMS4zMyAxOC4yOSwgMTEzLjIyIDIwLjE3LCAxMTQuOTcgMjIuMTUgQzExNi43MiAyNC4xMywgMTE4LjM3IDI2LjIzLCAxMTkuODcgMjguNCBDMTIxLjM3IDMwLjU4LCAxMjIuNzUgMzIuODYsIDEyMy45NyAzNS4yIEMxMjUuMiAzNy41NCwgMTI2LjMgMzkuOTcsIDEyNy4yMyA0Mi40NCBDMTI4LjE3IDQ0LjkxLCAxMjguOTYgNDcuNDUsIDEyOS42IDUwLjAyIEMxMzAuMjMgNTIuNTgsIDEzMC43MSA1NS4yLCAxMzEuMDMgNTcuODMgQzEzMS4zNSA2MC40NSwgMTMxLjUxIDYzLjExLCAxMzEuNTEgNjUuNzUiIHN0cm9rZT0iIzFlMWUxZSIgc3Ryb2tlLXdpZHRoPSI0IiBmaWxsPSJub25lIj48L3BhdGg+PC9nPjwvc3ZnPg==
```

</details>
