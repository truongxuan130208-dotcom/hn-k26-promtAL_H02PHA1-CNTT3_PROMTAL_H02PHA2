# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 07
- **Họ tên:PHẠM XUÂN TRƯỜNG**
- **Lớp:CNTT3**
- **Link repository Pha2:https://github.com/truongxuan130208-dotcom/hn-k26-promtAL_H02PHA1-CNTT3_PROMTAL_H02PHA2/blob/4c7e5a6f69a1f6eaaa31cb49deec58756d5a30a4/bai_lam_pha2.md**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):GEMINI**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé vào cổng ra JSON

**KET QUA AI**

```text
[
  {
    "loai_ve": "VECH",
    "ngay_choi": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_tu": "nho",
    "ghi_chu": null
  },
  {
    "loai_ve": "VECN",
    "ngay_choi": "2027-01-03",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_tu": null,
    "ghi_chu": "Một người đang bó bột tay"
  },
  {
    "loai_ve": "VEVIP",
    "ngay_choi": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_tu": "lon",
    "ghi_chu": "một bạn đi xe lăn"
  }
]
```

**Link trò chuyện:https://share.gemini.google/ZFZhq8OmoVxD**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
1. **Tiền vé người lớn:** Đoàn gồm 8 người lớn áp dụng mức giá vé cả ngày (VECN): `8 x 250.000 = 2.000.000 đồng`
2. **Tiền vé trẻ em:** Gồm 4 trẻ cao từ 1 m đến 1,4 m (1,05 m; 1,15 m; 1,2 m; 1,3 m) tính 60% giá vé người lớn và 2 bé dưới 1 m được miễn phí: `(4 x 250.000 x 60%) + (2 x 0) = 600.000 đồng`
3. **Tiền vé:** Tổng tiền vé trước khi giảm giá: `2.000.000 + 600.000 = 2.600.000 đồng`
4. **Giảm giá đoàn:** Đoàn có 8 người lớn (đạt điều kiện từ 8 người lớn trở lên) nên được giảm 10% trên tiền vé: `2.600.000 x 10% = 260.000 đồng`
5. **Phụ thu:** Phí thuê 6 áo phao (không áp dụng giảm giá): `6 x 40.000 = 240.000 đồng`
6. **Tổng tiền:** Tiền vé sau giảm giá cộng với phụ thu: `(2.600.000 - 260.000) + 240.000 = 2.580.000 đồng`

[RESULT: 2.580.000 đồng]
```

**Link trò chuyện:https://share.gemini.google/rxHjEIr7p2Tj**

### b) Kiểm tra kết quả AI

kết quả Al đã đúng

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "dong_khu_choi",
  "so_khach": 4,
  "so_khu_bi_dong": 2,
  "tom_tat": "Khách phản ánh hai khu trò chơi đóng cửa cả ngày không báo trước trên website."
}
```

**Link trò chuyện:https://share.gemini.google/yFPb75OGqB25**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| Đúng thông tin (50%) | 0/5 | Báo giá "150k" (sai với 180.000 đồng/vé người lớn); báo "hoàn tiền mặt 100%" (sai với chính sách vào dưới 2 giờ được tặng 1 vé cùng loại dùng trong 30 ngày, không hoàn tiền mặt). | Cập nhật giá vé chiều là 180.000 đồng/vé người lớn; khi đóng cửa do mưa và khách mới vào 1 tiếng (dưới 2 giờ), tặng 1 vé cùng loại có hiệu lực trong 30 ngày, không hoàn tiền mặt. |
| Đầy đủ (30%) | 2/3 | Có trả lời câu hỏi về giá và tình huống mưa đóng cửa sau 1 tiếng, nhưng thiếu lời mời cung cấp ngày đi và số lượng vé để đặt. | Bổ sung lời mời khách cung cấp ngày đi và số lượng vé cần đặt để hỗ trợ nhanh chóng. |
| Giọng điệu (20%) | 0.5/2 | Dùng từ ngữ suồng sã, kém trang trọng: "Hello chị!", "mát rượi luôn", "nha", "ới em nhé". | Chuyển sang xưng hô lịch sự, nhã nhặn (ví dụ: "Chào Quý khách", "Dạ, bên em xin thông tin...", "Rất hân hạnh được hỗ trợ Quý khách"). |
| **Tổng điểm** | **2.5/10** |  |  |
```

**Link trò chuyện:https://share.gemini.google/w1rya2BY9kr8**
