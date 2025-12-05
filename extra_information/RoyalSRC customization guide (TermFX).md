Royal SRC TermFX
Created by https://royalprojets.com
Make sure to read to the bottom for designing tools and colors!

1. ## Attack Attributes (assets/attacks/attacks.json) & (assets/dlc/funnel.json) 
{HOST}                              `Description`	The targeted host (Example: `70.70.70.7`)
{TARGET}                            `Description`	The targeted host (Example: `70.70.70.7`)
{target}                            `Description`	The targeted host (Example: `70.70.70.7`)
{host}                              `Description`	The targeted host (Example: `70.70.70.7`)
{PORT}                              `Description`	The targeted port (Example: `80`)
{port}                              `Description`	The targeted port (Example: `80`)
{dport}                             `Description`	The targeted port (Example: `80`)
{TIME}                              `Description`	The attack duration (Example: `300`)
{time}                              `Description`	The attack duration (Example: `300`)
{DURATION}                          `Description`	The attack duration (Example: `300`)
{duration}                          `Description`	The attack duration (Example: `300`)
{METHOD}                            `Description`	The method that was used (Example: `OVH-TCP`)
{method}                            `Description`	The method that was used (Example: `OVH-TCP`)

almost any variable can be added on any page !!

2. ## Command Placeholders General System Stats (commands/title.royal)
<<$spinner>>                        `Description`   Current spinner position (Example: \ and /)
<<$spinner_custom>>                 `Description`   Custom spinner defined in config.json - Replace 'custom' with any spinner name
<<$total_attack_logs>>              `Description`	Total attacks count on system
<<$max_c2_slots>>                   `Description`	Max slots C2 
<<$max_api_slots>>                  `Description`	Max slots API
<<$total_active_users>>             `Description`	Total Active Users
<<$total_expired_users>>            `Description`	Total Expired Users
<<$total_users>>                    `Description`	Total Users
<<$total_no_active_users>>          `Description`	Total No Active Users ( New User ) First Connection or Api request
<<$online>>                         `Description`	Total number of users currently logged in
<<$fake_online>>                    `Description`	Fake online count + real online users (default adds `4` fake users)
<<$cnc_name>>                       `Description`	CNC name set in config.json (Settings > Cnc_Settings > projet_name)
<<$user.created_by>>                `Description`	Created by (`author`)
<<$all_ongoing>>                    `Description`	All ongoing C2/API attacks count
<<$all_ongoing_c2>>                 `Description`	All C2 ongoing attacks count
<<$all_ongoing_api>>                `Description`	All APi ( Funnel) ongoing attacks count

3. ## User-Specific Data (assets/theme/)
<<$user.username>>                  `Description`	User username (Example: `root`)
<<$user.created_by>>                `Description`	User Created by (`author`)
<<$user.initial_days>>              `Description`	Initial Days Exemple: `31`
<<$user.days_left>>                 `Description`	Days until user expiry
<<$user.time_since_creation>>       `Description`	Days since user creation
<<$user.time_expiry_fmt_1>>         `Description`	User expiry date formatted as `Jan 02 2006`
<<$user.time_expiry_fmt_2>>	        `Description`   Years until expiry
<<$user.admin>>                     `Description`	User Administrator status `true/false`
<<$user.reseller>>	                `Description`   User Reseller status `true/false`
<<$user.vip>>                       `Description`	User VIP status `true/false`
<<$user.api>>	                    `Description`   User API access status `true/false`
<<$user.private>>                   `Description`	User Private status `true/false`
<<$user.owner>>	                    `Description`   User Owner access status `true/false`
<<$user.holder>>	                `Description`   User Holder access status `true/false`
<<$user.ssh_client>>                `Description`   User ssh client 
<<$user.new_user>>                  `Description`	New user status `true/false`
<<$user.total_purchases>>           `Description`	Total purchases for the user.
<<$user.total_purchases_pending>>   `Description`	Total purchases pending for the user.
<<$user.total_purchases_failed>>    `Description`	Total purchases failed for the user.
<<$user.banned>>                    `Description`	User Banned status `true/false`
<<$user.banned_msg>>                `Description`	Custom banned message
<<$user.locked>>                    `Description`	User Locked status `true/false`
<<$user.lock_until_days>>           `Description`	User Lock Until Days
<<$user.lock_message>>              `Description`	User Lock Message
<<$user.bypass_power_saving>>       `Description`	Bypass Power Saving Status
<<$user.bypass_anti_spam>>          `Description`	Bypass Anti Spam Status
<<$user.bypass_blacklist>>          `Description`	Bypass Blacklist Status
<<$user.attacks_count>>             `Description`	User Attack Count
<<$user.unique_targets_count>>      `Description`   Total number of unique targets attacked by the user.
<<$user.first_login_date>>          `Description`   Date of the user's very first login.
<<$user.activity_days_count>>       `Description`   Total number of active days (with at least one connection or attack) for the user.
<<$user.longest_attack_target>>     `Description`   Target attacked for the longest duration by the user.
<<$current_attack_targets>>         `Description`   List of targets currently under attack.
<<$user.daily_attack_limit>>        `Description`   Daily attack limit for this user.
<<$user.daily_attack_left>>         `Description`   Number of attacks remaining for today.
<<$user.last_attack_method_used>>   `Description`   Most frequently used attack method.
<<$user.activity_7_days>>           `Description`   User activity over the last 7 days.
<<user.total_created_users()>>      `Description`   Total users created by the current user.
<<$total_uptime_attacks>>           `Description`   Total User attack uptime.
<<$user.attacks_latest>>            `Description`	Users latest attack target
<<$user.most_frequent_target>>      `Description`   Shows the most frequently attacked target by the user.
<<$user.active_hours>>              `Description`   Shows the hours during which the user was most active in the last 2 days.
<<$user.current_session_ip>>        `Description`   IP address of the active session.
<<$user.daily_usage_summary>>       `Description`   Summary of daily usage per user.
<<$user.last_login>>                `Description`   user's last login date and time
<<$user.login_count>>               `Description`   total number of logins for this user.
<<$user.total_attack_api>>          `Description`   number from Api ( Funnel ) attacks.
<<$user.total_attack_c2>>           `Description`   number from C2 attacks.
<<$user.client.ip>>                 `Description`	User IP address
<<$user.ongoing>>                   `Description`	Ongoing attacks for the user
<<$user.max_sessions>>	            `Description`   Max sessions allowed
<<$user.max_time>>                  `Description`	Max time per attack
<<$user.cooldown>>                  `Description`	Cooldown period
<<$user.max_concurrents>>	        `Description`   Max concurrent attacks
<<$user.most_used_port>>            `Description`   Most used port in user attacks.
<<$user.average_session_time>>      `Description`   Average time of a user session.
<<$user.invest_level>>              `Description`   Current investor level (e.g., "1", "2", "3" or "0" if none)
<<$user.invest_montant_achat>>      `Description`   Total purchase amount (format: "$XX.XX")
<<$user.invest_montant_parraine>>   `Description`   Total referral amount (format: "$XX.XX")
<<$user.invest_total_fortune>>      `Description`   Total fortune (purchases + referrals) (format: "$XX.XX")
<<$user.invest_channel_id>>         `Description`   Investor's private Discord channel ID
<<$user.invest_packs>>              `Description`   List of purchased packs separated by commas or "None"

4. ##### attacks/attack-sent.royal (assets/theme/)
<<$user.most_used_attack_time>>     `Description`   Most used attack time by the user.
<<$target>>                         `Description`   The targeted host (Example: 70.70.70.7)
<<$target.host>>                    `Description`   The targeted host (Example: 70.70.70.7)
<<$target.method>>                  `Description`   The method that was used (Example: OVH-TCP)
<<$target.time_sent>>               `Description`   The unix time when the attack was sent (Example: 1703566826)
<<$target.region>>                  `Description`   Region of target (Example: ON)
<<$target.country>>                 `Description`   Country of target (Example: Canada)
<<$target.country_code>>            `Description`   Country code of target (Example: CA)
<<$target.city>>                    `Description`   Country of target (Example: Toronto)
<<$target.zip>>                     `Description`   Organization of target (Example: M5A)
<<$target.isp>>                     `Description`   ISP of target (Example: Cloudflare, Inc.)
<<$target.org>>                     `Description`   Organization of target (Example: Cloudflare, Inc.)
<<$target.timezone>>                `Description`   Time zone of target (Example: America/Toronto)

5. ##### Commands/lookup-cfx.royal (assets/theme/)
`Response Type: string`
<<$cfx.ip>>                         `Description`   Server Fivem IP
<<$cfx.code>>                       `Description`   Server Fivem Code CFX
<<$cfx.country>>                    `Description`   Server Fivem Country
<<$cfx.owner>>                      `Description`   Server Fivem Owner
<<$cfx.gametype>>                   `Description`   Server Fivem Game Type
<<$cfx.map>>                        `Description`   Server Fivem Map
<<$cfx.project_name>>               `Description`   Server Fivem Projet Name
<<$cfx.project_desc>>               `Description`   Server Fivem Projet Description
<<$cfx.discord_link>>               `Description`   Server Fivem Discord Link
<<$cfx.resources_count>>            `Description`   Server Fivem Ressource count 
<<$cfx.self_reported>>              `Description`   Server Fivem Self Reported
<<$cfx.server_version>>             `Description`   Server Fivem Version
<<$cfx.enhanced_hosting>>           `Description`   Server Fivem Hosting
<<$cfx.hosting>>                    `Description`   Server Fivem Hosting
<<$cfx.org>>                        `Description`   Server Fivem Org
<<$cfx.city>>                       `Description`   Server Fivem City
<<$cfx.region>>                     `Description`   Server Fivem Region
<<$cfx.postal>>                     `Description`   Server Fivem Code Postal
<<$cfx.timezone>>                   `Description`   Server Fivem Timezone
<<$cfx.hostname>>                   `Description`   Server Fivem HostName
`Response Type: int`
<<$cfx.port>>                       `Description`   Server Fivem Port
<<$cfx.players.current>>            `Description`   Server Fivem Players Online
<<$cfx.players.max>>                `Description`   Server Fivem Players Max

6. ##### Commands/lookup-mc.royal (assets/theme/)
`Response Type: string`
<<$mc.ip>>                          `Description`    Server MC IP
<<$mc.code>>                        `Description`    Server MC Domain
<<$mc.country>>                     `Description`    Server MC Country
<<$mc.hosting>>                     `Description`    Server MC Hosting
<<$mc.org>>                         `Description`    Server MC Org
<<$mc.port>>                        `Description`    Server MC Port
<<$mc.players.current>>             `Description`    Server MC Players Online
<<$mc.dns.name>>                    `Description`    dnsData.Name
<<$mc.dns.type>>                    `Description`    dnsData.Type
<<$mc.dns.class>>                   `Description`    dnsData.Class
<<$mc.dns.ttl>>                     `Description`    strconv.Itoa(dnsData.TTL)
<<$mc.dns.rdlength>>                `Description`    strconv.Itoa(dnsData.RDLength)
<<$mc.dns.rdata>>                   `Description`    dnsData.RData
<<$mc.dns.address>>                 `Description`    dnsData.Address

7. ##### Commands/lookup-host.royal (assets/theme/)
<<$host.ip>>                        `Description`   Host IP
<<$host.region>>                    `Description`   Host Region
<<$host.country>>                   `Description`   Host Country
<<$host.continent>>                 `Description`   Host Continent
<<$host.city>>                      `Description`   Host City
<<$host.zip>>                       `Description`   Host ZIP
<<$host.isp>>                       `Description`   Host ISP
<<$host.org>>                       `Description`   Host Organisation
<<$host.timezone>>                  `Description`   Host Timezone

8. ## Login and Position Settings ( assets/theme/views/login & assets/theme/views/newuser )
<<usernameposition(37,11)>>         `Description`   Set position for username input 11 is high & 37 is number of characters
<<passwordposition(37,13)>>         `Description`   Set position for password input 13 is high & 37 is number of characters
<<newpwdposition(37,11)>>	        `Description`   Set position for new password input 11 is high & 37 is number of characters
<<cnewpwdposition(37,13)>>          `Description`   Set position for confirm new password input 13 is high & 37 is number of characters

9. ## System and Date Information (assets/theme/)
<<$uptime_cnc>>                     `Description`   Duration since Royal SRC startup.
<<$uptime_server>>                  `Description`   Duration since the last system startup.
<<time()>>	                        `Description`   UTC time zone
<<$date>>	                        `Description`   UTC date
<<$short_date>>                     `Description`   current date in short format (e.g., DD/MM/YYYY).
<<$full_time>>                      `Description`   full time (e.g., HH:MM:AM/PM).
<<$os>>	                            `Description`   SSH client used for connection (e.g., SSH-2.0-PuTTY_Release_0.81)
<<cpu_usage()>>                     `Description`   CPU usage percentage
<<memory_usage()>>                  `Description`   memory usage percentage
<<os_version()>>                    `Description`   operating system (OS) version
<<kernel_version()>>                `Description`   kernel version (especially useful on Linux)
<<disk_space_used()>>               `Description`   Disk space used.
<<disk_space()>>                    `Description`   Free disk space.

10. ## Terminal ( Screen ) (assets/theme/)
<<clear()>>	                        `Description`   Clear A page
<<$default_screen>>                 `Description`   Screen By Default `80X24`
<<full_screen()>>                   `Description`   Full Screen Defaut `132X40`
<<full_screen_custom(90x30)>>       `Description`   Full Screen `90x30` 90 is high & 30 is width
<<skipline()>>                      `Description`   Skip Defaut `1` Line
<<skipline(5)>>                     `Description`   Custom Skipline `5` Line

11. ## Sleep Functions (assets/theme/)
<<sleep(150)>>                      `Description`   Sleep Custom for `150`  milliseconds
<<10()>>                            `Description`   Sleep for `10`  milliseconds
<<20()>>                            `Description`   Sleep for `20`  milliseconds
<<100()>>                           `Description`   Sleep for `100` milliseconds
<<200()>>                           `Description`   Sleep for `200` milliseconds
<<300()>>                           `Description`   Sleep for `300` milliseconds
<<400()>>                           `Description`   Sleep for `400` milliseconds
<<500()>>                           `Description`   Sleep for `500` milliseconds
<<600()>>                           `Description`   Sleep for `600` milliseconds
<<700()>>                           `Description`   Sleep for `700` milliseconds
<<800()>>                           `Description`   Sleep for `800` milliseconds
<<900()>>                           `Description`   Sleep for `900` milliseconds
<<1000()>>                          `Description`   Sleep for `1`   second

12. ## Bonus (assets/theme/)
<<$top_3_users_by_attacks>>         `Description`   Top 3 users ranked by number of attacks.
<<$new_features_available>>         `Description`   New features or updates available.
<<$attack_methods_availability>>    `Description`   List of available attack methods.
<<$bots_count>>                     `Description`   Bot count ( Attacks.json)
<<$servers_count>>                  `Description`   Server count ( Attacks.json)
<<all_users_rank()>>                `Description`   Ranking of users by rank.
<<top_methods_usage()>>             `Description`   Most used methods in the RoyalSRC.
<<$top_reseller_activity>>          `Description`   Displays the top reseller of the day and the number of users added by them.
<<$attack_peak_hour_today>>         `Description`   Displays the hour today when the highest number of attacks were sent.
<<$attack_method_least_used>>       `Description`   Displays the least used attack method currently in the system.
<<$attack_status>>                  `Description`   Attacks Status Disable/enable
<<$maintenance_status>>             `Description`   Maintenance Status Disable/enable
<<$api_status>>                     `Description`   API status (online or offline).
<<$shop_status>>                    `Description`   Shop status (online or offline).
<<$global_total_users_created>>     `Description`   Total number of users created in the system.
<<$global_new_users_today>>         `Description`   Number of users created today.
<<$global_purchase_today>>          `Description`   Number of purchases today.
<<$global_total_purchases>>         `Description`   Total number of purchases in the system.
<<$global_total_purchases_pending>> `Description`   Total number of purchases pending in the system.
<<$global_total_purchases_failed>>  `Description`   Total number of purchases failed in the system.
<<$global_most_used_payment>>       `Description`   Most used payment method in the system.
<<$global_users_currently_banned>>  `Description`   Number of users currently banned.
<<$global_active_resellers_count>>  `Description`   Number of resellers currently active.
<<$global_active_admin_count>>      `Description`   Number of admins currently active.
<<$global_users_expired_today>>     `Description`   Number of users who expired today.
<<$global_average_attack_time>>     `Description`   Average duration of attacks on the system.
<<$global_top_target_today>>        `Description`   Most attacked target today.
<<$global_peak_user_activity>>      `Description`   Time with the highest number of users connected.
<<$>>                               `Description`   Additional placeholders for future use
<<$>>                               `Description`   Additional placeholders for future use


13. ## Soon-to-Be-Added Features
<<$fake_bots>>                     `Description`   Placeholder for future bot count feature
<<$>>                              `Description`   Additional placeholders for future use
<<$>>                              `Description`   Additional placeholders for future use
<<$>>                              `Description`   Additional placeholders for future use
<<$>>                              `Description`   Additional placeholders for future use
