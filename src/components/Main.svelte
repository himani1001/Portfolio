<script>
    import Step from "./Step.svelte";

    let steps = [
        { name: "My Book Store", icon: "fa-solid fa-book-open-reader" },
        {
            name: "Multiple Feature Integration Website",
            icon: "fa-solid fa-globe",
        },
        { name: "Breast Cancer Prediction", icon: "fa-solid fa-ribbon" },
    ];

    let benefits = [
        {
            name: "a self taught developer",
            description:
                "When I was 18, I started reading books and wished I could store them somewhere, not knowing there were websites for that purpose. I promised myself I would create something to solve this problem. Driven by this goal, I taught myself to code using free online resources. I began with JavaScript, HTML, and CSS, and gradually expanded my knowledge to include JavaScript frameworks, backend programming, design, cloud services, and much more.",
        },
        {
            name: "a product design & UX finatic",
            description:
                "Creating exquisite user experiences and experimenting with them let me employ every ounce of creativity I possess. I enjoy taking on new design challenges and giving users incredible web experiences.",
        },
        {
            name: "an excellent communicator",
            description:
                "Effective communication is fundamental to my approach, emphasizing transparency and constructive dialogue. I prioritize these values as they foster deep connections and enhance my productivity and effectiveness within any team and workspace.",
        },
    ];
</script>

<main class="flex flex-col flex-1 p-4">
    <section
        id="introPage"
        class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
    >
        <div
            class="flex flex-col lg: justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
        >
            <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                Hi! I'm <span class="poppins text-violet-400">Himani</span>
                Sharma<br /> Full Stack
                <span class="poppins text-violet-400">Developer</span>
            </h2>
            <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400">favorite tech</span> includes includes
                React.js + Express.js + MongoDB + Node.js, Javascript, CSS & HTML
            </p>
            <a
                href="https://github.com/himani1001"
                target="_blank"
                class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
            >
                <div
                    class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
                />
                <h4 class="relative z-9">Get in touch <i class="fa-brands fa-github"></i> &rarr;</h4>
            </a>
        </div>
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={"images/file.png"}
                alt="Profile image"
                class="object-cover z-[2] max-h-[70vh]"
            />
        </div>
    </section>

    <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-lg sm:text-xl md:text-2xl">
                A Few of my projects...
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Want to <span class="poppins text-violet-400">see </span>my
                work?
            </h3>
        </div>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    I stored all the books that I want to read in further using
                    <strong class="text-violet-400">MERN</strong> stack
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    Website similar to ChatGPT created with <strong
                        class="text-violet-400">OpenAI API + React</strong
                    >
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Predicts the chances of one having breast cancer using
                    database with <strong class="text-violet-400">Python</strong
                    >
                </p>
            </Step>
        </div>
    </section>
    <section
        id="about"
        class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
    >
        <div
            class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
        >
            <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                A bit <span class="poppins text-violet-400">about</span> me.
            </h3>
        </div>
        <p class="mx-auto poppins text-center font-semibold text-lg sm:text-xl md:text-2xl">
            I am currently in the fourth year of my Computer Science B.E. program, specializing in the development of web applications using the <strong class="text-violet-400">MERN</strong> stack.
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}
                <div class="flex gap-6 sm:gap-8">
                    <p
                        class="poppins text-4xl sm:text-5xl md: text-6xl text-slate-500 font-semibold"
                    >
                        0{index + 1}
                    </p>
                    <div class="flex flex-col gap-6 sm:gap-8">
                        <h3 class="text-2xl sm:text-3xl md:text-5xl">
                            {benefit.name}
                        </h3>
                        <p>{benefit.description}</p>
                    </div>
                </div>
            {/each}
        </div>
        <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
            The <span class="text-violet-400 poppins">Complete</span> Package
        </h5>
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
            <!-- Frontend Development -->
            <div class="border-2 border-white rounded-lg p-6">
                <h3 class="text-violet-400 text-center font-semibold text-2xl mb-4">
                    Frontend Development
                </h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div class="flex items-center gap-4">
                        <i class="fa-solid fa-square-check"></i>
                        <div>
                            <h3 class="text-xl font-semibold">HTML</h3>
                            <p>Experienced</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <i class="fa-solid fa-square-check"></i>
                        <div>
                            <h3 class="text-xl font-semibold">CSS</h3>
                            <p>Experienced</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <i class="fa-solid fa-square-check"></i>
                        <div>
                            <h3 class="text-xl font-semibold">JavaScript</h3>
                            <p>Intermediate</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <i class="fa-solid fa-square-check"></i>
                        <div>
                            <h3 class="text-xl font-semibold">React JS</h3>
                            <p>Intermediate</p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Backend Development -->
            <div class="border-2 border-white rounded-lg p-6">
                <h3 class="text-violet-400 text-center font-semibold text-2xl mb-4">
                    Backend Development
                </h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                    <div class="flex items-center gap-4">
                        <i class="fa-solid fa-square-check"></i>
                        <div>
                            <h3 class="text-xl font-semibold">MongoDB</h3>
                            <p>Intermediate</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <i class="fa-solid fa-square-check"></i>
                        <div>
                            <h3 class="text-xl font-semibold">Node JS</h3>
                            <p>Intermediate</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <i class="fa-solid fa-square-check"></i>
                        <div>
                            <h3 class="text-xl font-semibold">Express JS</h3>
                            <p>Intermediate</p>
                        </div>
                    </div>
                    <div class="flex items-center gap-4">
                        <i class="fa-solid fa-square-check"></i>
                        <div>
                            <h3 class="text-xl font-semibold">Git</h3>
                            <p>Intermediate</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <p class="mx-auto">So why not invest?</p>
    </section>
</main>
