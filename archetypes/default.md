+++
title = '{{ replace .File.ContentBaseName "-" " " | title }}'
date = {{ .Date }}
draft = true
tags = []
unique_id = "{{ .File.UniqueID }}"
aliases = ["{{.File.UniqueID}}"]
+++
