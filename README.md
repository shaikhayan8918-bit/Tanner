# Tanner
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pain Psychotherapy Canada</title>
    <style>
        /* CSS Reset/Normalization */
        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html, body {
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        /* Base Styles */
        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #fdfdfd;
        }

        .container {
            width: 100%;
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Typography & Spacing */
        h1, h2, h3 {
            line-height: 1.2;
            margin-bottom: 20px;
            font-weight: 700;
            color: #1a1a1a;
        }

        h1 {
            font-size: 2.5rem;
        }

        h2 {
            font-size: 2rem;
            text-align: center;
            margin-top: 40px;
            margin-bottom: 30px;
        }

        h3 {
            font-size: 1.5rem;
        }

        p {
            margin-bottom: 1.2em;
            font-size: 1.1rem;
            max-width: 720px;
            margin-left: auto;
            margin-right: auto;
        }

        .preheader {
            text-align: center;
            font-size: 0.9rem;
            font-weight: 600;
            color: #666;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 15px;
        }

        .subheader {
            font-size: 1.25rem;
            color: #444;
            max-width: 650px;
            margin: 20px auto 30px;
            text-align: center;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 60px 20px;
            background-color: #f4f7f6;
        }

        /* VSL Section */
        .vsl-container {
            display: inline-block;
            text-decoration: none;
            color: inherit;
            margin-bottom: 30px;
        }

        .vsl-icon {
            position: relative;
            width: 100%;
            max-width: 500px;
            aspect-ratio: 16 / 9;
            background-color: #000;
            background-image: url('https://i.imgur.com/G4hXqf7.jpg'); /* Placeholder image representing pain/therapy */
            background-size: cover;
            background-position: center;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.2s ease-in-out;
        }
        .vsl-icon:hover {
            transform: scale(1.03);
        }

        .play-button {
            width: 80px;
            height: 80px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 0 20px rgba(0,0,0,0.2);
        }

        .play-triangle {
            width: 0;
            height: 0;
            border-left: 24px solid #c0392b;
            border-top: 14px solid transparent;
            border-bottom: 14px solid transparent;
            margin-left: 5px;
        }

        .vsl-text {
            margin-top: 15px;
            font-weight: 600;
            color: #2c3e50;
            font-size: 1rem;
        }

        /* Buttons */
        .cta-button {
            display: inline-block;
            background-color: #27ae60;
            color: #fff;
            padding: 15px 35px;
            font-size: 1.2rem;
            font-weight: 700;
            text-decoration: none;
            border-radius: 8px;
            box-shadow: 0 4px 10px rgba(39, 174, 96, 0.4);
            transition: all 0.3s ease;
        }

        .cta-button:hover {
            background-color: #2ecc71;
            transform: translateY(-2px);
            box-shadow: 0 6px 15px rgba(39, 174, 96, 0.5);
        }

        /* Section Styling */
        section {
            padding: 50px 0;
        }
        
        .section-problem {
            background-color: #fff;
        }

        .section-origin {
            background-color: #ecf0f1;
        }
        
        .section-solution, .section-product, .section-faq {
            background-color: #fff;
        }

        .section-offer {
            background-color: #f4f7f6;
            text-align: center;
        }

        /* Bullets */
        ul.benefits-list {
            list-style: none;
            margin: 30px auto;
            max-width: 680px;
        }

        ul.benefits-list li {
            font-size: 1.1rem;
            padding: 15px 15px 15px 50px;
            position: relative;
            background-color: #f9f9f9;
            border-radius: 5px;
            margin-bottom: 12px;
            border-left: 4px solid #27ae60;
        }

        ul.benefits-list li::before {
            content: '✓';
            position: absolute;
            left: 15px;
            top: 50%;
            transform: translateY(-50%);
            color: #27ae60;
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        /* Offer Section */
        .offer-box {
            background: #fff;
            border: 1px solid #ddd;
            padding: 30px;
            border-radius: 10px;
            max-width: 650px;
            margin: 20px auto 40px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }

        .offer-box .price {
            font-size: 1.1rem;
            margin-bottom: 10px;
            color: #34495e;
        }

        /* FAQ Section */
        .faq-item {
            margin-bottom: 25px;
        }
        .faq-item h3 {
            font-size: 1.2rem;
            color: #2c3e50;
        }

        /* Utilities */
        .text-center {
            text-align: center;
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            h2 {
                font-size: 1.75rem;
            }
            .container {
                padding: 15px;
            }
            p, .subheader {
                font-size: 1rem;
            }
            .cta-button {
                width: 100%;
                padding: 18px;
            }
            .hero {
                padding: 40px 15px;
            }
        }
    </style>
</head>
<body>

    <header class="hero">
        <div class="container">
            <p class="preheader">FOR CANADIANS AGED 30–65 LIVING WITH CHRONIC PAIN</p>
            <h1>New Study Shows 66% of Sufferers Were Pain-Free By Retraining Their Brain—Not Treating Their Body</h1>
            <p class="subheader">And it works without endless specialist appointments, addictive medications, or being told “the tests are normal” while you’re still in agony.</p>
            
            <a href="https://docs.google.com/document/d/1NOzjBT4rITD_NPbnFCEVv9Zmp9HlBzRRAA3ScsSs3AA/edit?usp=sharing" target="_blank" class="vsl-container">
                <div class="vsl-icon">
                    <div class="play-button">
                        <div class="play-triangle"></div>
                    </div>
                </div>
                <p class="vsl-text">Click Here To See The: VSL I WROTE FOR YOU</p>
            </a>
            
            <a href="#offer" class="cta-button">Book My Free 20-Minute Consultation</a>
        </div>
    </header>

    <main>
        <section class="section-problem">
            <div class="container">
                <h2>The ‘Try-And-Fail’ Medical Merry-Go-Round That Keeps You Trapped</h2>
                <p>Does this sound familiar?</p>
                <p>It starts with a twinge. A deep ache. A burning sensation that just… won’t… quit.</p>
                <p>So you do the responsible thing. You see your doctor. Then a specialist. Maybe a physiotherapist or a chiropractor.</p>
                <p>You get X-rays. An MRI. Blood tests. They all come back “inconclusive.”</p>
                <p>You’re given prescriptions that barely touch the sides, or come with side effects that are almost as bad as the pain itself.</p>
                <p>You try injections. You rest. You push through it. You spend hundreds, maybe thousands, on treatments that promise relief but deliver nothing lasting.</p>
                <p>And with every failed attempt, a little part of you starts to panic.</p>
                <p>The fear creeps in at 3 AM. <em>What if this is permanent? What if it gets worse? Will I lose my ability to work, to play with my kids, to simply enjoy a walk?</em></p>
                <p>You feel invalidated. Ignored. Like your own body has betrayed you, and the system meant to help has left you behind.</p>
                <p>The real cost isn’t just the money spent. It’s the life you’re missing out on. The constant drain on your energy and your mood. The feeling of being a prisoner in your own body.</p>
                <p>But what if the reason nothing has worked… is because everyone has been looking in the wrong place?</p>
            </div>
        </section>

        <section class="section-origin">
            <div class="container">
                <h2>Why The Medical System Fails So Many (And It’s Not Your Fault)</h2>
                <p>For decades, medicine has treated chronic pain as a purely structural problem.</p>
                <p>A "bad back" must mean a slipped disc. Fibromyalgia must mean something is wrong with the muscles. Migraines… well, they’re still mostly a mystery to many doctors.</p>
                <p>This approach assumes your body is like a car. If something hurts, a part must be broken. Fix the part, and the pain goes away.</p>
                <p>But a wave of new scientific evidence has revealed a completely different story.</p>
                <p>Researchers at top institutions discovered that for many chronic conditions—like back pain, fibromyalgia, IBS, and migraines—the problem often isn’t in the body part that hurts.</p>
                <p>The problem is in the brain.</p>
                <p>It’s called <strong>neuroplastic pain</strong>. The brain essentially learns pain. After an injury or a period of intense stress, the brain can get stuck in a "danger" loop, creating real, physical pain signals even after the original physical issue has healed.</p>
                <p>Your pain is 100% real. But its source is a misfiring prediction from the brain.</p>
                <p>This is why treatments focused only on the body—like surgery, injections, and manual therapies—so often fail for chronic pain. They’re fixing the wrong thing.</p>
                <p>It’s like trying to fix a software bug by polishing the computer screen.</p>
                <p>This is where the real path to relief begins. Not by focusing on the body part that hurts, but by retraining the brain that creates the pain.</p>
            </div>
        </section>

        <section class="section-solution">
            <div class="container">
                <h2>Retraining Your Brain To Erase Pain Signals</h2>
                <p>Imagine your brain is a highly advanced, but overly protective, alarm system.</p>
                <p>With neuroplastic pain, that alarm is stuck ON. It's screaming "DANGER!" at normal sensations like bending over, sitting for too long, or even just feeling stressed.</p>
                <p>Our method, grounded in approaches like Pain Reprocessing Therapy (PRT), gives you the tools to calmly walk over to that alarm panel and turn it off.</p>
                <p>It’s a guided process of teaching your brain that you are, in fact, safe. It involves:</p>
                <p><strong>1. Understanding the True Source:</strong> We help you see the conclusive evidence that your pain is due to these faulty brain signals, not a broken body. This insight alone can begin to lower the fear and the pain.</p>
                <p><strong>2. Somatic Tracking:</strong> You learn to pay attention to your sensations with curiosity instead of fear. This simple shift in awareness teaches the brain that these sensations are not dangerous, dialing down the alarm.</p>
                <p><strong>3. Addressing Emotional Drivers:</strong> We help you process underlying stress and emotions that keep your nervous system on high alert, fueling the pain cycle.</p>
                <p>This isn’t just a theory. It’s a proven, evidence-based method.</p>
                <p>A randomized controlled trial on Pain Reprocessing Therapy found that <strong>66% of participants with chronic back pain were pain-free or nearly pain-free</strong> after nine sessions.</p>
                <p>Even more astounding? <strong>98% had at least some reduction in their pain.</strong></p>
                <p>Think about that. After years of suffering, two-thirds of people were virtually free from pain. By learning to retrain their brain.</p>
                <ul class="benefits-list">
                    <li><strong>One-on-One Virtual Therapy Sessions</strong> &rarr; Receive expert guidance from a therapist trained in the science of neuroplastic pain &rarr; You become someone who finally has a clear, proven map out of pain.</li>
                    <li><strong>Access to 30+ Guided Worksheets</strong> &rarr; To help you rewire old beliefs and reinforce new messages of safety for your brain &rarr; You build an unshakable confidence in your body’s strength.</li>
                    <li><strong>A Library of 60+ Somatic Practices</strong> &rarr; Giving you on-demand tools to calm your nervous system anytime, anywhere &rarr; You feel in control, knowing you can handle any sensation your body produces.</li>
                </ul>
            </div>
        </section>

        <section class="section-product">
            <div class="container">
                <h2>Introducing: Pain Psychotherapy Canada — A Guided Path To A Life Without Pain</h2>
                <p>This isn't just another "coping mechanism." And it's not traditional talk therapy where you just discuss your feelings about the pain.</p>
                <p>This is an active, structured, and educational process designed to get you a specific result: a significant reduction or the complete elimination of your chronic symptoms.</p>
                <p>We combine several evidence-based mind-body approaches into a coherent plan tailored to you.</p>
                <p>Unlike physiotherapy, which focuses only on the muscles…</p>
                <p>We work with the brain’s <em>interpretation</em> of the signals coming from those muscles.</p>
                <p>Unlike medication, which just masks the signals…</p>
                <p>We address the root cause, helping your brain stop sending the signals in the first place.</p>
                <p>And unlike the endless cycle of specialist visits that leave you with more questions than answers…</p>
                <p>We provide a clear framework that makes sense of your experience and gives you actionable steps to take back control. This is the missing piece you’ve been searching for.</p>
            </div>
        </section>

        <section class="section-offer" id="offer">
            <div class="container">
                <h2>Your First Step Starts Today</h2>
                <p>You’ve already spent enough time and money on things that didn’t work. You’ve felt the frustration and the hopelessness.</p>
                <p>Now it’s time for a different approach. One based on the latest science of the brain.</p>
                <p>Your journey begins with a free, no-obligation 20-minute virtual consultation with one of our pain therapy specialists.</p>
                <div class="offer-box">
                    <h3>Get Started With A Complimentary Consultation</h3>
                    <p>In this call, we will listen to your story, help you understand if your symptoms are likely neuroplastic, and explain exactly how this process could work for you. There is no pressure to commit.</p>
                    <p>It's simply a chance for you to get clarity and see if this feels right.</p>
                    <p>If you decide to move forward, our session rates are transparent:</p>
                    <ul>
                        <li class="price">Standard 50-minute therapy session: $220 CAD</li>
                        <li class="price">90-minute EMDR or ART session: $330 CAD</li>
                        <li class="price">Naturopathic sessions: from $175–$250 CAD</li>
                    </ul>
                </div>
                <p>How many more weeks, months, or years are you willing to let pain dictate your schedule, your mood, and your life?</p>
                <p>The possibility of a life with less—or even zero—pain is real. It starts with a single conversation.</p>
                <a href="#" class="cta-button">Book My Free 20-Minute Consultation Now</a>
            </div>
        </section>

        <section class="section-faq">
            <div class="container">
                <h2>Your Questions, Answered</h2>
                <div class="faq-item">
                    <h3>But my pain feels 100% physical. How can a psychological approach fix a physical problem?</h3>
                    <p>This is the most important question. The pain IS 100% real and physical. We are not saying it's "in your head." What we're saying is that it's *generated* by the brain and nervous system. Think of phantom limb pain—a person with an amputated leg can feel intense pain in a foot that isn’t there. This proves the brain can create very real pain without any input from the body. Our job is to correct the faulty signaling that's causing your very real physical sensations.</p>
                </div>
                <div class="faq-item">
                    <h3>Why is it priced this way? It seems expensive.</h3>
                    <p>Consider the alternative. What is the cost of staying in pain? Think of the accumulated expenses of medications, injections, and therapies that haven't worked. The lost income from days you couldn't work. The immeasurable cost of missing out on life's precious moments. This is an investment in a long-term solution that gives you your life back, potentially saving you tens of thousands of dollars in future ineffective treatments.</p>
                </div>
                <div class="faq-item">
                    <h3>I'm worried that focusing on the pain or my emotions will make it worse.</h3>
                    <p>It’s a common and understandable fear. That’s why our approach is so different. We don’t ask you to "push through" pain. Instead, we guide you through a gentle process called somatic tracking, where you learn to observe sensations from a place of safety and curiosity. This actually calms the nervous system and reduces the fear-pain cycle, rather than making it worse. You are guided every step of the way.</p>
                </div>
                <div class="faq-item">
                    <h3>How long does this take to work? I've been in pain for years.</h3>
                    <p>The time it takes varies, but it's often faster than people think. The landmark study showed significant results after just nine sessions. The goal is not to keep you in therapy forever. It's to equip you with the understanding and the tools to become your own healer. Your years of pain don’t mean years of recovery. Once your brain learns it's safe, change can happen surprisingly fast.</p>
                </div>
                <div class="text-center">
                    <a href="#offer" class="cta-button">I'm Ready To Take The First Step</a>
                </div>
            </div>
        </section>
    </main>

</body>
</html>
