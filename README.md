// ==UserScript==
// @name         My name an a andy
// @namespace    
// @version      0.2
// @description  Trigger the 'ended' event on video elements when a new page is loaded
// @grant        none
// ==/UserScript==

document.addEventListener('click', function() {
    // 检查页面中是否存在视频元素
    var videoElement = document.querySelector('video');
    if (videoElement) {
        // 创建一个'ended'事件
        var endedEvent = new Event('ended');
        // 触发视频元素的'ended'事件
        videoElement.dispatchEvent(endedEvent);
        console.log('Video ended event triggered:', videoElement);
    } else {
        console.log('No video element found');
    }
});
