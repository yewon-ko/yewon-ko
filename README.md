<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <div class="container-fluid bg-success text-center py-5">
        <h1 class="display-4 text-black">자원봉사 찾기</h1>
        <p class="lead text-black">누구나 쉽게 자원봉사 찾기</p>
    </div>

    <!-- 드롭다운 메뉴 추가 -->
    <div class="container mt-5">
        <div class="row justify-content-center">
            <!-- 지역 선택 드롭다운 -->
            <div class="col-md-3 mb-3">
                <div class="dropdown">
                    <button class="btn btn-primary dropdown-toggle" type="button" id="regionDropdownMenuButton" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        지역선택
                    </button>
                    <div class="dropdown-menu" aria-labelledby="regionDropdownMenuButton">
                        <a class="dropdown-item" href="#" onclick="selectRegion('마포구')">마포구</a>
                        <a class="dropdown-item" href="#" onclick="selectRegion('영등포구')">영등포구</a>
                        <a class="dropdown-item" href="#" onclick="selectRegion('용산구')">용산구</a>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- 선택된 항목 표시를 위한 스크립트 추가 -->
    <script>
        function selectRegion(region) {
            document.getElementById('regionDropdownMenuButton').innerText = region;
            // 지역에 따라 다른 이미지 설정
            var imgSrc = '';
            if (region === '마포구') {
                imgSrc = 'https://ifh.cc/g/YKwfh8.png';
            } else if (region === '영등포구') {
                imgSrc = 'https://ifh.cc/g/1rS4Sl.png4';
            } else if (region === '용산구') {
                imgSrc = 'https://ifh.cc/g/NMkwYY.png';
            }
            // 이미지를 표시할 div에 이미지 추가
            document.getElementById('imageContainer').innerHTML = '<img src="' + imgSrc + '" alt="' + region + '" style="max-width: 100%; height: auto;">';
        }
    </script>

    <!-- 이미지를 표시할 div -->
    <div class="container mt-5 text-center" id="imageContainer">
        <img src="https://ifh.cc/g/ohR7zD.png"  style="max-width: 100%; height: auto;>
        <img src="https://ifh.cc/g/ohR7zD.png" alt="마포구" style="max-width: 100%; height: auto;">
    </div>


    <!-- 부트스트랩 JS 및 jQuery 추가 -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</body>
</html>
