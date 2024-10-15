<template>
  <div class="scene">
    <div class="carousel">
      <div class="carousel__face box" v-for="(item, index) in carouselItems" :key="index" :style="`--i:${index}`">
        <img class="img-fluid" :src="item.image" :alt="`Cover ${index + 1}`">
        <h3 class="carousel__title">{{ item.title }}</h3>
        <button class="view-btn" @click="openModal(item.modalImage)">View More</button>
      </div>
    </div>

    <!-- Modal Structure -->
    <div id="myModal" class="modal" v-if="isModalOpen">
      <span class="close" @click="closeModal">&times;</span>
      <img class="modal-content" :src="modalImage" alt="Modal Image">
      <div class="caption">{{ modalCaption }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isModalOpen: false,
      modalImage: '',
      modalCaption: '',
      carouselItems: [
        {
          title: 'Introduction To AWS Cloud',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Intro .png'
        },
        {
          title: 'Why We Use AWS',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Why AWS.png'
        },
        {
          title: 'AWS Job Roles',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Job Roles.png'
        },
        {
          title: 'Demystifying Generative AI',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Demystifying Generative AI.png'
        },
        {
          title: 'Cloud Foundations Part 1',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - CF Part 1.png'
        },
        {
          title: 'Cloud Foundations Part 2',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - CF Part 2.png'
        },
        {
          title: 'Cloud Foundations Part 3',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - CF Part 3.png'
        },
        {
          title: 'Cloud Foundations Part 4',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - CF Part 4.png'
        },
        {
          title: 'Become A Cloud Practioner Part 1',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Part 1.png'
        },
        {
          title: 'Becoming A Cloud Practioner Part 2',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Part 2.png'
        },
        {
          title: 'Becoming A Cloud Practioner Part 3',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Part 3.png'
        },
        {
          title: 'Becoming A Cloud Practioner Part 4',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - BCP Part 4.png'
        },
        {
          title: 'Becoming A Cloud Career',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Building a cloud career.png'
        },
        {
          title: 'AWS Exam Preparations',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - Exam Prep.png'
        },
        {
          title: 'Becoming A Cloud Practioner Labs',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/AWS-logo.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/AWS Certifications/AWS Completion - BCP Lab .png'
        },
        
        // Learnify Certificates
        {
          title: 'Body Language Basics',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Body-Language.jpg'
        },
        {
          title: 'Communication Strategies',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Communication-Strategies.jpg'
        },
        {
          title: 'Critical Thinking',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Critical-Thinking.jpg'
        },
        {
          title: 'Emotional Intelligence',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Emotional-Intelligence.jpg'
        },
        {
          title: 'Goal Setting',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Goal-Setting.jpg'
        },
        {
          title: 'Improving Self-Awareness',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Imporving-Self-Awareness.jpg'
        },
        {
          title: 'Negotiation Skills',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Negotiation-skills.jpg'
        },
        {
          title: 'Self Leadership',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Self-Leadership.jpg'
        },
        {
          title: 'Work Life Balance',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/Learnify3.jpg',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Learnify-Certificates/Work-Life-Balance.jpg'
        },

//Udemy
        {
          title: 'Full Stack Web Developer',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/udemy3.png',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Udemy FSD.jpg'
        },

//LifeChoices
        {
          title: 'Cisco Linux Unhatched',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/LC.png',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Cisco/Linux-Unhatched.png'
        },
        {
          title: 'Cisco Operating Systems',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/LC.png',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Cisco/Operating Systems Basics.png'
        },
         {
          title: 'Full Stack Web Developer',
          image: 'https://joshua-langeveldt.github.io/Global-Images/images/Logo/LC.png',
          modalImage: 'https://joshua-langeveldt.github.io/Global-Images/images/Certifications/Cisco/Linux-Unhatched.png'
        }
      ],
    };
  },
  methods: {
    openModal(image) {
      this.modalImage = image;
      this.isModalOpen = true;
    },
    closeModal() {
      this.isModalOpen = false;
      this.modalImage = '';
    },
  },
};
</script>

<style scoped>
body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
}

.scene {
  width: 120px; /* Smaller size */
  height: 180px; /* Smaller size */
  perspective: 1300px; /* Suitable perspective for smaller carousel */
}

.carousel {
  left:34rem;
  width: 120%;
  height: 100%;
  position: relative;
  margin-top: 8rem;
  transform-style: preserve-3d;
  animation: spin 50s infinite linear; /* Slower spin for more slots */
  animation-play-state: running; /* Animation is running by default */
}

.carousel__face {
  position: absolute;
  width: 100%;
  height: 85%;
/*   backface-visibility: hidden; */
  border: 1px solid white;
  border-radius: 0.5rem;
  transform: rotateY(calc(var(--i) * 12.86deg)) translateZ(565px); /* Adjusted translateZ to fit */
  overflow: hidden;
  transition: transform 5s ease-out;
}

.carousel__face img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 0.5rem;
  transition: filter 0.3s ease;
}



/* Hidden by default */
.carousel__title,
.view-btn {
  position: absolute;
  color: white;
  opacity: 0;
  transition: opacity 0.3s ease;
  z-index: 10;
}

.carousel__title {
  top: 30%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 1.1rem;
  font-weight: 400;
  text-align: center;
}

.view-btn {
  top: 70%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 6px 10px;
  background-color: #0A0D12;
  border: none;
  font-size: 0.5rem;
  font-weight: 300;
  border-radius: 5px;
  margin-top: 0.5rem;
  cursor: pointer;
}

view-btn:hover{
    background-color: #141C27;
    color: #84A7A1;
    box-shadow: 0 10px 15px rgba(0, 0, 0, 0.7);
    transition: 0.2s;
    transform: scale(1.1);
}

.carousel__face:hover img {
  filter: blur(5px);
}

.carousel__face:hover .carousel__title,
.carousel__face:hover .view-btn {
  opacity: 1;
  overflow:hidden;
}


.scene:hover .carousel {
  animation-play-state: paused; /* Pauses the spin animation */
}

@keyframes spin {
  from {
    transform: rotateY(0deg);
  }
  to {
    transform: rotateY(360deg);
  }
}

/* Modal styles */
.modal {
    display: none;
    position: absolute;
    z-index: 1;
    left: -9rem;
    top: -3.6rem;
    width: 380%;
    height: 300%;
    overflow: hidden;
    border-radius: 10px;
    background-color: rgba(0, 0, 0, 0.8);
}

.modal-content {
    display: block;
    margin: 0% auto;
    max-width: 100%;
    border-radius: 10px;
    object-postion: center;
  object-fit:cover;
}

.close {
    position: absolute;
    top: -5px;
    right: 0px;
    color: #000;
    font-size: 50px;
    font-weight: bold;
    cursor: pointer;
}

</style>
