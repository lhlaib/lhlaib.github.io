---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-01-05
type: landing

design:
  # Default section spacing
  spacing: '0'

sections:
  # Developer Hero - Gradient background with name, role, social, and CTAs
  - block: dev-hero
    id: hero
    content:
      username: me-zh
      greeting: "您好，我是"
      show_status: true
      show_scroll_indicator: true
      typewriter:
        enable: true
        prefix: "我以溫潤而穿透的女中音"
        strings:
          - "在歌劇舞台塑造角色"
          - "以語意詮釋藝術歌曲"
          - "與交響／管樂精準合作"
          - "讓作品被聽見、被相信"
        type_speed: 70
        delete_speed: 40
        pause_time: 2500
      cta_buttons:
        - text: 觀看精選演出
          url: "#performances"
          icon: arrow-down
        - text: 邀演／合作洽詢
          url: "#contact"
          icon: envelope
    design:
      style: centered
      avatar_shape: circle
      animations: true
      background:
        color:
          light: "#fafafa"
          dark: "#0a0a0f"
      spacing:
        padding: ["6rem", "0", "4rem", "0"]

  # Filterable Portfolio - Alpine.js powered project filtering
  - block: portfolio
    id: performances
    content:
      title: "精選演出"
      subtitle: "歌劇｜音樂會｜合作演出｜競賽亮點"
      count: 0
      filters:
        folders:
          - performances
      buttons:
        - name: 全部
          tag: '*'
        - name: 歌劇
          tag: 歌劇
        - name: 音樂會
          tag: 音樂會
        - name: 藝術歌曲
          tag: 藝術歌曲
        - name: 合作演出
          tag: 合作演出
        - name: 競賽
          tag: 競賽
      default_button_index: 0
      # Archive link auto-shown if more projects exist than 'count' above
      # archive:
      #   enable: false  # Set to false to explicitly hide
      #   text: "瀏覽全部"  # Customize text
      #   link: "/work/"  # Custom URL
    design:
      columns: 3
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # Visual Tech Stack - Icons organized by category
  - block: tech-stack
    id: skills
    content:
      title: "核心曲目與合作能力"
      subtitle: "以作品為本，兼具舞台表達與合奏敏感度"
      categories:
        - name: 曲目領域
          items:
            - name: 歌劇角色詮釋
              icon: hero/mask
            - name: 藝術歌曲（語意與詩句）
              icon: hero/chat-bubble-left-right
            - name: 音樂會獨唱
              icon: hero/musical-note
            - name: 合唱／歌隊
              icon: hero/users
        - name: 舞台合作
          items:
            - name: 交響樂團合作
              icon: hero/building-library
            - name: 管樂團合作
              icon: hero/bolt
            - name: 排練效率與紀律
              icon: hero/clipboard-document-check
            - name: 製作流程適應力
              icon: hero/cog-6-tooth
        - name: 表演特質
          items:
            - name: 音色厚度與穿透
              icon: hero/sparkles
            - name: 長線條與呼吸支撐
              icon: hero/arrow-trending-up
            - name: 角色驅動聲線
              icon: hero/fire
            - name: 舞台穩定度
              icon: hero/shield-check
    design:
      style: grid
      show_levels: false
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # Experience Timeline
  - block: resume-experience
    id: experience
    content:
      username: me-zh   
      title: 獲獎與競賽亮點
      date_format: Jan 2006
    
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]



  # Recent Blog Posts
  - block: collection
    id: blog
    content:
      title: 最新消息
      subtitle: '演出預告｜活動紀錄｜近期動態'
      text: ''
      filters:
        folders:
          - blog
        exclude_featured: false
      count: 3
      order: desc
    design:
      view: card
      columns: 3
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # Contact Section
  - block: contact-info
    id: contact
    content:
      username: me-zh
      title: 邀演／合作洽詢
      subtitle: "歌劇製作｜音樂會與藝文活動｜校園與機構邀演｜媒體合作"
      text: |-
        我重視每一次登台的品質與作品的完整呈現。
        若您有節目策劃、演出邀約、試唱需求或合作企劃，歡迎來信聯繫。
        
        我可提供演出簡介、曲目單、影片連結與排練需求資訊，並與指揮／伴奏／製作團隊快速對齊音樂方向。
      email: lynn132427@gmail.com
      autolink: true
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # CTA Card
  - block: cta-card
    content:
      title: "下載演出簡介（PDF）"
      text: |-
        若您正在規劃節目、試唱或邀演合作，這份演出簡介可協助您快速掌握我的學習背景、舞台經驗與競賽成績。
        
        我也很樂意依節目需求提供曲目建議與排練資訊。
      button:
        text: '下載 PDF'
        url: uploads/簡介.pdf
        new_tab: true
    design:
      card:
        # Light mode: soft pastel theme gradient | Dark mode: rich deep gradient
        css_class: 'bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700'
        text_color: dark
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "6rem", "0"]
---