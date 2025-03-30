# Motor-Imagery

Mini project môn học Tính toàn khoa học thần kinh và ứng dụng

## 1. Clone the project: 
-	git clone (repository-url)
-	cd <repository-name>

## 2. Cài đặt môi trường ảo Python, sử dụng python phiên bản 3.9 
-	python -m venv venv-bci-experiment-1
-	source venv-bci-experiment-1/bin/activate (Macs)
-	venv-bci-experiment-1\Scripts\activate (Windows)

## 3.Cài đặt thư viện yêu cầu 
-	pip install -r requirements.txt
-	pip install notebook
-	pip install mne (1.16.0)

## 4.Chạy chương trình
-	jupyter notebook
-	python utils/get_csv_from_gdf.py (Trục quan hoá dữ liệu)

## 5. Cấu hình file
-	notepad “cd <repository-name>\ venv-bci-experiment-3\lib\site-packages\mne\io\edf\edf.py”
-	Thay thế dòng 
n_events = n_events + ne[i] * 2 ** (i * 8)
bằng
n_events += int(ne[i]) * (2 ** (i * 8))
