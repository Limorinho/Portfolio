<script lang="ts">

import linor from '$lib/images/linor.png';
import UiA from '$lib/images/UiA.jpg';
import github from '$lib/images/github.jpg';

</script>


	<h1 class="text-indigo-500 font-bold">About me
    
  </h1>

    <div class="py-6 sm:py-8 lg:py-12">
      <div class="mx-auto max-w-screen-xl px-4 md:px-8">
        <div class="grid gap-8 md:grid-cols-3 lg:gap-12 ">
        <div>
          
          <div class="w-full max-w-xl mx-auto mt-5">
            
                <!-- person - start -->
    <div class="flex flex-col place-items-center">
      <div class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32">
        <img src={linor} loading="lazy" alt="Photo of me" class="h-full w-full object-cover object-center" />
      </div>

      <div>
        <div class="text-center font-bold text-indigo-500 md:text-lg">Linor Ujkani</div>
        <p class="mb-3 text-center text-sm md:mb-4 md:text-base">CS graduate • Software engineer</p>

        <!-- social - start -->
        <div class="flex justify-center">
          <div class="flex gap-4">
            <a href="#" target="_blank" class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600">
              <svg class="h-5 w-5" width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z" />
              </svg>
            </a>

            <a href="#" target="_blank" class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600">
              <svg class="h-5 w-5" width="24" height="24" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z" />
              </svg>
            </a>
          </div>
        </div>
        <!-- social - end -->
      </div>

            <div class="p-3 text-center font-bold text-indigo-500 md:text-lg">Education</div>
      <ul class="space-y-4">
        <li>
          <strong>Bachelor’s in Computer Science</strong><br>
          [UiA, Grimstad], Graduated 2025
        </li>
        <li>
          <strong>Master’s in Artificial Intelligence</strong><br>
          [UiA, Grimstad], Expected 2027
        </li>
      </ul>

    </div>

            </div>
    
        </div>
      
        <div class="md:pt-4 col-span-2">

          <p class="mb-6 sm:text-lg md:mb-8">
            I’m a software developer with a bachelor’s degree in Computer Science, currently advancing my expertise through a Master’s in Artificial Intelligence.
          </p>
          <p class="mb-6 sm:text-lg md:mb-8">
            In my spare time, I love building new projects, diving into thought-provoking books, and exploring ideas on YouTube. My passion for programming has inspired me to create a variety of personal projects — many of which you can explore here!
          </p>
          <p class="mb-6 sm:text-lg md:mb-8">
            Most of my projects center around web development, automation, and playful experiments with technology. I’ve built everything from movie blogs and restaurant sites to tournament systems and Discord bots. Whether it’s using .NET for data-driven apps, Python for scraping and automation, or Godot for retro-style games, I enjoy learning by doing and exploring different tools to bring ideas to life.
          </p>
        </div>
    
        </div>
        </div>
      </div>

      <h1 class="pb-12 font-bold text-indigo-500">Experience</h1>
<div class="place-items-center">
      <ul class="space-y-8 px-8">
        <li class="flex items-start gap-4">
          <img src={UiA} alt="UiA Logo" class="w-12 h-12 rounded-lg object-cover">
          <div>
            <strong>Student Assistant</strong><br>
            UiA | Fall 2023 - Spring 2024
            <ul class="list-disc list-inside">
              <li>Assisted professors in Operative Systems (IKT102) & Microcontrollers (IKT104)</li>
              <li>Guided students in labs & reviewed assignments</li>
            </ul>
          </div>
        </li>
        <li class="flex items-start gap-4">
          <img src={github} alt="Freelance Icon" class="w-12 h-12 rounded-lg object-cover">
          <div>
            <strong>Freelance Developer</strong><br>
            2021 - Present
            <ul class="list-disc list-inside">
              <li>Built responsive websites for small businesses with PHP & MySQL</li>
              <li>Created open-source projects for the developer community on Github</li>
            </ul>
          </div>
        </li>
      </ul>
    </div>
         
      <h1 class="py-12 text-indigo-500">Technologies</h1>

      <div class="grid grid-cols-4 sm:grid-cols-4 gap-12 text-center text-gray-300">
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" class="h-12 mx-auto" alt="Python"/>
          <p>Python</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/svelte/svelte-original.svg" class="h-12 mx-auto" alt="Svelte"/>
          <p>Svelte</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" class="h-12 mx-auto" alt="JavaScript"/>
          <p>JavaScript</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" class="h-12 mx-auto" alt="TypeScript"/>
          <p>TypeScript</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" class="h-12 mx-auto" alt="HTML"/>
          <p>HTML</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" class="h-12 mx-auto" alt="CSS"/>
          <p>CSS</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" class="h-12 mx-auto" alt="PHP"/>
          <p>PHP</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" class="h-12 mx-auto" alt="C"/>
          <p>C</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/csharp/csharp-original.svg" class="h-12 mx-auto" alt="C#"/>
          <p>C#</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" class="h-12 mx-auto" alt="C++"/>
          <p>C++</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/godot/godot-original.svg" class="h-12 mx-auto" alt="Godot"/>
          <p>Godot</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" class="h-12 mx-auto" alt="Docker"/>
          <p>Docker</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" class="h-12 mx-auto" alt="Git"/>
          <p>Git</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" class="h-12 mx-auto" alt="Linux"/>
          <p>Linux</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/unity/unity-original.svg" class="h-12 mx-auto" alt="Unity"/>
          <p>Unity</p>
        </div>
        <div>
          <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/dot-net/dot-net-original.svg" class="h-12 mx-auto" alt=".NET"/>
          <p>.NET</p>
        </div>
      </div>
      