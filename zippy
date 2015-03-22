#!/usr/bin/env ruby

### This Ruby Script allows you to download files
### from Zippyshare.com in your terminal
### using open-uri and wget

### zippy-rb (Sheharyar Naseer © 2015)



# Requires
require 'open-uri'


# Constants
USER_AGENT = 'Mozilla/5.0 (Windows NT 6.0) Gecko/20100101 Firefox/14.0.1'
MAIN_REGEX = /test.test\('dlbutton', "(\/d\/\w*\/)" ?\+ ?\(a ?\* ?b ?\+ ?(\d*)\)\+"(.*)"\);/


# Methods
def host(link)
    "http://#{URI(link).host}"
end

def get_var(doc, var)
    regex = /var #{var} ?= ?(\d*%\d*);/
    value = doc[regex].gsub(regex, '\1')

    eval value
end

def get_cookie(page)
    cdata = page.meta["set-cookie"]
    regex = /(JSESSIONID=\w*)/

    cdata[regex]
end

def do_magic(link)
    # Fetch and Parse webpage
    page   = open(link, "User-Agent" => USER_AGENT)
    doc    = page.read

    cookie = get_cookie(page)

    var_a  = get_var(doc, 'a')
    var_b  = get_var(doc, 'b')

    exprs  = doc[MAIN_REGEX]
    sumval = exprs.gsub(MAIN_REGEX, '\2').to_i
    durl   = exprs.gsub(MAIN_REGEX, "#{ host(link) }#{ '\1' }#{ var_a * var_b + sumval }#{ '\3' }")


    # Run this output of this command in your terminal 
    system "wget #{durl} --referer='#{link}' --cookies=off --header 'Cookie: #{cookie}' --user-agent='#{USER_AGENT}'"
end



## MAIN
if ARGV.count == 0
    puts "usage: zippy link [link2 link3 ...]", ""
else
    ARGV.each do |link|
        do_magic  link
    end
end

