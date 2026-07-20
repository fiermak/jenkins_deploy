pipeline {
    agent any

    stages {
        stage('Build Steps - Test') {
            steps {
                sh '''
                echo "Перевірка файлу index.html..."

                if [ ! -f index.html ]; then
                    echo "ПОМИЛКА: Файл index.html не існує!"
                    exit 1
                fi

                lines=$(wc -l < index.html)
                text=$(cat index.html)

                if [ "$lines" -eq 1 ] && [ "$text" = "KAF21_TASP_JENKINS" ]; then
                    echo "Тест пройдено успішно!"
                else
                    echo "ПОМИЛКА: Вміст index.html неправильний!"
                    echo "Очікується один рядок: KAF21_TASP_JENKINS"
                    exit 1
                fi
                '''
            }
        }
    }
}
