# BugBounty-Portfolio
Bug bounty hunter | Web security researcher | Finding and reporting vulnerabilities ethically XSS • SQLi • IDOR • CSRF • Business Logic Flaws

# 1
# Reflected XSS on meratrip.in

**URL**: `https://www.meratrip.in/holiday/search?tag=Themes&slug=<script>alert("bugbounty")</script>&id=7`  
**Parameter**: `slug`  
**Type**: Reflected XSS  
**Severity**: Medium  
**Date**: 03.02.2026

**Proof**: Alert executes when visiting the URL  
**Impact**: Session theft, phishing, defacement  

**Fix**: Validate `slug` parameter, encode output, add CSP header  

**Status**: Reported to OpenBugBounty
