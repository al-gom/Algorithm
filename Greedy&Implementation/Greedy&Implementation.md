# ๐ ๊ทธ๋ฆฌ๋ ์๊ณ ๋ฆฌ์ฆ (ํ์๋ฒ) :: Greedy Algorithm
### - ํ์ฌ ์ํฉ์์ ์ง๊ธ ๋น์ฅ ์ข์ ๊ฒ๋ง ๊ณ ๋ฅด๋ ๋ฐฉ๋ฒ
### - ์ผ๋ฐ์ ์ธ ๊ทธ๋ฆฌ๋ ์๊ณ ๋ฆฌ์ฆ์ ๋ฌธ์ ๋ฅผ ํ๊ธฐ ์ํ ์ต์ํ์ ์์ด๋์ด๋ฅผ ๋ ์ฌ๋ฆด ์ ์๋ ๋ฅ๋ ฅ์ ์๊ตฌํ๋ค.
### - ํฌ๋ฃจ์ค์นด, ๋ค์ด์คํธ ์ต๋จ ๊ฒฝ๋ก๋ฑ ์ ์๋ ค์ง ์๊ณ ๋ฆฌ์ฆ์ ์ ์ธํ๊ณ  ์ผ๋ฐ์ ์ผ๋ก ๊ทธ๋ฆฌ๋ ์๊ณ ๋ฆฌ์ฆ์ด ์ถ์ ๋๋ฉด ํด๋น ๋ฌธ์ ๋ฅผ ํ๊ธฐ์ํ ์ ์ ํ ์๊ณ ๋ฆฌ์ฆ์ ๋ ์ฌ๋ ค์ผ ๋ฌธ์ ๋ฅผ ํ์์๋ค
### - ๋จ์ํ ๊ฐ์ฅ ์ข์ ๋ณด์ด๋ ๊ฒ์ ๋ฐ๋ณต์ ์ผ๋ก ์ ํํด๋ ์ต์ ์ ํด๋ฅผ ๊ตฌํ  ์ ์๋์ง ๊ฒํ ํ๋ค.
### - ๋ฌธ์ ์์ ์๊ตฌํ๋ ์ต์ ์ ํด๋ฅผ ์ฐพ์ ์ ์๋์ง๊ฐ ์ค์ํ๋ค.
## ๐ ์ฝ๋ฉํ์คํธ์์์ ๊ทธ๋ฆฌ๋ ์๊ณ ๋ฆฌ์ฆ
    ์ผ๋ฐ์ ์ธ ์ํฉ์์ ๊ทธ๋ฆฌ๋ ์๊ณ ๋ฆฌ์ฆ์ ์ต์ ์ ํด๋ฅผ ๋ณด์ฅํ  ์ ์์ ๋๊ฐ ๋ง๋ค.
    ํ์ง๋ง ์ฝ๋ฉํ์คํธ์์์ ๋๋ถ๋ถ์ ๊ทธ๋ฆฌ๋ ๋ฌธ์ ๋ ํ์๋ฒ์ผ๋ก ์ป์ ํด๊ฐ ์ต์ ์ ํด๊ฐ ๋๋ ์ํฉ์์,
    ๋จ์ํ ๊ทธ๋ฆฌ๋ ์๊ณ ๋ฆฌ์ฆ์ ์ด์ฉํด๋ ์ต์ ํด๊ฐ ๋๋ค๋ ๊ฒ์ ์ด๋ฅผ ์ถ๋ก ํ  ์ ์์ด์ผ ํ๋ฆฌ๋๋ก ์ถ์ ๋๋ค.
    ๊ทธ๋ฆฌ๋๋ก ์ป์ ํด๊ฐ ์ต์ ์ํด๊ฐ ๋๋ ๊ฒฝ์ฐ์ ํ์์ ๋ฌธ์ ๊ฐ ์์ฃผ ์ถ์ ๋๋ค.

# ๐ ๊ตฌํ :: Implementation
## ๐ ๊ตฌํ์ด๋, ๋จธ๋ฆฟ์์ ์๋ ์๊ณ ๋ฆฌ์ฆ์ ์์ค์ฝ๋๋ก ๋ฐ๊พธ๋ ๊ณผ์ ์ด๋ค.
    problem -> thinking -> solution

## ๐ ์๊ณ ๋ฆฌ์ฆ ๋ํ์์ ๊ตฌํ ์ ํ์ ๋ฌธ์ ๋?
    ํ์ด๋ฅผ ๋ ์ธ๋ฆฌ๋ ๊ฒ์ ์ฝ์ง๋ง ์์ค์ฝ๋๋ฅผ ์ฎ๊ธฐ๊ธฐ ์ด๋ ค์ด ๋ฌธ์ 
## ๐ ์์
### 1. ์๊ณ ๋ฆฌ์ฆ์ ๊ฐ๋จํ๋ฐ ์ฝ๋๊ฐ ์ง๋์น ๋งํผ ๊ธธ์ด์ง๋ ๋ฌธ์ 
- ์ฌ์ฉํ๋ ํ๋ก๊ทธ๋๋ฐ ์ธ์ด์ ๋ฐ๋ผ ๋ฌ๋ผ์ง ์๋ ์๋ค.
### 2. ์ค์ ์ฐ์ฐ์ ๋ค๋ฃจ๊ณ , ํน์  ์์์  ์๋ฆฌ๊น์ง ์ถ๋ ฅํด์ผ ํ๋ ๋ฌธ์ 
- ๋ฌธ๋ฒ์ ์ผ๋ก ํน์  ํ๋ก๊ทธ๋๋ฐ์ธ์ด๋ก ๊ตฌํํ๋ ๋ฐฉ๋ฒ์ ์๊ณ  ์์ด์ผํ๋ค.
### 3. ๋ฌธ์์ด์ ํน์ ํ ๊ธฐ์ค์ ๋ฐ๋ผ์ ๋์ด ์ฒ๋ฆฌํด์ผ ํ๋ ๋ฌธ์ 
- ํ์ด์ฌ์ด ๋ค๋ฅธ ์ธ์ด์ ๋นํด ์๋์ ์ผ๋ก ์ฌ์ฉํ๊ธฐ ํธํ๋ค.
### 4. ์ ์ ํ ๋ฆฌ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ์ฐพ์์ ์ฌ์ฉํด์ผํ๋ ๋ฌธ์ 
- ์ผ๋ฐ์ ์ผ๋ก ๋ง์ ๊ธฐ์ ๋ฌธ์ ์์ 2์ฐจ์ ๊ณต๊ฐ์ ์ฌ์ฉํ๋ค (ํ๋ ฌ)