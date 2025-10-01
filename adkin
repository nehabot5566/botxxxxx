const axios = require("axios");
const request = require("request");
const fs = require("fs-extra");
const moment = require("moment-timezone");

module.exports.config = {
    name: "admin",
    version: "1.0.0",
    hasPermssion: 0,
    credits: "RAIHAN", //don't change my credit 
    description: "Show Owner Info",
    commandCategory: "info",
    usages: "/",
    cooldowns: 5
};

module.exports.run = async function({ api, event }) {
    var time = moment().tz("Asia/Dhaka").format("DD/MM/YYYY hh:mm:ss A");

    var callback = () => api.sendMessage({
        body: `
┏━━━━━━━━━━━━━━━━━━━━━┓
┃      🌟 𝗢𝗪𝗡𝗘𝗥 𝗜𝗡𝗙𝗢 🌟      
┣━━━━━━━━━━━━━━━━━━━━━┫
┃ 👤 𝐍𝐚𝐦𝐞      : 𝐑𝐀𝐈𝐇𝐀𝐍
┃ 🚹 𝐆𝐞𝐧𝐝𝐞𝐫    : 𝐌𝐚𝐥𝐞
┃ ❤️ 𝐑𝐞𝐥𝐚𝐭𝐢𝐨𝐧  : 𝕊𝕚𝕟𝕘𝕖𝕝
┃ 🎂 𝐀𝐠𝐞       : 18+
┃ 🕌 𝐑𝐞𝐥𝐢𝐠𝐢𝐨𝐧  : 𝐈𝐬𝐥𝐚𝐦
┃ 🏫 𝐄𝐝𝐮𝐜𝐚𝐭𝐢𝐨𝐧 : 𝐓𝐎 𝐓𝐎 𝐂𝐀𝐌𝐏𝐀𝐍𝐈𝐑 𝐌𝐀𝐍𝐄𝐆𝐄𝐑
┃ 🏡 𝐀𝐝𝐝𝐫𝐞𝐬𝐬  : 𝐌𝐎𝐍𝐈𝐑𝐀𝐌𝐏𝐔𝐑,𝐉𝐄𝐒𝐒𝐎𝐑𝐄
┣━━━━━━━━━━━━━━━━━━━━━┫
┃ 🌐 𝐅𝐚𝐜𝐞𝐛𝐨𝐨𝐤 : https://www.facebook.com/WELCOME.TO.MY.PROFILE.CONGREGATION
┗━━━━━━━━━━━━━━━━━━━━━┛
        `,
        attachment: fs.createReadStream(__dirname + "/cache/1.png")
    }, event.threadID, () => fs.unlinkSync(__dirname + "/cache/1.png"));
    return request(encodeURI(`https://graph.facebook.com/100063630462991/posts/1297302935734043/?substory_index=2345636802505871&app=fbl`))
        .pipe(fs.createWriteStream(__dirname + '/cache/1.png'))
        .on('close', () => callback());
};
