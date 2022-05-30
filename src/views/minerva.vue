<template>
<div class = 'container-fluid quizzes'>
    <div class="row quizzes-row top" v-if="hasQuiz">
        <div class="col-sm-12 col-md-12 col-lg-6 col-xl-6 left">
            <div class="quizzes-title">Một trải nghiệm Đại học phi thường</div>
            <div class="quizzes-desc">Club Fair 2021 của Ams Advisor hân hạnh được tài trợ bởi Trường Đại học Minerva - một Chương trình Đại học phi thường vòng quanh thế giới. 

Là top 3 trường Đại học có Tầm ảnh hướng của thế giới, Đại học Minerva với mô hình khai phóng đã đưa việc học chủ động vào chương trình và thay đổi việc học trực tuyến cho toàn bộ nền giáo dục bậc cao. 

Sinh viên Minerva <strong>học và sinh sống, trải nghiệm tại 7 thành phố trong 4 năm học</strong> bao gồm San Francisco, London, Berlin hay Seoul. 

100% hệ thống tuyển sinh phụ thuộc vào thành tích của sinh viên và không cần điểm thi chứng chỉ. Đặc biệt, <strong>81% sinh viên Minerva được nhận hỗ trợ tài chính để đi học.</strong> 
</div>
        </div>
        <div class="col-sm-12 col-md-12 col-lg-6 col-xl-6 right">
            <div class="quizzes-title">Thử sức với khả năng tư duy của bạn: Are you one of us?</div>
            <div class="quizzes-desc"><img src = 'https://firebasestorage.googleapis.com/v0/b/clubfair2021.appspot.com/o/image1.png?alt=media&token=e5005836-8223-4777-a337-7af5024af05c'></div>
            <div class="quizzes-href"><a href = 'https://docs.google.com/forms/d/e/1FAIpQLScgKVoqJyz1V_zxcu9xU3ghbga6p78Tuan00QtWW_jFp4ltTg/viewform'>Nộp câu trả lời ở đây →</a></div>
        </div>
    </div>
    <div class="row quizzes-row"  v-if="hasQuiz">
        <div class="col-sm-12 col-md-12 col-lg-6 col-xl-6 left">
            <div class="quizzes-title">Thử sức với khả năng sáng tạo của bạn:</div>
            <div class="quizzes-desc">Can you think of all the usage for paper cups? The more usage you can think of, the higher your reward will be! </div>
             <div class="quizzes-href"><a href = '/1000-ngay-o-ams'>List your answers here →</a></div>
             <div class="quizzes-desc"><img src = 'https://firebasestorage.googleapis.com/v0/b/clubfair2021.appspot.com/o/image2.png?alt=media&token=c4005a31-abda-4b5c-b720-b63e4bf22dbb'></div>
        </div>
        <div class="col-sm-12 col-md-12 col-lg-6 col-xl-6 right last">
            <div class="quizzes-title">Tìm hiểu thêm thông tin tại:<br>https://www.minerva.edu/</div>
            <div class="quizzes-desc">Hạn nộp hồ sơ cho Khóa 2026:<br>
Early Action: 01/11/2022<br>
Regular Decision 1: 15/01/2022<br>
Regular Decision 2: 15/03/2022<br>
<br>
Hoặc liên hệ: <br>
Trần Hà Trang - Đại diện Đông Nam Á<br>
tranghatran@minerva.edu<br>
</div>
             <!-- <div class="quizzes-href"><a href = 'https://l.messenger.com/l.php?u=http%3A%2F%2Fwww.quiz-maker.com%2FQTQZDBOV8&h=AT2snhO5ub-2jTnv2r4rF3zjEkeBk7Ax2h0yS-lcLUni_7IVtun_iTPVbXDVtlEbRe5ofhRPRinM4a8SYQ-qKlbVwPZmx05QhutjzQYagQ2ezXPJ9pfDQzYnjjJ0UMjdMnITwrTYrEEtl798M2BaPg'>Tham gia Quiz →</a></div> -->
        </div>
    </div>

    <div class = 'explore-clubs'><a href = '/'>Khám phá các CLB</a></div>
</div>
</template>

<script>
import { gsap, Power4, Back, Power0 } from "gsap"
export default {
    name: 'Minerva',
    data() {
        return {
            hasQuiz: true
        }
    },
    methods: {
        transition() {
            var that = this
            var tl = gsap.timeline()
            tl.to('.title', {opacity: 0, y: -20, duration: 1.5, ease: Power4.easeOut, onComplete: function() {
                that.hasQuiz = true
            }})
        }
    }
}
</script>

<style lang = 'scss' scoped>

.title {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}

.title-quiz {
    font-size: 3rem;
    padding-bottom: 3rem;
}

.enter-quiz-button {
    padding: 0.5rem 2rem 0.5rem 2rem;
    background: black;
    color: white;
    cursor: pointer;
    border-radius: 5rem;
    border: 1px solid black
}

.enter-quiz-button:hover {
    background: white;
    color: black
}
.quizzes {
    width: 100vw;
    height: 100%;
    background: white;
    color: black;
}

.quizzes-row {
    /* height: 50vh; */
    text-align: left;
}

.top {
    border-bottom: 1px solid black;
}

.left {
    border-right: 1px solid black;
}

.quizzes-title {
    font-size: 3rem;
    padding-bottom: 2rem;
    padding-left: 1rem;
    padding-top: 1rem;
}

.quizzes-desc {
    padding-left:1rem;
}

.quizzes-href {
    font-size: 2rem;
    padding-top: 3rem;
    padding-bottom: 3rem;
    padding-left: 1rem;

    a {
        color: black;
        text-decoration: none !important;
        position: relative;
        transition: all 0.5s ease;
    }

    a:hover {
        color: #ffdb13;
    }
}

.quizzes-desc img {
    max-width: 80%;
    padding-bottom: 2rem;
}

@media screen and (max-width: 992px) {
    .top {
        border: 0;
    }

    .left {
        border: 0;
        border-bottom: 1px solid black;
    }

    .right {
        border: 0;
        border-bottom: 1px solid black;
    }
}

.last {
    padding-bottom: 4rem;
}

.explore-clubs {
    background: black;
    color: white;
    position: fixed;
    bottom: 2rem;
    right: 2rem;
    padding: 1rem 2rem 1rem 2rem;
    border-radius: 5rem;
    border: 1px solid black;
    transition: all 0.5s ease;

    a {
        color: white;
        text-decoration: none !important;
    }
}

.explore-clubs:hover {
    background: white;
    a {
        color: black;
    }
}

@media screen and (max-width: 576px) {
    .quizzes-title {
        font-size: 2.5rem;
        padding-left: 0rem;
    }

    .quizzes-desc {
        padding-left: 0rem;
    }

    .quizzes-href {
        padding-left: 0rem;
        font-size: 1.5rem;
    }
}
</style>