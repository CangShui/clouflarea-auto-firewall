# clouflarea-auto-firewall
<p>Auto open firewallrules</p>
<p>cpuauto.sh是通过本机负载来判断是否开启验证码</p>
<p>curlauto.sh是使用其他服务器curl网站获得的nginx code 来判断的</p>

<p>详细食用方法</p>
<a href="https://cangshui.net/?p=4516">https://cangshui.net/4516.html</a></p>


#### 推荐使用以下方法来快速获取脚本中的rulesid：

```bash
curl -X GET \
"https://api.cloudflare.com/client/v4/zones/<ZONE_ID>/firewall/rules" \
-H "X-Auth-Email: <EMAIL>" \
-H "X-Auth-Key: <API_KEY>"
```

<p>在WAF页面创建好规则再使用上面的GET方式获得该规则的ID</p>
<p>返回的结果中"result"下面的"id"即为脚本中的"rulesid1"</p>
<p>"filter"下面的"id"则为“rulesid2”，其余ID获取方式参考博客中的截图</p>
