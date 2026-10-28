# Isekai Cheat: authorship and content review

Release date: 2026-10-28. Dataset: `isekai-cheat-data.json`, schema version 1.

## Provenance

All 24 ability scenarios, activation rules, limitations, costs, first-use scenes, and two-sentence stories were composed for this release with AI assistance. The Korean, English, Spanish, Simplified Chinese, Japanese, German, French, and Portuguese versions were authored together as localized fictional game content. They are not adaptations of an existing quiz, book, film, comic, or game. Familiar fantasy mechanisms are combined here with newly written rules, practical situations, and consequences; no claim is made to ownership of a general fantasy idea.

The dataset contains no factual historical or demographic claims requiring citations. `sources` and every entry's `sourceIds` are therefore empty arrays. These empty arrays mean original fiction with no cited external material, rather than missing factual research. No source URLs or third-party licenses are fabricated.

No external text excerpts or visual assets are included in these two content files. Art data consists of approved colors and renderer enum values for an original code-drawn `magic` illustration. Actual SVG implementation and deployment verification belong to the shared renderer and release workflow.

## Game weights

Weights are authored gameplay values, not measured frequencies, real-world probabilities, predictions, or a ranking of users. There are 24 positive integer weights with a total of **186**. The base chance of a result is its weight divided by 186. The runtime must explain that excluding the current result on redraw changes the conditional probabilities. This note is translated into every supported language in the dataset.

## Localized original-fiction notices

| Language | Notice |
| --- | --- |
| 한국어 | 모든 능력과 이야기는 이 게임을 위해 직접 만든 가상 설정입니다. 확률은 제작자가 정한 게임용 가중치이며 실제 운명이나 능력과 무관합니다. |
| English | Every ability and story is original fiction written for this game. Probabilities use authored game weights and do not predict real fate or abilities. |
| Español | Todos los poderes y relatos son ficción original creada para este juego. Las probabilidades son pesos de juego definidos por el autor y no predicen el destino ni habilidades reales. |
| 简体中文 | 所有能力与故事均为本游戏创作的原创虚构内容。概率采用作者设定的游戏权重，与真实命运或能力无关。 |
| 日本語 | すべての能力と物語は、このゲームのために作った独自の架空設定です。確率は制作者が決めたゲーム用の重みで、現実の運命や能力とは無関係です。 |
| Deutsch | Alle Fähigkeiten und Geschichten sind eigens für dieses Spiel erfundene Fiktion. Die Wahrscheinlichkeiten beruhen auf festgelegten Spielgewichten und sagen nichts über echtes Schicksal oder Können aus. |
| Français | Tous les pouvoirs et récits sont des fictions originales écrites pour ce jeu. Les probabilités reposent sur des poids de jeu choisis par l’auteur et ne prédisent ni destin ni capacités réelles. |
| Português | Todos os poderes e histórias são ficção original criada para este jogo. As probabilidades usam pesos de jogo definidos pelo autor e não preveem destino ou habilidades reais. |

## Content inventory

Every listed entry provides the same five localized fields: `capability`, `condition`, `limit`, `drawback`, and `firstUse`. Each also provides a localized name, blurb, and independent two-sentence scene.

| Stable result ID | Korean name | Weight |
| --- | --- | ---: |
| pocket-pantry | 주머니 식품창고 | 12 |
| minute-mender | 5분 수리 | 10 |
| shadow-stairs | 그림자 계단 | 9 |
| honest-compass | 솔직한 나침반 | 8 |
| rain-receipt | 빗물 영수증 | 11 |
| talking-soup | 말하는 수프 | 7 |
| spare-door | 임시 연결문 | 6 |
| gravity-apron | 중력 앞치마 | 10 |
| sunrise-coupon | 일출 교환권 | 8 |
| polite-thunder | 공손한 천둥 | 5 |
| left-sock-porter | 왼쪽 양말 조수 | 9 |
| quilt-bridge | 이불 다리 | 7 |
| message-snail | 쪽지 달팽이 | 8 |
| breadcrumb-map | 빵가루 지도 | 10 |
| quiet-bell | 소음 보관 종 | 7 |
| rust-garden | 녹 정원 | 6 |
| scent-thread | 냄새 실 | 9 |
| margin-accountant | 여백 계산사 | 10 |
| puddle-window | 물웅덩이 창 | 6 |
| compliment-cushion | 칭찬 쿠션 | 7 |
| rain-pause | 10초 빗방울 정지 | 3 |
| parcel-bubble | 소포 거품 | 8 |
| beast-interpreter | 동물 통역 귀 | 6 |
| provisional-wall | 임시 벽 | 4 |

## Review scope

Content review checked the eight language versions for the same ability mechanics, activation conditions, numerical boundaries, costs, and first-use events. A wording pass aligned the compass's scope to any previously touched personal possession and refined Korean and Spanish phrasing. Each story contains two sentences and extends the field information with a specific action and a consequence.

Automated validation is run through the workspace's explicit RTK executable. It checks JSON parsing, the required eight languages, unique stable IDs, positive integer weights, the five matching field keys, nonempty localized content, localized non-English text, two-sentence stories, allowed art values, and absence of embedded markup or remote assets. This review does not establish runtime behavior, browser appearance, sharing behavior, deployment, or production availability.

Validation result on 2026-10-28: **PASS**, using `.tools/rtk/rtk.exe test node -` and an explicit `.tools/rtk/rtk.exe bypass node -` readback. The final dataset has 24 entries, 8 languages, 960 localized field values, 192 two-sentence stories, 24 distinct art configurations, and weight total 186. An additional language check confirmed that every non-English field differs from its English counterpart and that Latin-script translations do not contain untranslated Korean, Japanese, or Chinese text.
