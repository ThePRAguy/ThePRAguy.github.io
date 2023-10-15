### Multi-Unit CCF Impacts
B writes:
_"Hypothetically, if one had a two-unit NPP, each with two Emergency Diesel Generators (EDGs), and one experienced a failure,
in analyzing the events from a significance determination process (SDP) perspective, one might be expected to consider the potential for
higher common cause failure likelihood for the other unit's EDGs, right? How is one supposed to change the CCF values of the remaining EDGs,
given that the first failure has already occurred?"_

Great question, however, this question essentially encompasses two areas: (1) modifying CCF probabilities given a failure of a component in that CCF group,
and (2), multi-unit common cause failures. I'll try to provide my perspective on both.

Modifying CCF Probabilities for Failures - My go-to guidance here is Appendix E of [NUREG/CR-5485](https://nrcoe.inl.gov/publicdocs/CCF/NUREGCR-5485_Guidelines%20on%20Modeling%20Common-Cause%20Failures%20in%20PRA.pdf). Specifically, Section E.3.1 discusses how to modify CCF probabilities when a component in the CCF group is failed.
The only limiting piece of this discussion is that it really only focuses on a group of 3, which can leave something to be desired in the real world. In short though, the process discusses calculating conditional probabilities.
When using the alpha factor model, a very simple estimate of the delta risk would be to update only the CCF probability for the event that represents the failure of all components in the CCF group. For example, if we have a group 
of 3 components, and one of those components failed, we would update the probability of the CCF representing the failure of all three components to the value of $\alpha_{3}$. Technically speaking, you should also modify the CCF probabilities for
groups that represent smaller subsets of components (i.e., groups of 2 in the group of 3 example). In a future post I may walk through this specific details. 

Multi-Unit CCF - In general, the CCF parameters developed for the U.S. industry are generated using information from single-units. As an example, for a two-unit site that has four EDGs, if there was a failure of 1 component, the event would most likely be classified as a failure of one component
in a group of two components, not 1 failure in a group of four components. This classification has some very specific implications on how the alpha factors are derived, and generally speaking, classifying events as occurring from smaller group sizes will result in larger alpha factors. A lot of this discussion 
depends on how the CCF group was defined in the plant-specific PRA. If you are in development of a multi-unit PRA model, you may want to ensure that the CCF parameters you are using better reflect multi-unit experience. I will shamelessly plug a recent [paper](https://www.ans.org/meetings/npic13psa2023/session/view-1957/#paper_5879) I did for PSA 2023
which details the different considerations for multi-unit CCF alpha factors, in case you are interested. All that being said, if you really do have a multi-unit PRA model, the way you would modify CCF probabilities is unchanged.

-Matt

