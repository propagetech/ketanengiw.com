You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "css/2d33922edeb1ee82074efa8eb58f49ab.css",
    "context": {
      "path": "css/2d33922edeb1ee82074efa8eb58f49ab.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "imgs/0f7126cdce41e410ceb5e51f6d0036ab.webp",
    "context": {
      "refs": [
        {
          "alt": "Diaphragm Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22028688b990529f221cd4a3ddeaa191.webp",
    "context": {
      "refs": [
        {
          "alt": "Air Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2209f0e0c492870fc579e38bacdf515a.webp",
    "context": {
      "refs": [
        {
          "alt": "Plug Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/339080ebdb39722b087d74f1ee518019.webp",
    "context": {
      "refs": [
        {
          "alt": "Our Effective team",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/448978717384f4c175470ac2872e0724.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d58f80c441597f005ef2264fe2499bc.webp",
    "context": {
      "refs": [
        {
          "alt": "Gate Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66d4a03e05a3382f93263a02b50a75e4.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/6e5268da7bb3290c6299b74ca8654559.webp",
    "context": {
      "refs": [
        {
          "alt": "Check Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7e09e73b5b85f6199a600e7b4a8c2bc8.webp",
    "context": {
      "refs": [
        {
          "alt": "Ball Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/beb8ce65abc219edee13b5de4da2221a.webp",
    "context": {
      "refs": [
        {
          "alt": "BRAND PHILOSOPHY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c2026e53df0da7a34bd84c5fcaeae80b.webp",
    "context": {
      "refs": [
        {
          "alt": "KNOWLEDGE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de11ea234a274ad4f7878567d50b60b4.webp",
    "context": {
      "refs": [
        {
          "alt": "showcasetripleoutputexcdefault",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e6e190cbbff413dba94a1a500c010f96.webp",
    "context": {
      "refs": [
        {
          "alt": "VISION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/edb43813693c42b0742ebe786f7133b0.webp",
    "context": {
      "refs": [
        {
          "alt": "Globe Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee103b3e84ccc30dfcadec184bd0e115.webp",
    "context": {
      "refs": [
        {
          "alt": "Sluice Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f59423f65e76e7b9949e9063a2da9ea8.webp",
    "context": {
      "refs": [
        {
          "alt": "shutterstock",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa0768f4681baa55a59c1f2bcacbff10.webp",
    "context": {
      "refs": [
        {
          "alt": "Butterfly Valve",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fee660a116a280023a51d245fa768197.webp",
    "context": {
      "refs": [
        {
          "alt": "MISSION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Ketan Engineering Works",
      "first_heading": "Ketan Engineering Works"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.