<script lang="ts">
    import HdrCas9 from "./HDR_Cas9.svelte";
    import HdrDiagramContainer from "./HDR_DiagramContainer.svelte";
    import HdrDiagramPositioned from "./HDR_DiagramPositioned.svelte";
    import HdrDiagramStep from "./HDR_DiagramStep.svelte";
    import HdrDnaStrand from "./HDR_DNAStrand.svelte";
    import HdrLabeled from "./HDR_Labeled.svelte";
    import HdrSgRna from "./HDR_sgRNA.svelte";

    let exampleDNAStrand = "";

    function randItem<T>(items: T[]) {
        return items[Math.floor(Math.random() * items.length)];
    }

    function randDNALetter() {
        return randItem(["A", "G", "C", "T"]);
    }

    function complementaryRNABase(base: string) {
        return (
            {
                A: "U",
                G: "C",
                T: "A",
                C: "G",
            }[base] || " "
        );
    }

    for (let i = 0; i < 400; i++) {
        exampleDNAStrand += randDNALetter();
    }

    let casOffsetPos = 4;
    let guiding = Array.from(exampleDNAStrand.substr(casOffsetPos, 10))
        .map((c) => complementaryRNABase(c))
        .join("");
    console.log(exampleDNAStrand);
</script>

<h3>HDR: Step 1</h3>
<p>Cas9, with the aid of its guiding RNA strand, cuts the DNA at a designated spot.</p>
<HdrDiagramStep url="resources/step1.png" />
<h3>HDR: Step 2</h3>
<p>The DNA strand, now split, now needs to be repaired.</p>
<HdrDiagramStep url="resources/step2.png" />
<h3>HDR: Step 3</h3>
<p>A matching DNA strand is identified and aligned with the broken DNA strands.</p>
<HdrDiagramStep url="resources/step3.png" />
<h3>HDR: Step 4</h3>
<p>The donor DNA is patched into the broken DNA strand, adding custom bases where the cut occurred.</p>
<HdrDiagramStep url="resources/step4.png" />
