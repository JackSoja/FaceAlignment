cmake_minimum_required(VERSION 2.8)
set(OpenCV_DIR /usr/local/lib/opencv/share/OpenCV)
find_package( OpenCV REQUIRED )

set(source ./FaceAlignment.h ./FernCascade.cpp ./Fern.cpp ./ShapeRegressor.cpp ./Utils.cpp ./TrainDemo.cpp)
add_executable(TrainDemo.out ${source})
target_link_libraries(TrainDemo.out ${OpenCV_LIBS})

set(source ./FaceAlignment.h ./FernCascade.cpp ./Fern.cpp ./ShapeRegressor.cpp ./Utils.cpp ./TestDemo.cpp)
add_executable(TestDemo.out ${source})
target_link_libraries(TestDemo.out ${OpenCV_LIBS})


