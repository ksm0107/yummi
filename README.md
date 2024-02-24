<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>나만의 중고마켓</title>
    <link
      rel="stylesheet"
      href="https://s3.ap-northeast-2.amazonaws.com/materials.spartacodingclub.kr/easygpt/default.css"
    />
    <link
      href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.3/dist/css/bootstrap.min.css"
      rel="stylesheet"
      integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65"
      crossorigin="anonymous"
    />
    <style>
      /* 꾸미기 */
      .card {
        margin-bottom: 20px; /* 카드 간의 간격을 조절합니다. */
        transition: transform 0.3s ease; /* 마우스 호버 시 애니메이션 효과를 추가합니다. */
      }

      .card:hover {
        transform: scale(1.05); /* 마우스 호버 시 카드가 약간 커지도록 설정합니다. */
      }
    </style>
  </head>

  <body>
    <div class="hero bg-dark text-center py-5">
      <h1 class="text-white">윰쓰 Daily look</h1>
      <h2 class="text-white">shows 윰쓰 looks</h2>
    </div>
    <div class="container mt-5">
      <div class="row">
        <!-- candles -->
        <div class="col-md-4">
          <div class="card" style="width: 18rem">
            <img
              src="data:image/jpeg;base64,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"
              class="card-img-top"
              alt="최애캔들"
            />
            <div class="card-body">
              <h5 class="card-title">캔들</h5>
              <h6 class="card-subtitle mb-2 text-muted">Candles_forest</h6>
              <p class="card-text">
                엄마의 최애 캔들
              </p>
              <a
                href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.thefarmhouseproject.com%2Fproduct%2Fforest-candle%2F&psig=AOvVaw2mFxQvuE5G5dURnmBAZx7q&ust=1708877329393000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCLje8aKuxIQDFQAAAAAdAAAAABAI"
                class="btn btn-primary"
                target="_blank"
                rel="noopener noreferrer"
              >
              클릭하여 구매
              </a>
            </div>
          </div>
        </div>
        <!-- Smells -->
        <div class="col-md-4">
          <div class="card" style="width: 18rem">
            <img
              src="https://imgmedia.lbb.in/media/2020/12/5fed85b677b45c7d194202f9_1609401782517.jpg"
              class="card-img-top"
              alt="Smells"
            />
            <div class="card-body">
              <h5 class="card-title">향</h5>
              <h6 class="card-subtitle mb-2 text-muted">Deep_nature</h6>
              <p class="card-text">
                엄마의 Most pick Smells
              </p>
              <a
                href="https://www.google.com/url?sa=i&url=https%3A%2F%2Flbb.in%2Fmumbai%2Fdeep-forest-farms%2F&psig=AOvVaw3t3NgwtB2pX7AbIBEz_1FG&ust=1708877588554000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCPDb056vxIQDFQAAAAAdAAAAABAF"
                class="btn btn-primary"
                target="_blank"
                rel="noopener noreferrer"
              >
              클릭하여 구매
              </a>
            </div>
          </div>
        </div>
        <!-- Dishes -->
        <div class="col-md-4">
          <div class="card" style="width: 18rem">
            <img
              src="https://m.media-amazon.com/images/I/516PFcqea9L.jpg"
              class="card-img-top"
              alt="Dish"
            />
            <div class="card-body">
              <h5 class="card-title">접시</h5>
              <h6 class="card-subtitle mb-2 text-muted">Flower_Dressed up</h6>
              <p class="card-text">
                꽃 문양 그릇
              </p>
              <a
                href="https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.amazon.com%2FDessert-Dishes-Porcelain-Kitchen-Accessories%2Fdp%2FB0BKFWVFX6&psig=AOvVaw3zCpHjA-tVVFe8xuX_f7_i&ust=1708877729715000&source=images&cd=vfe&opi=89978449&ved=0CBIQjRxqFwoTCJCl9-GvxIQDFQAAAAAdAAAAABAJ"
                class="btn btn-primary"
                target="_blank"
                rel="noopener noreferrer"
              >
                클릭하여 구매
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </body>
</html>
