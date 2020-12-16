Flux to List – How to convert Reactor Flux to List/Map

![Flux to List – How to convert Reactor Flux to List/Map](https://loizenai.com/wp-content/uploads/2020/12/Reactor-Flux-to-List.png)

What is a Reactor Flux? A Flux is a Reactive Streams Publisher , augmented with a lot of operators that can be used to generate, transform, orchestrate Flux sequences. It can emit 0 to n elements ( onNext event) then either completes or errors ( onComplete and onError terminal events).
In this tutorial, I introduces ways to convert Reactor Flux into List/Map.

## I. Ways to convert Flux to List, Map
We will use Flux methods such as:
– collectList(): accumulate sequence into a Mono<List>.
-> Collect all elements emitted by this Flux into a List that is emitted by the resulting Mono when this sequence completes.

– collectSortedList(): accumulate sequence and sort into a Mono<List>.
-> Collect all elements emitted by this Flux until this sequence completes, and then sort them in natural order into a List that is emitted by the resulting Mono.

– collectMap(): convert sequence into a Mono<Map>.
-> Collect all elements emitted by this Flux into a hashed Map that is emitted by the resulting Mono when this sequence completes. The key is extracted from each element by applying the keyExtractor Function. In case several elements map to the same key, the associated value will be the most recently emitted element.

– collectMultimap(): convert sequence into a Mono<Map> that each Map’s key can be paired with multi-value (in a Collection).
-> Collect all elements emitted by this Flux into a multimap that is emitted by the resulting Mono when this sequence completes. The key is extracted from each element by applying the keyExtractor Function, and every element mapping to the same key is stored in the List associated to said key.

Then the Mono result above will be converted into a real List, Map using block() method.

## Initialization Reactor Flux

See at: https://loizenai.com/flux-to-list-reactor/
