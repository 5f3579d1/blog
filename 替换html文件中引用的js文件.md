替换html文件中引用的js文件
=========================

grep -r -A 2 'jquery.SuperSlide' .

xargs sed -e '/jquery.SuperSlide/c\<script type=\"text\/javascript\" src=\"http:\/\/static.todcy.cn\/js\/jquery.SuperSlide.js\"><\/script>'

find . -name '*html' | xargs sed -i '/jquery.SuperSlide/c\<script type=\"text\/javascript\" src=\"http:\/\/static.todcy.cn\/js\/jquery.SuperSlide.js\"><\/script>'

