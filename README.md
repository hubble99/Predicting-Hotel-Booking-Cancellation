# Predicting Hotel Booking Cancellation

Proyek ini bertujuan untuk mengembangkan model prediktif yang dapat memprediksi kemungkinan pembatalan pemesanan hotel. Selain itu, hasil analisis data akan digunakan untuk memberikan rekomendasi operasional kepada hotel.

## Dataset

Dataset yang digunakan adalah "Booking Hotel" yang terdiri dari 31 kolom dan 82,665 baris.

## Data Cleaning

Proses data cleaning melibatkan langkah-langkah sebagai berikut:
- Handling Missing Value
- Handling Incorrect Data Type
- Handling Incorrect Value

## Hasil EDA (Exploratory Data Analysis)

Beberapa temuan kunci dari analisis data adalah:
1. Lead Time and Cancellation: Longer lead times are associated with higher cancellation rates, perhaps because customers have more time to consider and plan their trip.
2. Deposit Type and Cancellation: Bookings with non-refundable deposits have the highest cancellation rates, suggesting that deposit policies may influence cancellation decisions.
3. Previous Cancellations and Cancellation: Previous cancellation history significantly increases the likelihood of future cancellations.
4. Guest Location and Cancellation: Local guests tend to have a higher cancellation rate than international guests, perhaps because local travel considerations are more flexible.
5. Repeated Guest and Cancellation: Repeat guests are less likely to cancel a booking.
6. Market Segment and Customer Type: Certain market segments and customer types have higher cancellation rates, demonstrating the importance of understanding customer profiles to manage cancellation risk.
7. Booking Changes and Cancellation: Customers who make changes to booking details have lower cancellation rates.
8. Special Request and Cancellation: Customers who request special requests have a lower cancellation rate.
9. Parking Space and Meal Type: Parking requests and meal types can influence cancellation decisions.
10. Distribution Channel and Cancellation: Certain distribution channels have higher cancellation rates, which may reflect the policies or characteristics of ordering through those channels.
11. Assigned Room Type and Reserved Room Type: Certain room types have different cancellation rates, indicating variations in preferences or room characteristics that may influence cancellation decisions.

## Data Preprocessing

Proses preprocessing data melibatkan langkah-langkah sebagai berikut:
- Penambahan fitur baru
- Simplifikasi fitur
- Transformasi data
- Feature scaling
- Encoding feature kategorikal
- Resampling data dengan Undersampling karena label target tidak seimbang

## Model yang Digunakan

Model yang digunakan untuk prediksi meliputi Logistic Regression, Decision Tree, Random Forest, dan XGBoost. Tuning model dilakukan dengan menggunakan Random Search.

## Model Evaluation

XGBoost yang sudah dituned pada resampling menjadi pilihan terbaik berdasarkan nilai F1-Score dan False Negative Rate.

## Feature Importance

Feature importance dari model:
- Random Forest: 1. Lead Time, 2. adr, 3. Total Stays, 4. deposit_type_No Deposit, 5. deposit_type_Non Refund
- XGBoost: 1. deposit_type_Non Refund, 2. Previous Cancellations, 3. park_car_req_Yes, 4. guest_location_Local, 5. deposit_type_No Deposit

## Rekomendasi

Berdasarkan temuan dari analisis dan model prediktif, beberapa rekomendasi operasional yang dapat dilakukan oleh hotel adalah:
1. Tinjau dan sesuaikan kebijakan deposit untuk meningkatkan fleksibilitas dan meminimalkan hambatan pembatalan.
2. Berikan penekanan khusus pada lead time dan ADR. Mungkin ada kebijakan pembatalan yang lebih fleksibel untuk pemesanan jangka panjang atau penyesuaian harga yang dapat menarik pelanggan.
3. Kembangkan pendekatan personalisasi untuk meminimalkan risiko pembatalan dari pelanggan yang memiliki riwayat pembatalan sebelumnya.
4. Pertimbangkan untuk menyusun paket atau penawaran khusus untuk mengundang pelanggan untuk menginap lebih lama.
