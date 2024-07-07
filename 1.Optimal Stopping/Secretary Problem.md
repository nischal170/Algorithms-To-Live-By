The basic form of the problem is the following: imagine an administrator who wants to hire the best secretary out of 𝑛![{\displaystyle n}](https://wikimedia.org/api/rest_v1/media/math/render/svg/a601995d55609f2d9f5e233e36fbe9ea26011b3b) rankable applicants for a position. The applicants are interviewed one by one in random order. A decision about each particular applicant is to be made immediately after the interview. Once rejected, an applicant cannot be recalled. During the interview, the administrator gains information sufficient to rank the applicant among all applicants interviewed so far, but is unaware of the quality of yet unseen applicants. The question is about the optimal strategy ([stopping rule](https://en.wikipedia.org/wiki/Stopping_rule "Stopping rule")) to maximize the probability of selecting the best applicant. If the decision can be deferred to the end, this can be solved by the simple maximum [selection algorithm](https://en.wikipedia.org/wiki/Selection_algorithm "Selection algorithm") of tracking the running maximum (and who achieved it), and selecting the overall maximum at the end. The difficulty is that the decision must be made immediately.

The 37% rule, also known as the Secretary Problem or the Optimal Stopping Theory, is a mathematical strategy used to determine the optimal point at which to stop searching and make a decision to maximize the chances of selecting the best option. This rule is particularly applicable to scenarios where you need to choose the best option (like hiring a secretary or selecting a partner) from a sequentially presented series of candidates, without being able to return to previously rejected options.

### The Problem Setup

1. **Candidates:** There are \( n \) candidates or options to choose from, presented sequentially in random order.
2. **Evaluation:** You can evaluate each candidate but must decide immediately whether to accept or reject them before moving on to the next.
3. **Goal:** Maximize the probability of selecting the best candidate.

### The 37% Rule

The optimal strategy to maximize the probability of choosing the best candidate involves the following steps:

1. **Rejection Phase:** Reject the first \( 37\% \) (approximately \( n/e \)) of the candidates outright. Here, \( e \) is the base of the natural logarithm, approximately equal to 2.718.
2. **Selection Phase:** After the rejection phase, select the next candidate who is better than all the candidates you have seen so far.

### Detailed Explanation

1. **Determine the Rejection Threshold:** Calculate $( r = \left\lfloor \frac{n}{e} \right\rfloor$). For a large \( n \), this is about 37% of the total number of candidates. If \( n = 100 \), then \( r = 37 \).
2. **Reject Initial Candidates:** Evaluate and reject the first \( r \) candidates. During this phase, keep track of the best candidate among the rejected ones.
3. **Select the Best Candidate:** Starting from the $$ (r+1) $$th candidate, select the first candidate who is better than the best candidate from the rejection phase. If no candidate is better than the best from the rejection phase, select the last candidate.

### Why 37%?

The number 37% comes from the mathematical analysis of the problem, which shows that this is the point where the probability of selecting the best candidate is maximized. Here's a brief overview of the mathematical reasoning:

- The probability \( P \) of selecting the best candidate after rejecting \( r \) candidates is given by:
  $$
  P(r) = \frac{r}{n} \sum_{k=r+1}^{n} \frac{1}{k-1}
  $$
- Maximizing this probability involves taking the derivative and solving for $( r$ \), leading to \( r \approx $\frac{n}{e}$).

### Example

Suppose you are interviewing 10 candidates for a job:

1. **Rejection Phase:** Reject the first 4 candidates (since \( $\frac{10}{e}$ \approx 3.7 \)).
2. **Selection Phase:** Out of the remaining 6 candidates, choose the first candidate who is better than any of the first 4 candidates.

### Applications

- **Hiring:** Selecting the best job candidate from a pool of applicants.
- **Dating:** Choosing a long-term partner from a sequence of potential partners.
- **Real Estate:** Deciding on the best house to buy when visiting several properties sequentially.

The 37% rule provides a practical and mathematically grounded approach to making optimal decisions in these and similar scenarios.
