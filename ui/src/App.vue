<template>
  <!-- eslint-disable max-len -->
  <main class="container">
    <div class="columns mt-3">
      <div class="col-12 mt-3 text-center">
        <img width="280px" alt="ElegantOTA" src="data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiIHN0YW5kYWxvbmU9Im5vIj8+CjxzdmcKICAgeG1sbnM6ZGM9Imh0dHA6Ly9wdXJsLm9yZy9kYy9lbGVtZW50cy8xLjEvIgogICB4bWxuczpjYz0iaHR0cDovL2NyZWF0aXZlY29tbW9ucy5vcmcvbnMjIgogICB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiCiAgIHhtbG5zOnN2Zz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciCiAgIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIKICAgeG1sbnM6c29kaXBvZGk9Imh0dHA6Ly9zb2RpcG9kaS5zb3VyY2Vmb3JnZS5uZXQvRFREL3NvZGlwb2RpLTAuZHRkIgogICB4bWxuczppbmtzY2FwZT0iaHR0cDovL3d3dy5pbmtzY2FwZS5vcmcvbmFtZXNwYWNlcy9pbmtzY2FwZSIKICAgdmVyc2lvbj0iMS4xIgogICBpZD0iTGF5ZXJfMSIKICAgeD0iMHB4IgogICB5PSIwcHgiCiAgIHZpZXdCb3g9IjAgMCAyNTQgODMiCiAgIHN0eWxlPSJlbmFibGUtYmFja2dyb3VuZDpuZXcgMCAwIDI1NCA4MzsiCiAgIHNvZGlwb2RpOmRvY25hbWU9ImxvZ28uc3ZnIgogICBpbmtzY2FwZTp2ZXJzaW9uPSIwLjkyLjQgKDVkYTY4OWMzMTMsIDIwMTktMDEtMTQpIj4KICA8bWV0YWRhdGEKICAgICBpZD0ibWV0YWRhdGExNSI+CiAgICA8cmRmOlJERj4KICAgICAgPGNjOldvcmsKICAgICAgICAgcmRmOmFib3V0PSIiPgogICAgICAgIDxkYzpmb3JtYXQ+aW1hZ2Uvc3ZnK3htbDwvZGM6Zm9ybWF0PgogICAgICAgIDxkYzp0eXBlCiAgICAgICAgICAgcmRmOnJlc291cmNlPSJodHRwOi8vcHVybC5vcmcvZGMvZGNtaXR5cGUvU3RpbGxJbWFnZSIgLz4KICAgICAgICA8ZGM6dGl0bGU+PC9kYzp0aXRsZT4KICAgICAgPC9jYzpXb3JrPgogICAgPC9yZGY6UkRGPgogIDwvbWV0YWRhdGE+CiAgPGRlZnMKICAgICBpZD0iZGVmczEzIiAvPgogIDxzb2RpcG9kaTpuYW1lZHZpZXcKICAgICBwYWdlY29sb3I9IiNmZmZmZmYiCiAgICAgYm9yZGVyY29sb3I9IiM2NjY2NjYiCiAgICAgYm9yZGVyb3BhY2l0eT0iMSIKICAgICBvYmplY3R0b2xlcmFuY2U9IjEwIgogICAgIGdyaWR0b2xlcmFuY2U9IjEwIgogICAgIGd1aWRldG9sZXJhbmNlPSIxMCIKICAgICBpbmtzY2FwZTpwYWdlb3BhY2l0eT0iMCIKICAgICBpbmtzY2FwZTpwYWdlc2hhZG93PSIyIgogICAgIGlua3NjYXBlOndpbmRvdy13aWR0aD0iMTkyMCIKICAgICBpbmtzY2FwZTp3aW5kb3ctaGVpZ2h0PSIxMDE3IgogICAgIGlkPSJuYW1lZHZpZXcxMSIKICAgICBzaG93Z3JpZD0iZmFsc2UiCiAgICAgaW5rc2NhcGU6em9vbT0iMy45NzUzODc3IgogICAgIGlua3NjYXBlOmN4PSIxMTUuNDMzNTUiCiAgICAgaW5rc2NhcGU6Y3k9IjEwLjMyNDIzIgogICAgIGlua3NjYXBlOndpbmRvdy14PSItOCIKICAgICBpbmtzY2FwZTp3aW5kb3cteT0iLTgiCiAgICAgaW5rc2NhcGU6d2luZG93LW1heGltaXplZD0iMSIKICAgICBpbmtzY2FwZTpjdXJyZW50LWxheWVyPSJMYXllcl8xIiAvPgogIDxzdHlsZQogICAgIHR5cGU9InRleHQvY3NzIgogICAgIGlkPSJzdHlsZTIiPgoJLnN0MHtmaWxsOiMyRTMwMzQ7fQoJLnN0MXtmaWxsOiM0ODhFRkY7fQo8L3N0eWxlPgogIDxwYXRoCiAgICAgc3R5bGU9ImZpbGw6IzQ4OGVmZjtzdHJva2Utd2lkdGg6MC4yMjU1MjA1NyIKICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgIGlkPSJwYXRoNyIKICAgICBkPSJtIDYxLjM1OTY5MiwzOC42MjY3OSBjIDEuMjg1NDY3LDAgMS43NTkwNiwxLjQ4ODQzNiAxLjAxNDg0MiwyLjQzNTYyMiAtMS42MjM3NDgsMS44OTQzNzMgLTMuMjQ3NDk2LDMuNzIxMDg5IC00Ljg3MTI0NCw1LjYxNTQ2MiAtMC40NzM1OTMsMC41NDEyNSAtMS40ODg0MzYsMC41NDEyNSAtMi4wMjk2ODUsMCAtMS42MjM3NDgsLTEuODk0MzczIC0zLjI0NzQ5NiwtMy43MjEwODkgLTQuODcxMjQ0LC01LjYxNTQ2MiAtMS4wMTQ4NDMsLTEuMTUwMTU1IDAuMjcwNjI0LC0yLjc3MzkwMyAxLjQyMDc3OSwtMi40MzU2MjIgaCAyLjk3Njg3MiBDIDUzLjM3NjI2NCwzMi4xMzE3OTcgNDguNDM3MzYzLDI2Ljc4Njk2IDQxLjczOTQwMiwyNS4yOTg1MjQgNDAuNDUzOTM1LDI1LjAyNzg5OSAzOS4xNjg0NjgsMjQuODkyNTg3IDM3Ljg4MywyNC44OTI1ODcgYyAtNi40OTQ5OTIsMCAtMTIuNTE2MzkxLDMuNTg1Nzc3IC0xNS42OTYyMzEsOS40NzE4NjQgLTAuODc5NTMsMS42MjM3NDggLTMuMzE1MTUzLDAuMjAyOTY5IC0yLjQzNTYyMiwtMS40MjA3NzkgNC4zMjk5OTUsLTcuODQ4MTE2IDEzLjM5NTkyMiwtMTIuMzgxMDggMjIuMjU4ODgsLTEwLjQxOTA1MSA3Ljk4MzQyOCwxLjY5MTQwNCAxNC4yMDc3OTYsOC4xMTg3NDEgMTUuODMxNTQ0LDE2LjEwMjE2OSAwLDAgMy41MTgxMjEsMCAzLjUxODEyMSwwIHogbSAtNDUuNjAwMjU5LDguNjU5OTkgYyAtMS4yODU0NjgsMCAtMS43NTkwNjEsLTEuNDg4NDM2IC0xLjAxNDg0MywtMi40MzU2MjIgMS42MjM3NDgsLTEuODk0MzczIDMuMjQ3NDk2LC0zLjcyMTA5IDQuODcxMjQ0LC01LjYxNTQ2MyAwLjQ3MzU5NCwtMC41NDEyNDkgMS40ODg0MzYsLTAuNTQxMjQ5IDIuMDI5Njg1LDAgMS42MjM3NDksMS44OTQzNzMgMy4yNDc0OTcsMy43MjEwOSA0Ljg3MTI0NSw1LjYxNTQ2MyAxLjAxNDg0MiwxLjE1MDE1NSAtMC4yNzA2MjUsMi43NzM5MDMgLTEuNDIwNzgsMi40MzU2MjIgaCAtMi45NzY4NzEgYyAxLjYyMzc0OCw2LjQ5NDk5MiA2LjU2MjY0OCwxMS44Mzk4MyAxMy4yNjA2MDksMTMuMzI4MjY1IDEuMjg1NDY3LDAuMjcwNjI1IDIuNTcwOTM1LDAuNDA1OTM3IDMuODU2NDAyLDAuNDA1OTM3IDYuNDk0OTkyLDAgMTIuNTE2MzkyLC0zLjU4NTc3NyAxNS42OTYyMzIsLTkuNDcxODYzIDAuODc5NTMsLTEuNjIzNzQ5IDMuMzE1MTUyLC0wLjIwMjk2OSAyLjQzNTYyMiwxLjQyMDc3OSBDIDUzLjAzNzk4Myw2MC44ODU2NyA0My45NzIwNTYsNjUuNDE4NjM0IDM1LjEwOTA5Nyw2My40NTY2MDUgMjcuMTI1NjY5LDYxLjY5NzU0NCAyMC44MzM2NDUsNTUuMjcwMjA4IDE5LjIwOTg5Nyw0Ny4yODY3OCBaIgogICAgIGNsYXNzPSJzdDEiIC8+CiAgPHBhdGgKICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgIGlkPSJwYXRoODI5IgogICAgIHN0eWxlPSJmb250LXN0eWxlOm5vcm1hbDtmb250LXZhcmlhbnQ6bm9ybWFsO2ZvbnQtd2VpZ2h0OjMwMDtmb250LXN0cmV0Y2g6bm9ybWFsO2ZvbnQtc2l6ZToyNy42NDc4NTM4NXB4O2xpbmUtaGVpZ2h0OjEuMjU7Zm9udC1mYW1pbHk6TW9udHNlcnJhdDstaW5rc2NhcGUtZm9udC1zcGVjaWZpY2F0aW9uOidNb250c2VycmF0IExpZ2h0JztsZXR0ZXItc3BhY2luZzotMC43NDIxMjQ1NnB4O3dvcmQtc3BhY2luZzowcHg7ZmlsbDojMmUzMDM0O2ZpbGwtb3BhY2l0eToxO3N0cm9rZTpub25lO3N0cm9rZS13aWR0aDowLjk5OTk5OTk0IgogICAgIGQ9Im0gODAuMzEzNDkzLDUxLjc4NDQ2IHEgLTIuODQ3NzI5LDAgLTUuMTQyNTAxLC0xLjI3MTgwMSAtMi4yOTQ3NzIsLTEuMjk5NDQ5IC0zLjYyMTg2OSwtMy41Mzg5MjUgLTEuMjk5NDQ5LC0yLjIzOTQ3NiAtMS4yOTk0NDksLTUuMDA0MjYyIDAsLTIuNzY0Nzg1IDEuMjk5NDQ5LC01LjAwNDI2MSAxLjMyNzA5NywtMi4yMzk0NzYgMy42MjE4NjksLTMuNTExMjc4IDIuMjk0NzcyLC0xLjI5OTQ0OSA1LjE0MjUwMSwtMS4yOTk0NDkgMi44NDc3MjksMCA1LjE0MjUwMSwxLjI3MTgwMSAyLjI5NDc3MiwxLjI3MTgwMiAzLjU5NDIyMSwzLjUxMTI3OCAxLjMyNzA5NywyLjIzOTQ3NiAxLjMyNzA5Nyw1LjAzMTkwOSAwLDIuNzkyNDM0IC0xLjMyNzA5Nyw1LjAzMTkxIC0xLjI5OTQ0OSwyLjIzOTQ3NiAtMy41OTQyMjEsMy41MTEyNzcgLTIuMjk0NzcyLDEuMjcxODAxIC01LjE0MjUwMSwxLjI3MTgwMSB6IG0gMCwtMS4yOTk0NDkgcSAyLjQzMzAxMSwwIDQuMzk2MDA5LC0xLjEwNTkxNCAxLjk2Mjk5NywtMS4xMDU5MTQgMy4wOTY1NTksLTMuMDQxMjY0IDEuMTMzNTYyLC0xLjk2Mjk5NyAxLjEzMzU2MiwtNC4zNjgzNjEgMCwtMi40MDUzNjMgLTEuMTMzNTYyLC00LjM0MDcxMyAtMS4xMzM1NjIsLTEuOTYyOTk3IC0zLjA5NjU1OSwtMy4wNjg5MTIgLTEuOTYyOTk4LC0xLjEwNTkxNCAtNC4zOTYwMDksLTEuMTA1OTE0IC0yLjQzMzAxMSwwIC00LjQyMzY1NywxLjEwNTkxNCAtMS45NjI5OTcsMS4xMDU5MTUgLTMuMDk2NTU5LDMuMDY4OTEyIC0xLjEzMzU2MiwxLjkzNTM1IC0xLjEzMzU2Miw0LjM0MDcxMyAwLDIuNDA1MzY0IDEuMTMzNTYyLDQuMzY4MzYxIDEuMTMzNTYyLDEuOTM1MzUgMy4wOTY1NTksMy4wNDEyNjQgMS45OTA2NDYsMS4xMDU5MTQgNC40MjM2NTcsMS4xMDU5MTQgeiIgLz4KICA8cGF0aAogICAgIGlua3NjYXBlOmNvbm5lY3Rvci1jdXJ2YXR1cmU9IjAiCiAgICAgaWQ9InBhdGg4MzEiCiAgICAgc3R5bGU9ImZvbnQtc3R5bGU6bm9ybWFsO2ZvbnQtdmFyaWFudDpub3JtYWw7Zm9udC13ZWlnaHQ6MzAwO2ZvbnQtc3RyZXRjaDpub3JtYWw7Zm9udC1zaXplOjI3LjY0Nzg1Mzg1cHg7bGluZS1oZWlnaHQ6MS4yNTtmb250LWZhbWlseTpNb250c2VycmF0Oy1pbmtzY2FwZS1mb250LXNwZWNpZmljYXRpb246J01vbnRzZXJyYXQgTGlnaHQnO2xldHRlci1zcGFjaW5nOi0wLjc0MjEyNDU2cHg7d29yZC1zcGFjaW5nOjBweDtmaWxsOiMyZTMwMzQ7ZmlsbC1vcGFjaXR5OjE7c3Ryb2tlOm5vbmU7c3Ryb2tlLXdpZHRoOjAuOTk5OTk5OTQiCiAgICAgZD0ibSAxMDEuMzI3MjEsMzcuMTAzNDUgcSAyLjAxODI5LDAgMy42NDk1MSwwLjk0MDAyNyAxLjYzMTIzLDAuOTQwMDI3IDIuNTQzNjEsMi41OTg4OTggMC45NDAwMiwxLjY1ODg3MiAwLjk0MDAyLDMuNzg3NzU2IDAsMi4xMjg4ODUgLTAuOTQwMDIsMy44MTU0MDQgLTAuOTEyMzgsMS42NTg4NzEgLTIuNTQzNjEsMi41OTg4OTggLTEuNjMxMjIsMC45MTIzOCAtMy42NDk1MSwwLjkxMjM4IC0xLjkwNzcwNiwwIC0zLjQ1NTk4NiwtMC44ODQ3MzIgLTEuNTQ4MjgsLTAuOTEyMzc5IC0yLjQwNTM2MywtMi41MTU5NTQgdiA4LjY1Mzc3OCBIIDk0LjA4MzQ2OCBWIDM3LjIxNDA0MSBoIDEuMzI3MDk3IHYgMy40MDA2ODYgcSAwLjg1NzA4NCwtMS42NTg4NzEgMi40MDUzNjQsLTIuNTcxMjUgMS41NzU5MjcsLTAuOTQwMDI3IDMuNTExMjgxLC0wLjk0MDAyNyB6IG0gLTAuMDgyOSwxMy40MDkyMDkgcSAxLjY1ODg3LDAgMi45ODU5NywtMC43NzQxNCAxLjMyNzEsLTAuNzc0MTQgMi4wNzM1OSwtMi4xNTY1MzIgMC43NzQxNCwtMS4zODIzOTMgMC43NzQxNCwtMy4xNTE4NTYgMCwtMS43Njk0NjIgLTAuNzc0MTQsLTMuMTUxODU1IC0wLjc0NjQ5LC0xLjM4MjM5MyAtMi4wNzM1OSwtMi4xNTY1MzMgLTEuMzI3MSwtMC43NzQxNCAtMi45ODU5NywtMC43NzQxNCAtMS42NTg4NjksMCAtMi45ODU5NjYsMC43NzQxNCAtMS4yOTk0NDksMC43NzQxNCAtMi4wNzM1ODksMi4xNTY1MzMgLTAuNzQ2NDkyLDEuMzgyMzkzIC0wLjc0NjQ5MiwzLjE1MTg1NSAwLDEuNzY5NDYzIDAuNzQ2NDkyLDMuMTUxODU2IDAuNzc0MTQsMS4zODIzOTIgMi4wNzM1ODksMi4xNTY1MzIgMS4zMjcwOTcsMC43NzQxNCAyLjk4NTk2NiwwLjc3NDE0IHoiIC8+CiAgPHBhdGgKICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgIGlkPSJwYXRoODMzIgogICAgIHN0eWxlPSJmb250LXN0eWxlOm5vcm1hbDtmb250LXZhcmlhbnQ6bm9ybWFsO2ZvbnQtd2VpZ2h0OjMwMDtmb250LXN0cmV0Y2g6bm9ybWFsO2ZvbnQtc2l6ZToyNy42NDc4NTM4NXB4O2xpbmUtaGVpZ2h0OjEuMjU7Zm9udC1mYW1pbHk6TW9udHNlcnJhdDstaW5rc2NhcGUtZm9udC1zcGVjaWZpY2F0aW9uOidNb250c2VycmF0IExpZ2h0JztsZXR0ZXItc3BhY2luZzotMC43NDIxMjQ1NnB4O3dvcmQtc3BhY2luZzowcHg7ZmlsbDojMmUzMDM0O2ZpbGwtb3BhY2l0eToxO3N0cm9rZTpub25lO3N0cm9rZS13aWR0aDowLjk5OTk5OTk0IgogICAgIGQ9Im0gMTI0LjIxNzk1LDQ0Ljc2MTkwNiBoIC0xMi40MTM4OSBxIDAuMDU1MywxLjY4NjUxOSAwLjg1NzA5LDMuMDEzNjE2IDAuODAxNzgsMS4yOTk0NDkgMi4xNTY1MywyLjAxODI5MyAxLjM4MjM5LDAuNzE4ODQ0IDMuMDk2NTYsMC43MTg4NDQgMS40MTAwNCwwIDIuNTk4OSwtMC40OTc2NjEgMS4yMTY1LC0wLjUyNTMwOSAyLjAxODI5LC0xLjUyMDYzMiBsIDAuODAxNzksMC45MTIzNzkgcSAtMC45NDAwMywxLjEzMzU2MiAtMi4zNzc3MiwxLjc0MTgxNSAtMS40MTAwNCwwLjYwODI1MyAtMy4wNjg5MSwwLjYwODI1MyAtMi4xNTY1MywwIC0zLjg0MzA1LC0wLjk0MDAyNyAtMS42ODY1MiwtMC45NDAwMjcgLTIuNjU0MTksLTIuNTk4ODk5IC0wLjk0MDAzLC0xLjY1ODg3MSAtMC45NDAwMywtMy43ODc3NTYgMCwtMi4xMDEyMzcgMC44ODQ3MywtMy43NjAxMDggMC45MTIzOCwtMS42ODY1MTkgMi40ODgzMSwtMi42MjY1NDYgMS41NzU5MiwtMC45NDAwMjcgMy41Mzg5MiwtMC45NDAwMjcgMS45NjMsMCAzLjUxMTI4LDAuOTQwMDI3IDEuNTc1OTMsMC45MTIzNzkgMi40NjA2NiwyLjU3MTI1IDAuOTEyMzgsMS42NTg4NzIgMC45MTIzOCwzLjc2MDEwOSB6IG0gLTYuODU2NjcsLTYuNDQxOTUgcSAtMS41MjA2MywwIC0yLjczNzE0LDAuNjkxMTk2IC0xLjIxNjUsMC42NjM1NDggLTEuOTYyOTksMS45MDc3MDIgLTAuNzE4ODUsMS4yMTY1MDUgLTAuODI5NDQsMi43NjQ3ODUgaCAxMS4wNTkxNCBxIC0wLjA4MjksLTEuNTQ4MjggLTAuODI5NDMsLTIuNzY0Nzg1IC0wLjc0NjQ5LC0xLjIxNjUwNiAtMS45NjMsLTEuOTA3NzAyIC0xLjIxNjUxLC0wLjY5MTE5NiAtMi43MzcxNCwtMC42OTExOTYgeiIgLz4KICA8cGF0aAogICAgIGlua3NjYXBlOmNvbm5lY3Rvci1jdXJ2YXR1cmU9IjAiCiAgICAgaWQ9InBhdGg4MzUiCiAgICAgc3R5bGU9ImZvbnQtc3R5bGU6bm9ybWFsO2ZvbnQtdmFyaWFudDpub3JtYWw7Zm9udC13ZWlnaHQ6MzAwO2ZvbnQtc3RyZXRjaDpub3JtYWw7Zm9udC1zaXplOjI3LjY0Nzg1Mzg1cHg7bGluZS1oZWlnaHQ6MS4yNTtmb250LWZhbWlseTpNb250c2VycmF0Oy1pbmtzY2FwZS1mb250LXNwZWNpZmljYXRpb246J01vbnRzZXJyYXQgTGlnaHQnO2xldHRlci1zcGFjaW5nOi0wLjc0MjEyNDU2cHg7d29yZC1zcGFjaW5nOjBweDtmaWxsOiMyZTMwMzQ7ZmlsbC1vcGFjaXR5OjE7c3Ryb2tlOm5vbmU7c3Ryb2tlLXdpZHRoOjAuOTk5OTk5OTQiCiAgICAgZD0ibSAxMzQuODU3MjMsMzcuMTAzNDUgcSAyLjcwOTQ5LDAgNC4yODU0MiwxLjU3NTkyOCAxLjU3NTkzLDEuNTc1OTI3IDEuNTc1OTMsNC41MzQyNDggdiA4LjQzMjU5NSBoIC0xLjM4MjM5IHYgLTguMzIyMDA0IHEgMCwtMi40MzMwMTEgLTEuMjQ0MTYsLTMuNzA0ODEyIC0xLjIxNjUsLTEuMjcxODAyIC0zLjQyODMzLC0xLjI3MTgwMiAtMi41NDM2LDAgLTQuMDA4OTQsMS41MjA2MzIgLTEuNDY1MzQsMS41MjA2MzIgLTEuNDY1MzQsNC4wOTE4ODMgdiA3LjY4NjEwMyBoIC0xLjM4MjM5IHYgLTE0LjQzMjE4IGggMS4zMjcxIHYgMy4xMjQyMDggcSAwLjc0NjQ5LC0xLjUyMDYzMiAyLjIxMTgzLC0yLjM3NzcxNSAxLjQ5Mjk4LC0wLjg1NzA4NCAzLjUxMTI3LC0wLjg1NzA4NCB6IiAvPgogIDxwYXRoCiAgICAgaW5rc2NhcGU6Y29ubmVjdG9yLWN1cnZhdHVyZT0iMCIKICAgICBpZD0icGF0aDgzNyIKICAgICBzdHlsZT0iZm9udC1zdHlsZTpub3JtYWw7Zm9udC12YXJpYW50Om5vcm1hbDtmb250LXdlaWdodDozMDA7Zm9udC1zdHJldGNoOm5vcm1hbDtmb250LXNpemU6MjcuNjQ3ODUzODVweDtsaW5lLWhlaWdodDoxLjI1O2ZvbnQtZmFtaWx5Ok1vbnRzZXJyYXQ7LWlua3NjYXBlLWZvbnQtc3BlY2lmaWNhdGlvbjonTW9udHNlcnJhdCBMaWdodCc7bGV0dGVyLXNwYWNpbmc6LTAuNzQyMTI0NTZweDt3b3JkLXNwYWNpbmc6MHB4O2ZpbGw6IzJlMzAzNDtmaWxsLW9wYWNpdHk6MTtzdHJva2U6bm9uZTtzdHJva2Utd2lkdGg6MC45OTk5OTk5NCIKICAgICBkPSJtIDE2NC40NDAwNSw1MS42NDYyMjEgLTAuMDI3NiwtMTYuNTYxMDY0IC04LjEwMDgyLDEzLjk4OTgxNCBoIC0wLjY5MTIgbCAtOC4xMDA4MiwtMTMuOTM0NTE5IHYgMTYuNTA1NzY5IGggLTEuMzgyMzkgViAzMi4yOTI3MjMgaCAxLjE4ODg1IGwgOC42NTM3OCwxNC45NTc0ODkgOC42NTM3OCwtMTQuOTU3NDg5IGggMS4xNjEyMSBsIDAuMDI3NiwxOS4zNTM0OTggeiIgLz4KICA8cGF0aAogICAgIGlua3NjYXBlOmNvbm5lY3Rvci1jdXJ2YXR1cmU9IjAiCiAgICAgaWQ9InBhdGg4MzkiCiAgICAgc3R5bGU9ImZvbnQtc3R5bGU6bm9ybWFsO2ZvbnQtdmFyaWFudDpub3JtYWw7Zm9udC13ZWlnaHQ6MzAwO2ZvbnQtc3RyZXRjaDpub3JtYWw7Zm9udC1zaXplOjI3LjY0Nzg1Mzg1cHg7bGluZS1oZWlnaHQ6MS4yNTtmb250LWZhbWlseTpNb250c2VycmF0Oy1pbmtzY2FwZS1mb250LXNwZWNpZmljYXRpb246J01vbnRzZXJyYXQgTGlnaHQnO2xldHRlci1zcGFjaW5nOi0wLjc0MjEyNDU2cHg7d29yZC1zcGFjaW5nOjBweDtmaWxsOiMyZTMwMzQ7ZmlsbC1vcGFjaXR5OjE7c3Ryb2tlOm5vbmU7c3Ryb2tlLXdpZHRoOjAuOTk5OTk5OTQiCiAgICAgZD0ibSAxNzYuOTk4NzEsNTEuNzU2ODEzIHEgLTIuMDQ1OTQsMCAtMy43MDQ4MiwtMC45NDAwMjcgLTEuNjMxMjIsLTAuOTQwMDI3IC0yLjU3MTI1LC0yLjU5ODg5OSAtMC45NDAwMiwtMS42ODY1MTkgLTAuOTQwMDIsLTMuNzg3NzU2IDAsLTIuMTAxMjM3IDAuOTQwMDIsLTMuNzYwMTA4IDAuOTQwMDMsLTEuNjg2NTE5IDIuNTcxMjUsLTIuNjI2NTQ2IDEuNjU4ODgsLTAuOTQwMDI3IDMuNzA0ODIsLTAuOTQwMDI3IDIuMDQ1OTQsMCAzLjY3NzE2LDAuOTQwMDI3IDEuNjU4ODcsMC45NDAwMjcgMi41OTg5LDIuNjI2NTQ2IDAuOTQwMDMsMS42NTg4NzEgMC45NDAwMywzLjc2MDEwOCAwLDIuMTAxMjM3IC0wLjk0MDAzLDMuNzg3NzU2IC0wLjk0MDAzLDEuNjU4ODcyIC0yLjU5ODksMi41OTg4OTkgLTEuNjMxMjIsMC45NDAwMjcgLTMuNjc3MTYsMC45NDAwMjcgeiBtIDAsLTEuMjQ0MTU0IHEgMS42NTg4NywwIDIuOTU4MzIsLTAuNzc0MTQgMS4zMjcwOSwtMC43NzQxNCAyLjA3MzU5LC0yLjE1NjUzMiAwLjc3NDE0LC0xLjM4MjM5MyAwLjc3NDE0LC0zLjE1MTg1NiAwLC0xLjc2OTQ2MiAtMC43NzQxNCwtMy4xNTE4NTUgLTAuNzQ2NSwtMS4zODIzOTMgLTIuMDczNTksLTIuMTU2NTMzIC0xLjI5OTQ1LC0wLjc3NDE0IC0yLjk1ODMyLC0wLjc3NDE0IC0xLjY1ODg3LDAgLTIuOTg1OTcsMC43NzQxNCAtMS4yOTk0NSwwLjc3NDE0IC0yLjA3MzU5LDIuMTU2NTMzIC0wLjc0NjQ5LDEuMzgyMzkzIC0wLjc0NjQ5LDMuMTUxODU1IDAsMS43Njk0NjMgMC43NDY0OSwzLjE1MTg1NiAwLjc3NDE0LDEuMzgyMzkyIDIuMDczNTksMi4xNTY1MzIgMS4zMjcxLDAuNzc0MTQgMi45ODU5NywwLjc3NDE0IHoiIC8+CiAgPHBhdGgKICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgIGlkPSJwYXRoODQxIgogICAgIHN0eWxlPSJmb250LXN0eWxlOm5vcm1hbDtmb250LXZhcmlhbnQ6bm9ybWFsO2ZvbnQtd2VpZ2h0OjMwMDtmb250LXN0cmV0Y2g6bm9ybWFsO2ZvbnQtc2l6ZToyNy42NDc4NTM4NXB4O2xpbmUtaGVpZ2h0OjEuMjU7Zm9udC1mYW1pbHk6TW9udHNlcnJhdDstaW5rc2NhcGUtZm9udC1zcGVjaWZpY2F0aW9uOidNb250c2VycmF0IExpZ2h0JztsZXR0ZXItc3BhY2luZzotMC43NDIxMjQ1NnB4O3dvcmQtc3BhY2luZzowcHg7ZmlsbDojMmUzMDM0O2ZpbGwtb3BhY2l0eToxO3N0cm9rZTpub25lO3N0cm9rZS13aWR0aDowLjk5OTk5OTk0IgogICAgIGQ9Im0gMTkxLjM4Mzg1LDUxLjc1NjgxMyBxIC0xLjc0MTgyLDAgLTMuMzE3NzUsLTAuNTI1MzEgLTEuNTc1OTIsLTAuNTI1MzA5IC0yLjQ2MDY1LC0xLjMyNzA5NyBsIDAuNjM1OSwtMS4xMDU5MTQgcSAwLjg4NDczLDAuNzQ2NDkyIDIuMjY3MTIsMS4yNDQxNTQgMS40MTAwNCwwLjQ5NzY2MSAyLjkzMDY3LDAuNDk3NjYxIDIuMTg0MTgsMCAzLjIwNzE1LC0wLjcxODg0NCAxLjA1MDYyLC0wLjcxODg0NCAxLjA1MDYyLC0xLjk5MDY0NiAwLC0wLjkxMjM3OSAtMC41ODA2LC0xLjQzNzY4OCAtMC41NTI5NiwtMC41MjUzMDkgLTEuMzgyNCwtMC43NzQxNCAtMC44Mjk0MywtMC4yNDg4MzEgLTIuMjk0NzcsLTAuNTI1MzA5IC0xLjcxNDE2LC0wLjMwNDEyNyAtMi43NjQ3OCwtMC42NjM1NDkgLTEuMDUwNjIsLTAuMzU5NDIyIC0xLjc5NzExLC0xLjE2MTIxIC0wLjc0NjUsLTAuODAxNzg3IC0wLjc0NjUsLTIuMjExODI4IDAsLTEuNzE0MTY3IDEuNDEwMDUsLTIuODIwMDgxIDEuNDM3NjgsLTEuMTMzNTYyIDQuMDY0MjMsLTEuMTMzNTYyIDEuMzgyMzksMCAyLjczNzE0LDAuMzg3MDcgMS4zNTQ3NCwwLjM4NzA3IDIuMjExODMsMS4wMjI5NzEgbCAtMC42MzU5MSwxLjEwNTkxNCBxIC0wLjg4NDczLC0wLjYzNTkwMSAtMi4wMTgyOSwtMC45Njc2NzUgLTEuMTMzNTYsLTAuMzMxNzc0IC0yLjMyMjQyLC0wLjMzMTc3NCAtMi4wMTgyOSwwIC0zLjA0MTI2LDAuNzQ2NDkyIC0xLjAyMjk3LDAuNzQ2NDkyIC0xLjAyMjk3LDEuOTYyOTk3IDAsMC45Njc2NzUgMC41ODA2LDEuNTIwNjMyIDAuNTgwNjEsMC41MjUzMDkgMS40MTAwNCwwLjgwMTc4OCAwLjg1NzA5LDAuMjQ4ODMxIDIuMzc3NzIsMC41NTI5NTcgMS42ODY1MiwwLjMwNDEyNiAyLjcwOTQ5LDAuNjYzNTQ5IDEuMDUwNjIsMC4zMzE3NzQgMS43Njk0NiwxLjEwNTkxNCAwLjcxODg0LDAuNzc0MTQgMC43MTg4NCwyLjEyODg4NCAwLDEuNzk3MTExIC0xLjQ5Mjk4LDIuODc1Mzc3IC0xLjQ5Mjk4LDEuMDc4MjY3IC00LjIwMjQ3LDEuMDc4MjY3IHoiIC8+CiAgPHBhdGgKICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgIGlkPSJwYXRoODQzIgogICAgIHN0eWxlPSJmb250LXN0eWxlOm5vcm1hbDtmb250LXZhcmlhbnQ6bm9ybWFsO2ZvbnQtd2VpZ2h0OjMwMDtmb250LXN0cmV0Y2g6bm9ybWFsO2ZvbnQtc2l6ZToyNy42NDc4NTM4NXB4O2xpbmUtaGVpZ2h0OjEuMjU7Zm9udC1mYW1pbHk6TW9udHNlcnJhdDstaW5rc2NhcGUtZm9udC1zcGVjaWZpY2F0aW9uOidNb250c2VycmF0IExpZ2h0JztsZXR0ZXItc3BhY2luZzotMC43NDIxMjQ1NnB4O3dvcmQtc3BhY2luZzowcHg7ZmlsbDojMmUzMDM0O2ZpbGwtb3BhY2l0eToxO3N0cm9rZTpub25lO3N0cm9rZS13aWR0aDowLjk5OTk5OTk0IgogICAgIGQ9Im0gMjA0LjU2Mjg1LDMyLjIwOTc4IHEgLTIuNzA5NDksMCAtMi43MDk0OSwyLjkwMzAyNSB2IDIuMTAxMjM2IGggNC42MTcxOSB2IDEuMTg4ODU4IGggLTQuNTg5NTQgdiAxMy4yNDMzMjIgaCAtMS4zODIzOSBWIDM4LjQwMjg5OSBoIC0yLjY1NDIgdiAtMS4xODg4NTggaCAyLjY1NDIgdiAtMi4yMTE4MjggcSAwLC0xLjgyNDc1OCAxLjA1MDYyLC0yLjkwMzAyNSAxLjA1MDYxLC0xLjA3ODI2NiAyLjk1ODMyLC0xLjA3ODI2NiAwLjgyOTQzLDAgMS41NzU5MiwwLjI0ODgzMSAwLjc3NDE0LDAuMjIxMTgzIDEuMjcxOCwwLjY5MTE5NiBsIC0wLjU1Mjk1LDEuMDUwNjE5IFEgMjA1LjkxNzYsMzIuMjA5NzggMjA0LjU2Mjg1LDMyLjIwOTc4IFoiIC8+CiAgPHBhdGgKICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgIGlkPSJwYXRoODQ1IgogICAgIHN0eWxlPSJmb250LXN0eWxlOm5vcm1hbDtmb250LXZhcmlhbnQ6bm9ybWFsO2ZvbnQtd2VpZ2h0OjMwMDtmb250LXN0cmV0Y2g6bm9ybWFsO2ZvbnQtc2l6ZToyNy42NDc4NTM4NXB4O2xpbmUtaGVpZ2h0OjEuMjU7Zm9udC1mYW1pbHk6TW9udHNlcnJhdDstaW5rc2NhcGUtZm9udC1zcGVjaWZpY2F0aW9uOidNb250c2VycmF0IExpZ2h0JztsZXR0ZXItc3BhY2luZzotMC43NDIxMjQ1NnB4O3dvcmQtc3BhY2luZzowcHg7ZmlsbDojMmUzMDM0O2ZpbGwtb3BhY2l0eToxO3N0cm9rZTpub25lO3N0cm9rZS13aWR0aDowLjk5OTk5OTk0IgogICAgIGQ9Im0gMjIwLjQ3NDY3LDQ0Ljc2MTkwNiBoIC0xMi40MTM4OCBxIDAuMDU1MywxLjY4NjUxOSAwLjg1NzA4LDMuMDEzNjE2IDAuODAxNzksMS4yOTk0NDkgMi4xNTY1MywyLjAxODI5MyAxLjM4MjM5LDAuNzE4ODQ0IDMuMDk2NTYsMC43MTg4NDQgMS40MTAwNCwwIDIuNTk4OSwtMC40OTc2NjEgMS4yMTY1LC0wLjUyNTMwOSAyLjAxODI5LC0xLjUyMDYzMiBsIDAuODAxNzksMC45MTIzNzkgcSAtMC45NDAwMywxLjEzMzU2MiAtMi4zNzc3MiwxLjc0MTgxNSAtMS40MTAwNCwwLjYwODI1MyAtMy4wNjg5MSwwLjYwODI1MyAtMi4xNTY1MywwIC0zLjg0MzA1LC0wLjk0MDAyNyAtMS42ODY1MiwtMC45NDAwMjcgLTIuNjU0MTksLTIuNTk4ODk5IC0wLjk0MDAzLC0xLjY1ODg3MSAtMC45NDAwMywtMy43ODc3NTYgMCwtMi4xMDEyMzcgMC44ODQ3MywtMy43NjAxMDggMC45MTIzOCwtMS42ODY1MTkgMi40ODgzMSwtMi42MjY1NDYgMS41NzU5MywtMC45NDAwMjcgMy41Mzg5MiwtMC45NDAwMjcgMS45NjMsMCAzLjUxMTI4LDAuOTQwMDI3IDEuNTc1OTMsMC45MTIzNzkgMi40NjA2NiwyLjU3MTI1IDAuOTEyMzgsMS42NTg4NzIgMC45MTIzOCwzLjc2MDEwOSB6IG0gLTYuODU2NjcsLTYuNDQxOTUgcSAtMS41MjA2MywwIC0yLjczNzEzLDAuNjkxMTk2IC0xLjIxNjUxLDAuNjYzNTQ4IC0xLjk2MywxLjkwNzcwMiAtMC43MTg4NSwxLjIxNjUwNSAtMC44Mjk0NCwyLjc2NDc4NSBoIDExLjA1OTE0IHEgLTAuMDgyOSwtMS41NDgyOCAtMC44Mjk0MywtMi43NjQ3ODUgLTAuNzQ2NDksLTEuMjE2NTA2IC0xLjk2MywtMS45MDc3MDIgLTEuMjE2NSwtMC42OTExOTYgLTIuNzM3MTQsLTAuNjkxMTk2IHoiIC8+CiAgPHBhdGgKICAgICBpbmtzY2FwZTpjb25uZWN0b3ItY3VydmF0dXJlPSIwIgogICAgIGlkPSJwYXRoODQ3IgogICAgIHN0eWxlPSJmb250LXN0eWxlOm5vcm1hbDtmb250LXZhcmlhbnQ6bm9ybWFsO2ZvbnQtd2VpZ2h0OjMwMDtmb250LXN0cmV0Y2g6bm9ybWFsO2ZvbnQtc2l6ZToyNy42NDc4NTM4NXB4O2xpbmUtaGVpZ2h0OjEuMjU7Zm9udC1mYW1pbHk6TW9udHNlcnJhdDstaW5rc2NhcGUtZm9udC1zcGVjaWZpY2F0aW9uOidNb250c2VycmF0IExpZ2h0JztsZXR0ZXItc3BhY2luZzotMC43NDIxMjQ1NnB4O3dvcmQtc3BhY2luZzowcHg7ZmlsbDojMmUzMDM0O2ZpbGwtb3BhY2l0eToxO3N0cm9rZTpub25lO3N0cm9rZS13aWR0aDowLjk5OTk5OTk0IgogICAgIGQ9Im0gMjMxLjIyNDU1LDUwLjczMzg0MiBxIC0wLjUyNTMxLDAuNDk3NjYxIC0xLjMyNzEsMC43NzQxNCAtMC43NzQxNCwwLjI0ODgzMSAtMS42MzEyMiwwLjI0ODgzMSAtMS44ODAwNiwwIC0yLjkwMzAzLC0xLjAyMjk3MSAtMS4wMjI5NywtMS4wNTA2MTggLTEuMDIyOTcsLTIuOTAzMDI1IHYgLTkuNDI3OTE4IGggLTIuNjU0MTkgdiAtMS4xODg4NTggaCAyLjY1NDE5IHYgLTMuMTUxODU1IGggMS4zODIzOSB2IDMuMTUxODU1IGggNC41ODk1NSB2IDEuMTg4ODU4IGggLTQuNTg5NTUgdiA5LjI4OTY3OSBxIDAsMS40MTAwNDEgMC42NjM1NSwyLjE1NjUzMyAwLjY5MTIsMC43MTg4NDQgMi4wMTgzLDAuNzE4ODQ0IDEuMzU0NzQsMCAyLjIzOTQ3LC0wLjgwMTc4OCB6IiAvPgo8L3N2Zz4K">
      </div>
      <div class="col-12 p-centered"></div>
      <div class="col-12 mt-3 p-centered" v-if="loading">
        <div class="col-3 col-sm-10 p-centered">
          <div class="loading loading-lg mt-3"></div>
        </div>
      </div>
      <transition name="fade" mode="out-in">
        <div class="col-12 mt-3 pt-2 p-centered" v-if="!loading && !uploading && OTAError !== null" key="error">
          <div class="col-3 col-sm-9 col-md-6 p-centered text-center">
            <svg width="32px" height="32px" style="vertical-align: middle;" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                <rect id="bound" x="0" y="0" width="24" height="24"></rect>
                <circle id="Oval-5" fill="#DF4759" opacity="0.3" cx="12" cy="12" r="10"></circle>
                <rect id="Rectangle-9" fill="#DF4759" x="11" y="7" width="2" height="8" rx="1"></rect>
                <rect id="Rectangle-9-Copy" fill="#DF4759" x="11" y="16" width="2" height="2" rx="1"></rect>
              </g>
            </svg>
            <span style="vertical-align: middle;" class="ml-2"> {{ OTAError }} </span>
            <br>
            <br>
            <div class="mt-3">
              <button class="btn btn-light mr-2" @click="clear">
                <svg xmlns="http://www.w3.org/2000/svg" class="pt-1" width="16px" height="16px" viewBox="0 0 24 24">
                  <g data-name="Layer 2">
                    <g data-name="arrow-back">
                      <rect width="24" height="24" transform="rotate(90 12 12)" opacity="0" />
                      <path
                        fill="currentColor"
                        d="M19 11H7.14l3.63-4.36a1 1 0 1 0-1.54-1.28l-5 6a1.19 1.19 0 0 0-.09.15c0 .05 0 .08-.07.13A1 1 0 0 0 4 12a1 1 0 0 0 .07.36c0 .05 0 .08.07.13a1.19 1.19 0 0 0 .09.15l5 6A1 1 0 0 0 10 19a1 1 0 0 0 .64-.23 1 1 0 0 0 .13-1.41L7.14 13H19a1 1 0 0 0 0-2z" />
                    </g>
                  </g>
                </svg>
                Back
              </button>
              <button class="btn btn-primary ml-2" @click="retryOTA">
                <svg xmlns="http://www.w3.org/2000/svg" class="pt-1" width="16px" height="16px" viewBox="0 0 24 24">
                  <g data-name="Layer 2">
                    <g data-name="refresh">
                      <rect width="24" height="24" opacity="0" />
                      <path
                        fill="currentColor"
                        d="M20.3 13.43a1 1 0 0 0-1.25.65A7.14 7.14 0 0 1 12.18 19 7.1 7.1 0 0 1 5 12a7.1 7.1 0 0 1 7.18-7 7.26 7.26 0 0 1 4.65 1.67l-2.17-.36a1 1 0 0 0-1.15.83 1 1 0 0 0 .83 1.15l4.24.7h.17a1 1 0 0 0 .34-.06.33.33 0 0 0 .1-.06.78.78 0 0 0 .2-.11l.09-.11c0-.05.09-.09.13-.15s0-.1.05-.14a1.34 1.34 0 0 0 .07-.18l.75-4a1 1 0 0 0-2-.38l-.27 1.45A9.21 9.21 0 0 0 12.18 3 9.1 9.1 0 0 0 3 12a9.1 9.1 0 0 0 9.18 9A9.12 9.12 0 0 0 21 14.68a1 1 0 0 0-.7-1.25z" />
                    </g>
                  </g>
                </svg>
                Retry
              </button>
            </div>
          </div>
        </div>
        <div class="col-12 mt-3 pt-2 p-centered" v-else-if="!loading && !uploading && OTASuccess" key="success">
          <div class="col-3 col-sm-9 col-md-6 p-centered text-center">
            <svg width="32px" height="32px" style="vertical-align: middle;" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
              <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                <rect id="bound" x="0" y="0" width="24" height="24"></rect>
                <circle id="Oval-5" fill="#42BA96" opacity="0.3" cx="12" cy="12" r="10"></circle>
                <path d="M16.7689447,7.81768175 C17.1457787,7.41393107 17.7785676,7.39211077 18.1823183,7.76894473 C18.5860689,8.1457787 18.6078892,8.77856757 18.2310553,9.18231825 L11.2310553,16.6823183 C10.8654446,17.0740439 10.2560456,17.107974 9.84920863,16.7592566 L6.34920863,13.7592566 C5.92988278,13.3998345 5.88132125,12.7685345 6.2407434,12.3492086 C6.60016555,11.9298828 7.23146553,11.8813212 7.65079137,12.2407434 L10.4229928,14.616916 L16.7689447,7.81768175 Z" id="Path-92" fill="#42BA96"></path>
              </g>
            </svg>
            <span style="vertical-align: middle;" class="ml-2 mb-2"> OTA Success </span>
            <br>
            <br>
            <button class="btn btn-primary mt-3" @click="clear">
              <svg xmlns="http://www.w3.org/2000/svg" class="pt-1" width="16px" height="16px" viewBox="0 0 24 24">
                <g data-name="Layer 2">
                  <g data-name="arrow-back">
                    <rect width="24" height="24" transform="rotate(90 12 12)" opacity="0" />
                    <path
                      fill="currentColor"
                      d="M19 11H7.14l3.63-4.36a1 1 0 1 0-1.54-1.28l-5 6a1.19 1.19 0 0 0-.09.15c0 .05 0 .08-.07.13A1 1 0 0 0 4 12a1 1 0 0 0 .07.36c0 .05 0 .08.07.13a1.19 1.19 0 0 0 .09.15l5 6A1 1 0 0 0 10 19a1 1 0 0 0 .64-.23 1 1 0 0 0 .13-1.41L7.14 13H19a1 1 0 0 0 0-2z" />
                  </g>
                </g>
              </svg>
              Back
            </button>
          </div>
        </div>
        <div class="col-12 mt-3 p-centered" v-else-if="!loading && !uploading" key="otainput">
          <div class="col-3 col-sm-9 col-md-6 p-centered">
            <div class="form-group pt-2 mt-2">
              <label class="form-radio form-inline mr-2">
                <input type="radio" name="firmwaretype" for="firmwaretype" value="firmware" v-model="type"><i class="form-icon"></i> Firmware
              </label>
              <label class="form-radio form-inline ml-2">
                <input type="radio" name="firmwaretype" for="firmwaretype" value="filesystem" v-model="type"><i class="form-icon"></i> Filesystem
              </label>
            </div>
            <div class="form-group pt-2 mt-3">
              <input class="form-input file-input" type="file" ref="file" accept=".bin,.bin.gz" @change="uploadOTA">
            </div>
          </div>
        </div>
      </transition>
      <transition name="fade" mode="out-in">
        <div class="col-12 mt-3 mb-2 pt-2 p-centered" v-if="!loading && uploading">
          <div class="col-2 mt-3 mb-2 col-sm-7 col-md-4 text-right p-centered">
            <div class="bar mt-3 bar-sm">
              <div class="bar-item tooltip" :data-tooltip="progress+'%'" :style="{ width: progress+'%' }"></div>
            </div>
            <div class="pt-2">{{progress}}%</div>
          </div>
        </div>
      </transition>
      <div class="col-12 mt-3 p-centered"></div>
    </div>
    <transition name="fade" mode="out-in">
      <div class="columns mt-3" v-if="!loading">
        <div class="col-12 text-center">
          <span class="label label-rounded mr-2">{{ deviceData.id }}</span> - <span class="label label-rounded label-primary ml-2">{{ deviceData.hardware }}</span>
        </div>
      </div>
    </transition>
  </main>
</template>

<script>
export default {
  name: 'App',

  data() {
    return {
      loading: true,
      uploading: false,
      progress: 0,
      OTAError: null,
      OTASuccess: false,

      type: 'firmware',
      file: null,
      deviceData: {
        id: null,
        hardware: null,
      },
    };
  },

  methods: {
    fileMD5(file) {
      return new Promise((resolve, reject) => {
        const blobSlice = File.prototype.slice
          || File.prototype.mozSlice || File.prototype.webkitSlice;
        const chunkSize = 2097152; // Read in chunks of 2MB
        const chunks = Math.ceil(file.size / chunkSize);
        const spark = new this.SparkMD5.ArrayBuffer();
        const fileReader = new FileReader();
        let currentChunk = 0;
        let loadNext;

        fileReader.onload = (e) => {
          spark.append(e.target.result); // Append array buffer
          currentChunk += 1;

          if (currentChunk < chunks) {
            loadNext();
          } else {
            const md5 = spark.end();
            resolve(md5);
          }
        };

        fileReader.onerror = (e) => {
          reject(e);
        };

        loadNext = () => {
          const start = currentChunk * chunkSize;
          const end = ((start + chunkSize) >= file.size) ? file.size : start + chunkSize;

          fileReader.readAsArrayBuffer(blobSlice.call(file, start, end));
        };

        loadNext();
      });
    },
    uploadOTA(event) {
      this.uploading = true;
      const formData = new FormData();
      if (event !== null) {
        [this.file] = event.target.files;
      }
      const request = new XMLHttpRequest();

      request.addEventListener('load', () => {
        // request.response will hold the response from the server
        if (request.status === 200) {
          this.OTASuccess = true;
        } else if (request.status !== 500) {
          this.OTAError = `[HTTP ERROR] ${request.statusText}`;
        } else {
          this.OTAError = request.responseText;
        }
        this.uploading = false;
        this.progress = 0;
      });

      // Upload progress
      request.upload.addEventListener('progress', (e) => {
        this.progress = Math.trunc((e.loaded / e.total) * 100);
      });

      request.withCredentials = true;

      this.fileMD5(this.file)
        .then((md5) => {
          formData.append('MD5', md5);
          formData.append(this.type, this.file, this.type);
          request.open('post', '/update');
          request.send(formData);
        })
        .catch(() => {
          this.OTAError = 'Unknown error while upload, check the console for details.';
          this.uploading = false;
          this.progress = 0;
        });
    },

    retryOTA() {
      this.OTAError = null;
      this.OTASuccess = false;
      this.uploadOTA(null);
    },

    clear() {
      this.OTAError = null;
      this.OTASuccess = false;
    },
  },

  mounted() {
    fetch('/update/identity').then(async (response) => {
      if (response.ok) {
        this.deviceData = await response.json();
        this.loading = false;
      }
    });
  },

};
</script>

<style lang="scss">
$primary-color: #488EFF;
// Variables and mixins
@import "~spectre.css/src/variables";
@import "~spectre.css/src/mixins";

/*! Spectre.css v#{$version} | MIT License | github.com/picturepan2/spectre */
// Reset and dependencies
@import "~spectre.css/src/normalize";
@import "~spectre.css/src/base";

// Elements
@import "~spectre.css/src/typography";

@import "~spectre.css/src/labels";
@import "~spectre.css/src/buttons";
@import "~spectre.css/src/tooltips";
@import "~spectre.css/src/cards";
@import "~spectre.css/src/bars";
@import "~spectre.css/src/forms";

@import "~spectre.css/src/layout";

@import "~spectre.css/src/animations";
@import "~spectre.css/src/utilities";

.logo{
  width: 100%;
  max-width: 320px;
}

.card{
  border: 0;
  box-shadow: 0 0.25rem 1rem rgba(48,55,66,.1);
  border-radius: 0.275rem;
}

.label{
  font-size: 0.65rem !important;
}

.file-input{
  border-radius: 0.275rem;
}

.pt-3{
  padding-top: 32px;
}

.mt-3{
  margin-top: 24px;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .25s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
</style>
