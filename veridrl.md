---
layout: default
title: VeriDRL - Verification of Deep Reinforcement Learning Applications
---

<div class="post">
     <h2> {{page.title}} </h2>
     <p> Machine learning (ML) solutions are being massively adopted
     in all sorts of applications. This project particularly targets
     Deep Reinforcement Learning (DRL) for control
     applications. Despite its performance, DRL suffers, like other ML
     approaches, from adversarial inputs [11, 8]. The idea of using
     reinforcement learning for control applications is not new [3]
     and several works stress the importance of formally ensuring the
     safety if the resulting applications [7, 13].</p>

     <p> In control application of reinforcement learning, an agent
     interacts with an environment and tries to maximize a reward
     function. For this, The behavior of the environment might be
     known a priori (and the focus will be on optimizing the reward)
     or might need to be explored (and the focus will be on
     discovering new behaviors that will hopefully result in better
     rewards). Practically, a reinforcement learning solution will
     read the state of the system it aims to control, perform an
     action according to the identified policy, and obtain as a result
     a new state of the environment and a new reward. This set-up
     particularly suits ML solutions for synthesizing optimal
     policies, whether the environment behavior is known or
     approximated with samples. However, given the central role of
     such policies and their direct impact on safety-critical systems
     (e.g., autonomous drones or insulin pumps), the verification
     problem of the resulting systems is particularly relevant [7,
     13]. </p>

     <p>Recent development in ML verification [1, 9, 15, 14, 5] mainly
     focus on simple properties such as local robustness of
     classification for single inputs. In fact, very recent works do
     target verification of DRL systems [2, 6, 10, 4]. This however
     comes with many challenges [16, 13, 12] and opportunities for
     research:
     <ul>
        <li>
	Scalability: current ML verification techniques strike
        different trade-offs between scalable but incomplete solutions
        [15, 5] and precise but less scalable ones [9]. Verification
        of DRL policies requires orders of magnitude more scalable
        verification approaches as they will target sequences of
        actions, not just the output to a single input.
	</li>
	<li>
	Stochastic behavior: the controlled systems are typically
	assumed to hold a stochastic behavior as capturing all details
	of their behavior is out-of-reach.
	</li>
	<li>
	Exploration: in fact a model for the controlled system
	might not even be available and one is left with sample of
	possible interactions. A question is then what guarantees can
	one enforce during exploration?
	</li>
	<li>
	The definition of what is to be verified is
	domain dependent and can be complex: from plain safety (no bad
	state should occur more than a given number of times) or
	liveness properties (a good state should eventually occur) to
	probabilistic guarantees based on assumptions on the
	environment
	</li>
     </ul>
     </p>

     <h3>Expected results</h3>
     
     <p>We build on our expertise with extending automatic verification
     techniques to identify DRL problems for which to formulate
     relevant verification problems that will require new verification
     approaches and techniques. Expected results of the project will
     include:
     <ul>
     <li> New ML verification techniques that can scale to realistic DRL
     systems of moderate sizes. </li>
     <li> Verification of (probabilistic) safety and liveness properties
     resulting from learned policies up to bounds to be defined.</li>
     <li>Investigate possibilities to synthesize correct-by-design
     policies.</li>
     </ul>
     </p>

     <h3>Research methodology</h3>

     <p> We build on insights gained in our ongoing WASP project "SafeML"
     with Lund University. The project aims to extend the possibility
     to bring formal correctness guarantees to ML based applications
     targeting safety-critical system. This involves both deriving
     new verification methods for (convolutional) DNNs, investigating
     friendliness of DNNs architectures to verification, and 
     investigating relations of safety (as in robustness) and other behaviors
     of the DNNs. </p>

     <p> We will also build on existing approaches for verifying
     “traditional soft- ware” (from abstract interpretation and
     (bounded) model-checking to rely-guarantee and axiomatic
     reasoning).
     <ul>
     <li> The idea is then to first target DRLs for which an
     environment model is available and to explore the scalability of
     the existing verification techniques and how this can be
     extended. </li>
     <li> Then we will investigate how to reason about the
     inherent stochastic behavior of the models and how to combine
     this with probabilistic model checking [?, 4]. </li>
     <li> Finally, we
     will investigate how to formulate relevant properties and how to
     use and extend these techniques during when synthesizing
     exploratory policies in unknown environments. </li>
     </ul>
     </p>

     <h3>References</h3>
     <ul>
     <li>[1] Aws Albarghouthi et al. Introduction to neural network verification. Foundations and Trends in Programming Languages, 7(1–2):1–157, 2021. </li>
     <li>[2] Guy Amir, Michael Schapira, and Guy Katz. Towards scalable verification of deep reinforcement learning. In 2021 formal methods in computer aided design (FMCAD), pages 193–203. IEEE,
2021.</li>
     <li>[3] Kai Arulkumaran, Marc Peter Deisenroth, Miles Brundage, and Anil Anthony Bharath. Deep reinforcement learning: A brief survey. IEEE Signal Processing Magazine, 34(6):26–38, 2017.</li>
     <li>[4] Edoardo Bacci and David Parker. Verified probabilistic policies for deep reinforcement learning. In NASA Formal Methods Symposium, pages 193–212. Springer, 2022.</li>     
     <li>[5] Anahita Baninajjar, Kamran Hosseini, Ahmed Rezine, and Amir Aminifar. Safedeep: A scalable robustness verification framework for deep neural networks. In ICASSP 2023-2023 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), pages 1–5. IEEE,
2023.</li>
     <li>[6] Davide Corsi, Raz Yerushalmi, Guy Amir, Alessandro Farinelli, David Harel, and Guy Katz. Constrained reinforcement learning for robotics via scenario-based programming. arXiv preprint arXiv:2206.09603, 2022.</li>
     <li>[7] Javier Garcıa and Fernando Fern ́andez. A comprehensive survey on safe reinforcement learning. Journal of Machine Learning Research, 16(1):1437–1480, 2015.</li>
     <li>[8] Sandy Huang, Nicolas Papernot, Ian Goodfellow, Yan Duan, and Pieter Abbeel. Adversarial attacks on neural network policies. arXiv preprint arXiv:1702.02284, 2017.</li>
     <li>[9] Guy Katz, Derek A Huang, Duligur Ibeling, Kyle Julian, Christopher Lazarus, Rachel Lim, Parth Shah, Shantanu Thakoor, Haoze Wu, Aleksandar Zelji ́c, et al. The marabou framework for verification and analysis of deep neural networks. In Computer Aided Verification: 31st International Conference, CAV 2019, New York City, NY, USA, July 15-18, 2019, Proceedings, Part I 31, pages 443–452. Springer, 2019.</li>
     <li>[10]  Yafim Kazak, Clark Barrett, Guy Katz, and Michael Schapira. Verifying deep-rl-driven systems. In Proceedings of the 2019 workshop on network meets AI & ML, pages 83–89, 2019.</li>
     <li>[11] Jernej Kos and Dawn Song. Delving into adversarial attacks on deep policies. arXiv preprint arXiv:1705.06452, 2017.</li>
     <li>[12] Matthew Landers and Afsaneh Doryab. Deep reinforcement learning verification: A survey. ACM Computing Surveys, 2023.</li>
     <li>[13] Erik Nikko, Zoran Sjanic, and Fredrik Heintz. Towards verification and validation of reinforcement learning in safety-critical systems: A position paper from the aerospace industry. In IJCAI 2021 Workshop, August 19, 2021, 2021.</li>
     <li>[14] Matan Ostrovsky, Clark Barrett, and Guy Katz. An abstraction-refinement approach to verifying convolutional neural networks. In International Symposium on Automated Technology for Verification and Analysis, pages 391–396. Springer, 2022.</li>
     <li>[15] Gagandeep Singh, Timon Gehr, Markus P ̈uschel, and Martin Vechev. An abstract domain for certifying neural networks. Proceedings of the ACM on Programming Languages, 3(POPL):1–30, 2019.</li>
     <li>[16] Perry Van Wesel and Alwyn E Goodloe. Challenges in the verification of reinforcement learning algorithms. Technical report, 2017.</li>
     </ul>
</div>
