# frozen_string_literal: true

source "https://rubygems.org"

gem "jekyll", "~> 4.3"
gem "jekyll-seo-tag", "~> 2.8"
gem "jekyll-paginate", "~> 1.1"
gem "jekyll-feed", "~> 0.17"
gem "jekyll-redirect-from", "~> 0.16"

# Ruby 3+ 에서 webrick이 기본 포함에서 제외됨
gem "webrick", "~> 1.8"

# Ruby 4.0 stub: eventmachine C extension은 Ruby 4.0과 비호환
# jekyll --livereload 미사용 시 런타임에서 실제로 호출되지 않음
gem "eventmachine", path: "vendor/eventmachine"
