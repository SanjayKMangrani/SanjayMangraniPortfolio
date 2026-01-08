<template>
<div class="banner-1">
    <!-- NavBar -->
    <nav class="container px-6 mx-auto md:flex md:justify-between md:items-center">
        <div class="flex items-center justify-between">
            <div class="relative w-16 h-16">
                <img class="rounded-full border border-gray-100 shadow-sm" src="./assets/Mypic.png" alt="user image" />
            </div>
            <!-- Mobile menu button -->
            <div @click="showMenu = !showMenu" class="flex md:hidden">
                <button type="button" class="text-gray-800 hover:text-gray-400 focus:outline-none focus:text-gray-400">
                    <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                        <path fill-rule="evenodd" d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"></path>
                    </svg>
                </button>
            </div>
        </div>
        <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
        <ul :class="showMenu ? 'flex' : 'hidden'" class="flex-col items-end mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0">
            <li class="menu-button"><a href="#">Home</a></li>
            <li class="menu-button"><a href="#work" v-smooth-scroll>Works</a></li>
            <li class="menu-button">
                <a href="#employment-history" v-smooth-scroll>Employment</a>
            </li>
            <li class="menu-button"><a href="#about" v-smooth-scroll>About</a></li>
        </ul>
    </nav>
    <!-- End Navbar -->

    <div class="flex items-center">
        <div class="w-11/12 space-y-5 md:space-y-10">
            <h3 class="hello-button text-gray-700 w-fit md:py-3 md:px-5 py-1 px-2 rounded-lg 3xl:text-3xl 2xl:text-xl lg:text-xl md:text-md text-sm font-semibold font-work_sans">
                👋 Hola,
            </h3>
            <h1 class="3xl:text-8xl 2xl:text-7xl xl:text-6xl lg:text-4xl md:text-3xl sm:text-3xl text-xl font-Eczar font-bold leading-tight text-gray-700">
                It's
                <a href="https://www.linkedin.com/in/sanjay-kumar-639099158/" target="_blank" class="text-black hover:underline">
                    Sanjay Kumar</a><br />Web Developer
            </h1>

            <div class="md:flex gap-1 md:gap-10">
                <a href="#work" v-smooth-scroll><button class="text-white bg-gray-800 submit-button hidden md:block">
                        View my Work
                    </button></a>
                <a href="#contact" v-smooth-scroll><button class="text-gray-800 border-4 border-gray-800 submit-button mb-5 md:mb-0">
                        Contact Me
                    </button></a>
            </div>
        </div>

        <div class="w-8/12 flex justify-end">
            <img class="3xl:h-[800px] 2xl:h-[650px] xl:h-[550px] lg:h-[550px] md:h-[450px] sm:h-[350px] rounded-full" src="./assets/Mypic.png" alt="user image" />
        </div>
    </div>
</div>

<div class="banner-2 space-y-10 pb-20" id="work">
    <h3 class="heading3 my-5">My Recent Work</h3>
<div class="card flex">
    <!-- AI Retail Forecasting Dashboard Project -->
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-3/5">
        <h4 class="project-title item">AI Retail Forecasting Dashboard</h4>
        <p class="font-work_sans pr-12 text-justify">
            A full-stack machine learning dashboard that forecasts next-day retail sales and flags potential low-sales-risk days from raw Excel datasets. Designed for business teams to monitor sales trends and improve decision-making.
            <br /><br /><strong>Technologies Used:</strong>
            <ul class="list-disc pl-6">
                <li>Pandas + scikit-learn for time-based feature engineering and ML pipelines.</li>
                <li>Flask for serving the dashboard as a web app.</li>
                <li>HTML/CSS (Jinja templates) for the frontend.</li>
            </ul>
            <br />
            <strong>Real-World Use Case:</strong> Retail managers or analysts can upload raw Excel sales files and instantly view predictive insights for planning promotions, inventory, or staffing.
        </p>
        <div class="flex gap-4 pt-2">
            <a href=" https://github.com/SanjayKMangrani/ai-retail-dashboard" target="_blank">
                <button class="bg-gray-800 text-white px-5 py-2 rounded hover:bg-gray-700">
                    GitHub Code
                </button>
            </a>
            <!-- Optional Live Demo button
            <a href="https://your-live-demo-url.com/" target="_blank">
                <button class="bg-sky-600 text-white px-5 py-2 rounded hover:bg-sky-500">
                    Live Demo
                </button>
            </a>
            -->
        </div>
    </div>

    <div class="card-images-container bg-white-100 p-4 md:w-2/5 flex items-center justify-center">
        <a href="./assets/RetailDashboard.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover rounded shadow-md" src="./assets/RetailDashboard.png" alt="Retail Forecasting Screenshot" />
        </a>
    </div>
</div>

    <div class="card flex">
    <!-- PhoneGradeAI Project -->
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-3/5">
        <h4 class="project-title item">PhoneGradeAI - Mobile Screen Condition Classifier</h4>
        <p class="font-work_sans pr-12 text-justify">
            A deep learning-powered application that classifies mobile phone screen conditions as either cracked or intact. Designed for integration into automated inspection systems, such as refurbishment lines or resale evaluation tools.
            <br /><br /><strong>Technologies Used:</strong>
            <ul class="list-disc pl-6">
                <li>TensorFlow + Keras for training a binary image classifier (CNN).</li>
                <li>Flask for backend API handling predictions.</li>
                <li>Streamlit for a simple, interactive user interface.</li>
            </ul>
            <br />
            <strong>Real-World Use Case:</strong> Can be installed in inspection pipelines using camera sensors on conveyor belts to identify damaged phone screens in real time.
        </p>
        <div class="flex gap-4 pt-2">
            <a href="https://github.com/SanjayKMangrani/PhoneGradeAI" target="_blank">
                <button class="bg-gray-800 text-white px-5 py-2 rounded hover:bg-gray-700">
                    GitHub Code
                </button>
            </a>
            <a href="https://phonegrade-frontend-production.up.railway.app/" target="_blank">
                <button class="bg-sky-600 text-white px-5 py-2 rounded hover:bg-sky-500">
                    Live Demo
                </button>
            </a>
        </div>
    </div>

    <div class="card-images-container bg-white-100 p-4 md:w-2/5 flex items-center justify-center">
        <a href="./assets/PhoneGradAi.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover rounded shadow-md" src="./assets/PhoneGradAi.png" alt="PhoneGradeAI Screenshot" />
        </a>
    </div>
</div>
    
    <div class="card flex">
    <!-- PDF Chatbot Project -->
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-2/4">
      <h4 class="project-title item">PDF Chatbot Application</h4>
      <p class="font-work_sans pr-12 text-justify">
        A chatbot that can analyze and answer questions from your uploaded PDF files. Built with Flask and LangChain for powerful AI-driven document comprehension.
        <br /><br /><strong>Technologies Used:</strong>
        <ul class="list-disc pl-6">
          <li>Flask for backend server and API development.</li>
          <li>LangChain for processing and understanding PDF documents.</li>
          <li>HTML, CSS, JavaScript for the interactive frontend UI.</li>
          <li>REST API for communication between frontend and backend.</li>
        </ul>
      </p>
      <a href="https://github.com/SanjayKMangrani/PdfChatbot" target="_blank" class="mt-6 inline-block">
        <button class="bg-gray-800 text-white px-5 py-2 rounded hover:bg-gray-700">
            GitHub Code
        </button>
      </a>
    </div>
    
    <div class="card-images-container flex flex-col space-y-4 bg-white-100 p-4 md:w-2/4">
      <a href="./assets/PDFChatbot1.png" target="_blank" class="block w-full">
        <img class="w-full h-auto object-cover" src="./assets/PdfChatbot.png" alt="PDF Chatbot Screenshot 1" />
      </a>
    </div>
  </div>
    
    <div class="card flex">
    <!-- LLM Chatbot Project -->
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-2/4">
        <h4 class="project-title item">LLM Chatbot Application</h4>
        <p class="font-work_sans pr-12 text-justify">
            A conversational AI chatbot leveraging IBM Watson and Hugging Face models for intelligent dialogue. Deployed as a web service using Flask, integrating a Vue.js frontend.
            <br /><br /><strong>Technologies Used:</strong>
            <ul class="list-disc pl-6">
                <li>IBM Watson and Hugging Face for LLM-based chatbot responses.</li>
                <li>Flask for backend server deployment.</li>
                <li>Vue.js for interactive frontend UI.</li>
                <li>REST API integration for chatbot communication.</li>
            </ul>
        </p>
        <a href="https://github.com/SanjayKMangrani/LLM_Chatbot.git" target="_blank" class="mt-6 inline-block">
            <button class="bg-gray-800 text-white px-5 py-2 rounded hover:bg-gray-700">
                GitHub Code
            </button>
        </a>
    </div>

    <!-- Chatbot Output Images -->
    <div class="card-images-container flex flex-col space-y-4 bg-white-100 p-4 md:w-2/4">
        <a href="chatBot.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover" src="./assets/chatBot.png" alt="LLM Chatbot Screenshot 1" />
        </a>
    </div>
</div>

    <div class="card flex">
    <!-- Emotion Detection Project -->
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-2/4">
        <h4 class="project-title item">Emotion Detection Application</h4>
        <p class="font-work_sans pr-12 text-justify">
            An advanced emotion detection application using Watson NLP, extracting emotions like joy, sadness, and anger. Deployed as a web service using Flask.
            <br /><br /><strong>Technologies Used:</strong>
            <ul class="list-disc pl-6">
                <li>Watson NLP for emotion detection.</li>
                <li>Flask for web deployment.</li>
                <li>Python for backend logic.</li>
                <li>Static code analysis for PEP8 compliance.</li>
            </ul>
        </p>
        <a href="https://github.com/SanjayKMangrani/EmotionDetection.git" target="_blank" class="mt-6 inline-block">
            <button class="bg-gray-800 text-white px-5 py-2 rounded hover:bg-gray-700">
                GitHub Code
            </button>
        </a>
    </div>
    
    <div class="card-images-container flex flex-col space-y-4 bg-white-100 p-4 md:w-2/4">
        <a href="./assets/ED1.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover" src="./assets/ED1.png" alt="Emotion Detection Screenshot 1" />
        </a>
        <a href="./assets/ED2.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover" src="./assets/ED2.png" alt="Emotion Detection Screenshot 2" />
        </a>
    </div>
</div>

    <div class="card flex">
    <!-- Sentiment Analysis Project -->
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-2/4">
        <h4 class="project-title item">Sentiment Analysis Application</h4>
        <p class="font-work_sans pr-12 text-justify">
            A sentiment analysis application using Watson NLP embedded libraries and Flask. The project extracts relevant information from Watson's responses and deploys it as a web application.
            <br /><br /><strong>Technologies Used:</strong>
            <ul class="list-disc pl-6">
                <li>Watson NLP for sentiment analysis.</li>
                <li>Flask for web deployment.</li>
                <li>Python for application logic.</li>
                <li>Unit testing for validation.</li>
            </ul>
        </p>
        <a href="https://github.com/SanjayKMangrani/SentimentAnalysis.git" target="_blank" class="mt-6 inline-block">
            <button class="bg-gray-800 text-white px-5 py-2 rounded hover:bg-gray-700">
                GitHub Code
            </button>
        </a>
    </div>
    
    <div class="card-images-container flex flex-col space-y-4 bg-white-100 p-4 md:w-2/4">
        <a href="./assets/NLP1.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover" src="./assets/NLP1.png" alt="Sentiment Analysis Screenshot 1" />
        </a>
        <a href="./assets/NLP2.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover" src="./assets/NLP2.png" alt="Sentiment Analysis Screenshot 2" />
        </a>
    </div>
</div>

    <div class="card flex">
    <!-- Project Description Section -->
    <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-2/4">
        <h4 class="project-title item">Recipe Sharing - Full Stack Web Application</h4>
        <p class="font-work_sans pr-12 text-justify">
            A full-stack recipe-sharing web application built using ASP.Net Core Web API, React JS, and SQL Server. Users can register, log in, and share their favorite recipes. The project includes user authentication, recipe creation, and recipe viewing functionality, all managed through a RESTful API and a modern frontend built with React JS.
            <br /><br /><strong>Technologies Used:</strong>
            <ul class="list-disc pl-6">
                <li>ASP.Net Core Web API for backend development.</li>
                <li>React JS for building a responsive and interactive frontend.</li>
                <li>SQL Server with Entity Framework Core for database management and operations.</li>
                <li>JWT for secure user authentication and session management.</li>
                <li>Postman for API testing and documentation.</li>
            </ul>
        </p>
        <a href="https://github.com/SanjayKMangrani/RecipeSharingProject" target="_blank" class="mt-6 inline-block">
            <button class="bg-gray-800 text-white px-5 py-2 rounded hover:bg-gray-700">
                GitHub Code
            </button>
        </a>
    </div>
    
    <div class="card-images-container flex flex-col space-y-4 bg-white-100 p-4 md:w-2/4">
        <!-- First Image -->
        <a href="./assets/Login.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover" src="./assets/Login.png" alt="Recipe Sharing Login" />
        </a>
        
        <!-- Second Image -->
        <a href="./assets/RecipeSharing.png" target="_blank" class="block w-full">
            <img class="w-full h-auto object-cover" src="./assets/RecipeSharing.png" alt="Recipe Sharing Recipe" />
        </a>
    </div>
</div>

    <div class="card">
        <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
            <h4 class="project-title item">Vue Task Tracker</h4>
            <p class="font-work_sans pr-12 text-justify">
                Developed a Task Management System with a Vue.js frontend and ASP.NET Core backend. The system allows users to manage tasks, view details, and perform CRUD operations. Implemented features include task listing, details, due dates, and status updates.
                <br /><br /><strong>Working On:</strong>
                <ul class="list-disc pl-6">
                    <li>Integration with Azure for secure and scalable hosting.</li>
                    <li>Enhanced RESTful API capabilities for seamless data interaction.</li>
                    <li>User authentication and authorization for secure task management.</li>
                </ul>
                <br /><strong>Technologies Used:</strong>
                <ul class="list-disc pl-6">
                    <li>Vue.js for the frontend.</li>
                    <li>ASP.NET Core for backend development.</li>
                    <li>Integration of CRUD operations for task management.</li>
                    <li>Database integration for storing task information.</li>
                </ul>
            </p>
            <a href="https://github.com/SanjayKMangrani/VueTaskTracker/blob/main/README.md" target="_blank" class="mt-6 inline-block"> <button class="bg-gray-800 text-white px-5 py-2 rounded hover:bg-gray-700">
                    GitHub Code
                </button></a>
        </div>
        <div class="card-image bg-green-100">
            <img class="w-full h-72 md:h-96" src="./assets/TaskProject.png" alt="Project Image">
        </div>
    </div>
</div>

<div class="banner-1" id="employment-history">
    <div class="space-y-4 grid place-items-center mt-5">
        <h3 class="heading3">Employment History</h3>
    </div>
    <div class="max-w-6xl mx-auto px-8 py-16">
        <div class="flex flex-col md:flex-row space-y-6 md:space-y-0 md:space-x-6">
            <!-- Adwani Motors Limited -->
            <div class="flex flex-col md:flex-1 bg-white p-8 rounded-lg shadow-md">
                <h4 class="font-bold text-2xl mb-4">Junior Web Developer (Part-Time), Adwani Motors Limited</h4>
                <p class="mb-4">Dec. 2023 – Present, Middlesbrough, UK</p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Developed an AI-driven chatbot to assist customers in finding products and answering queries, enhancing user interaction.</li>
                    <li>Integrated a machine learning-based recommendation system to suggest relevant vehicle options based on browsing behavior.</li>
                    <li>Implemented sentiment and emotion analysis features to enhance customer insights and feedback mechanisms.</li>
                    <li>Assisted in SQL Server database management, ensuring data integrity for AI-driven insights.</li>
                    <li>Participated in Agile development, contributing to sprint planning and collaborative development processes.</li>
                </ul>
            </div>
            
            <!-- BASF Asia-Pacific -->
            <div class="flex flex-col md:flex-1 bg-white p-8 rounded-lg shadow-md">
                <h4 class="font-bold text-2xl mb-4">Web Developer, BASF Asia-Pacific Service Centre Sdn Bhd</h4>
                <p class="mb-4">March 2020 – Dec. 2021, Kuala Lumpur, Malaysia</p>
                <ul class="list-disc pl-6 space-y-2">
                    <li>Spearheaded coding, design, and implementation of in-house web and mobile portals, driving enhanced user experiences and streamlined processes.</li>
                    <li>Collaborated with cross-functional teams to gather and understand end-user requirements, translating them into functional and technical specifications.</li>
                    <li>Designed the MY Desk KL App, enabling employees to reserve seats for office use during the pandemic. Implemented features like seat allocation optimization, email notifications, and administrative controls.</li>
                    <li>Contributed to the development of the APTC Trade Portal in a front-end capacity, applying proficiency in Bootstrap, HTML, CSS, and JavaScript to design user-friendly web pages.</li>
                </ul>
            </div>
        </div>
    </div>
</div>

<div class="banner-1 flex h-full items-center" id="contact">
    <div class="w-7/12 p-12">
        <h2 class="text-gray-700 md:text-6xl text-2xl font-Eczar mb-5 font-bold">
            Let’s work together and make everything super cute and super useful.
        </h2>
        <a class="underline text-2xl text-blue-600 font-work_sans">📧 sanjaykmangrani@gmail.com</a>
    </div>
    <div class="w-5/12 pr-28">
        <div class="flex flex-wrap justify-end gap-2">
            <button class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center space-x-2 rounded">
                <svg class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10 fill-current" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                    <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z" />
                </svg>
            </button>

            <button class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center space-x-2 rounded">
                <svg class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10 fill-current" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                    <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z" />
                </svg>
            </button>

            <button class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center space-x-2 rounded">
                <svg class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10 fill-current" role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path d="M12 0A12 12 0 0 0 0 12a12 12 0 0 0 12 12 12 12 0 0 0 12-12A12 12 0 0 0 12 0zm5.01 4.744c.688 0 1.25.561 1.25 1.249a1.25 1.25 0 0 1-2.498.056l-2.597-.547-.8 3.747c1.824.07 3.48.632 4.674 1.488.308-.309.73-.491 1.207-.491.968 0 1.754.786 1.754 1.754 0 .716-.435 1.333-1.01 1.614a3.111 3.111 0 0 1 .042.52c0 2.694-3.13 4.87-7.004 4.87-3.874 0-7.004-2.176-7.004-4.87 0-.183.015-.366.043-.534A1.748 1.748 0 0 1 4.028 12c0-.968.786-1.754 1.754-1.754.463 0 .898.196 1.207.49 1.207-.883 2.878-1.43 4.744-1.487l.885-4.182a.342.342 0 0 1 .14-.197.35.35 0 0 1 .238-.042l2.906.617a1.214 1.214 0 0 1 1.108-.701zM9.25 12C8.561 12 8 12.562 8 13.25c0 .687.561 1.248 1.25 1.248.687 0 1.248-.561 1.248-1.249 0-.688-.561-1.249-1.249-1.249zm5.5 0c-.687 0-1.248.561-1.248 1.25 0 .687.561 1.248 1.249 1.248.688 0 1.249-.561 1.249-1.249 0-.687-.562-1.249-1.25-1.249zm-5.466 3.99a.327.327 0 0 0-.231.094.33.33 0 0 0 0 .463c.842.842 2.484.913 2.961.913.477 0 2.105-.056 2.961-.913a.361.361 0 0 0 .029-.463.33.33 0 0 0-.464 0c-.547.533-1.684.73-2.512.73-.828 0-1.979-.196-2.512-.73a.326.326 0 0 0-.232-.095z" />
                </svg>
            </button>

            <button class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center space-x-2 rounded">
                <svg class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10 fill-current" role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path d="M12.017 0C5.396 0 .029 5.367.029 11.987c0 5.079 3.158 9.417 7.618 11.162-.105-.949-.199-2.403.041-3.439.219-.937 1.406-5.957 1.406-5.957s-.359-.72-.359-1.781c0-1.663.967-2.911 2.168-2.911 1.024 0 1.518.769 1.518 1.688 0 1.029-.653 2.567-.992 3.992-.285 1.193.6 2.165 1.775 2.165 2.128 0 3.768-2.245 3.768-5.487 0-2.861-2.063-4.869-5.008-4.869-3.41 0-5.409 2.562-5.409 5.199 0 1.033.394 2.143.889 2.741.099.12.112.225.085.345-.09.375-.293 1.199-.334 1.363-.053.225-.172.271-.401.165-1.495-.69-2.433-2.878-2.433-4.646 0-3.776 2.748-7.252 7.92-7.252 4.158 0 7.392 2.967 7.392 6.923 0 4.135-2.607 7.462-6.233 7.462-1.214 0-2.354-.629-2.758-1.379l-.749 2.848c-.269 1.045-1.004 2.352-1.498 3.146 1.123.345 2.306.535 3.55.535 6.607 0 11.985-5.365 11.985-11.987C23.97 5.39 18.592.026 11.985.026L12.017 0z" />
                </svg>
            </button>

            <button class="bg-gray-700 p-2 font-semibold text-white inline-flex items-center space-x-2 rounded">
                <svg class="w-4 h-4 md:w-10 md:h-10 lg:w-10 lg:h-10 xl:h-10 xl:w-10 fill-current" role="img" viewBox="0 0 256 256" xmlns="http://www.w3.org/2000/svg">
                    <g>
                        <path d="M218.123122,218.127392 L180.191928,218.127392 L180.191928,158.724263 C180.191928,144.559023 179.939053,126.323993 160.463756,126.323993 C140.707926,126.323993 137.685284,141.757585 137.685284,157.692986 L137.685284,218.123441 L99.7540894,218.123441 L99.7540894,95.9665207 L136.168036,95.9665207 L136.168036,112.660562 L136.677736,112.660562 C144.102746,99.9650027 157.908637,92.3824528 172.605689,92.9280076 C211.050535,92.9280076 218.138927,118.216023 218.138927,151.114151 L218.123122,218.127392 Z M56.9550587,79.2685282 C44.7981969,79.2707099 34.9413443,69.4171797 34.9391618,57.260052 C34.93698,45.1029244 44.7902948,35.2458562 56.9471566,35.2436736 C69.1040185,35.2414916 78.9608713,45.0950217 78.963054,57.2521493 C78.9641017,63.090208 76.6459976,68.6895714 72.5186979,72.8184433 C68.3913982,76.9473153 62.7929898,79.26748 56.9550587,79.2685282 M75.9206558,218.127392 L37.94995,218.127392 L37.94995,95.9665207 L75.9206558,95.9665207 L75.9206558,218.127392 Z M237.033403,0.0182577091 L18.8895249,0.0182577091 C8.57959469,-0.0980923971 0.124827038,8.16056231 -0.001,18.4706066 L-0.001,237.524091 C0.120519052,247.839103 8.57460631,256.105934 18.8895249,255.9977 L237.033403,255.9977 C247.368728,256.125818 255.855922,247.859464 255.999,237.524091 L255.999,18.4548016 C255.851624,8.12438979 247.363742,-0.133792868 237.033403,0.000790807055"></path>
                    </g>
                </svg>
            </button>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            showMenu: false,
        }
    },
}
</script>
<style scoped>
.card-images-container {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.card-images-container img {
  width: 100%; /* Makes the image take the full width of its container */
  height: auto; /* Maintains the aspect ratio of the image */
  object-fit: cover;
  border-radius: 8px; /* Optional: adds rounded corners */
}

.card-images-container a {
  display: block;
  width: 100%; /* Ensures the anchor takes the full width of its container */
  overflow: hidden; /* Ensures images stay within the container */
}
</style>
