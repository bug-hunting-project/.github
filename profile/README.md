## Project introduction

### Background of product

사이버 공격은 시간이 지날수록 고도화되어 증가하는 추세로 최근에는 주요 공격 대상을 스타트업으로 확장하면서 많은 스타트업에서 개인정보 유출 사례가 급증하고 있다. 이로 인한 정보보안 강화의 중요성은 날이갈수록 증가하고 있지만 예산과 인력 문제 등으로 어려움을 겪고 있다.

![image](https://github.com/bug-hunting-project/.github/assets/29292618/ff005587-9fa2-4a48-9f5c-610701483a7e)


 하루 평균 약 수십 개에서 수백 개까지 발표되는 공개 취약점(CVE, Common Vulnerabilities and Exposures)은 공개적으로 알려진 보안 결함 목록으로 영향을 미치는 소프트웨어와 버전, 심각도를 명시하여 발표하고 있으며 계속하여 증가세를 유지하고 있다.

![image](https://github.com/bug-hunting-project/.github/assets/29292618/904ab035-df5c-4d98-b0d3-0bcf6c740ff5)


 하지만 발표되는 공개 취약점은 공격코드 존재 및 서비스에서 사용 중인 소프트웨어 여부 등과 같이 추가 정보가 없는 경우 현재 기업에서 개발/운영중인 서비스에 실질적인 보안 위험이 존재하는지 여부와 파급력을 파악하기 어려운 문제가 존재한다.
 이러한 문제를 해결하기 위하여 본 프로젝트에서는 먼저 서비스에서 사용중인 소프트웨어 명세서를 나타내는 SBOM (Software Bill Of Materials)을 분석한다. 공개취약점을 활용한 공격 코드 유무를 수집하고, Multi GAI를 활용하여 공개 취약점에 대해 쉬운 설명과 프로젝트에 영향이 있는지 확인할 수 있는 방법을 질의한 결과 등을 종합한다. 서비스에 실질적인 보안 위험이 발생하는 우선순위를 재산출하여 보안 위험에 대비하는 프로젝트를 개발하고자 한다.

## Features

### 프로젝트 파일(packages.json, build.gradle, setup.py 등) 기반의 SBOM (Software Bill Of Materials) 분석

    - SBOM 분석으로 프로젝트에 존재하는 취약점 존재 여부 확인 및 정보 파싱
    - 파싱된 취약점 정보를 통한 데이터 분석
        • 취약점의 개념증명코드(PoC) 및 공격 코드(Exploit Code) 존재 여부
        • 미국 국립표준기술연구소(NIST)의 취약점 데이터베이스(NVD)에서 평가한 위험도 점수

### 공개 취약점 현황 정보 대시보드

    - 실시간으로 다양한 취약점 데이터베이스(NVD, SecDB, ALAS, RHSAs, GHSAs 외 6개)에서 정보 파싱
    - 취약점의 개념증명코드(PoC) 및 공격 코드(Exploit Code) 공개 URL 정보 파싱
    - Next.JS를 이용한 SSR 환경의 대시보드를 개발하여 발견된 취약점 갯수 및 여러 데이터 시각화

### Multi GAI를 활용한 데이터 분석 및 레포트 제작

    - 다양한 GAI(ChatGPT, Bard Ai, Bing GPT 등)에 취약점 정보를 제공하여 데이터 분석
    - 분석을 동해 취약점 설명, 대응 방안, 주의점 등을 정리하여 레포트 제작

## Architecture

![image](https://github.com/bug-hunting-project/.github/assets/29292618/f5c47ed8-3606-41b0-9f0e-4a98b33a70ff)


## UI Image

<b> 
  
- Main

![image](https://github.com/bug-hunting-project/.github/assets/29292618/b4d0cc80-8eef-4abd-a8c7-5d4baa4d0800)

  
- Analytics and Report
  
![image](https://github.com/bug-hunting-project/.github/assets/29292618/10515ba5-66fc-40f6-9df2-9e11a9db4dce)


<b> 
  
- Export Report

![image](https://github.com/bug-hunting-project/.github/assets/29292618/9e0f72b7-2ee2-4155-a404-6c07f112b760)


## Sequence Diagram

![image](https://github.com/bug-hunting-project/.github/assets/29292618/68c6388f-5947-49f1-b380-a0b50171913e)
