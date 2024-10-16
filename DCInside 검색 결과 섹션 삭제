// ==UserScript==
// @name         DCInside 검색 결과 섹션 삭제
// @namespace    http://tampermonkey.net/
// @version      1.0
// @description  DCInside 게시물 검색 결과를 삭제합니다.
// @author       You
// @match        *://gall.dcinside.com/*
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    // 특정 검색 결과 섹션을 삭제하는 함수
    function removeSearchResults() {
        const searchSection = document.querySelector('#kakao_search');
        if (searchSection) {
            searchSection.remove();  // 해당 섹션 전체 삭제
        }
    }

    // 페이지 로드 시 실행
    window.addEventListener('load', function() {
        removeSearchResults();
    });

    // 페이지 동적 업데이트 감지하여 재실행
    const observer = new MutationObserver(removeSearchResults);
    observer.observe(document.body, { childList: true, subtree: true });
})();
