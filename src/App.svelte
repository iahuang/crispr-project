<script lang="ts">
    import Bibliography from "./components/Bibliography.svelte";
    import HdrDiagram from "./components/hdrepair/HDR_Diagram.svelte";
    import InlineImage from "./components/InlineImage.svelte";
    import SpecialTerm from "./components/SpecialTerm.svelte";
    import TwoColumn from "./components/TwoColumn.svelte";
    import type { MLASource } from "./mla";

    const sources: MLASource[] = [
        {
            author: "Medline Plus",
            organization: "U.S. National Library of Medicine",
            title: "Sickle Cell Disease",
            date: "7 June 2018",
            url: "https://medlineplus.gov/sicklecelldisease.html",
        },
        {
            author: "National Heart, Lung, and Blood Institute",
            organization: "U.S. Department of Health and Human Services",
            title: "Anemia",
            url: "https://www.nhlbi.nih.gov/health-topics/anemia",
        },
        {
            organization: "WebMD",
            title: "Anemia",
            url: "https://www.webmd.com/a-to-z-guides/understanding-anemia-basics",
        },
        {
            organization: "Center for Disease Control and Prevention",
            title: "Complications and Treatments of Sickle Cell Disease",
            url: "https://www.cdc.gov/ncbddd/sicklecell/treatments.html",
        },
        {
            author: "SJCRH Dept. of Hematology",
            organization: "St. Jude Children's Research Hospital",
            title: "Bone Marrow (Stem Cell) Transplant for Sickle Cell Disease",
            url:
                "https://www.stjude.org/content/dam/en_US/shared/www/patient-support/hematology-literature/bone-marrow-stem-cell-transplant-for-sickle-cell-disease.pdf",
        },
        {
            author: "National Heart, Lung, and Blood Institute",
            organization: "U.S. Department of Health and Human Services",
            title: "Sickle Cell Disease",
            url: "https://www.nhlbi.nih.gov/health-topics/sickle-cell-disease",
            date: "1 September 2020",
        },
        {
            organization: "Mayo Clinic",
            title: "Hemoglobin Test",
            url: "https://www.mayoclinic.org/tests-procedures/hemoglobin-test/about/pac-20385075",
            date: "9 October 2019",
        },
        {
            title: "What are genome editing and CRISPR-Cas9?",
            organization: "Medline Plus",
            date: "18 September 2020",
            url: "https://medlineplus.gov/genetics/understanding/genomicresearch/genomeediting/",
        },
        {
            title: "CRISPR/Cas9",
            organization: "Tufts University",
            author: "Peter Cananagh, Anthony Garrity",
            url: "https://sites.tufts.edu/crispr/",
        },
        {
            title: "Gene Editing Mechanism of CRISPR-Cas9",
            author: "Wyss Institute",
            organization: "Harvard University",
            url: "https://wyss.harvard.edu/media-post/gene-editing-mechanism-of-crispr-cas9/",
        },
        {
            title: "Gene Therapy in a Patient with Sickle Cell Disease",
            author:
                "Jean-Antoine Ribeil, M.D., Ph.D., Salima Hacein-Bey-Abina, Pharm.D., Ph.D., Emmanuel Payen, Ph.D., et. al.",
            date: "2 March 2017",
            url: "https://www.nejm.org/doi/full/10.1056/NEJMoa1609677",
        },
        {
            title: "Genetic Mutation",
            author: "Suzanne Clancy, Ph.D.",
            organization: "Nature Education",
            url: "https://www.nature.com/scitable/topicpage/genetic-mutation-441/",
        },
    ];
</script>

<main>
    <div class="header">
        <h1>Sickle Cell Anemia and CRISPR</h1>
        <span>By Ian Huang</span>
    </div>
    <div class="main">
        <h1>What is Sickle Cell Anemia?</h1>
        <TwoColumn split={70}>
            <div slot="first">
                <p>
                    Sickle cell anemia is a form of <SpecialTerm
                        definition="A condition defined by a low count of blood cells, characterized by a lack of oxygen in the blood."
                        >anemia</SpecialTerm
                    >, a blood condition that causes dizziness, irregular heartbeat, joint pain, fatigue, and
                    developmental problems for children. At its core, sickle cell anemia is caused by a <SpecialTerm
                        definition="A health problem caused by issues in one's genes">genetic disorder</SpecialTerm
                    >
                    called <i>sickle cell disease</i> (SCD). A defective gene causes red blood cells to become
                    <i>sickle-shaped</i>, as shown in the image to the right.
                </p>
                <p>
                    These irregularly-shaped red blood cells are fragile, breaking easily, and making it difficult for
                    the body to replenish them in sufficient amounts. Additionally, the sickle cells can stick to the
                    walls of blood vessels, causing blockages and starving tissues of oxygen.
                </p>
                <h3>Common Health Problems Resulting from Sickle Cell Disease</h3>

                <ul>
                    <li>Fatigue related to anemia</li>
                    <li>Swelling of hands and feet</li>
                    <li>
                        Damage to the <SpecialTerm
                            definition="An organ that filters the blood, stores red and white blood cells, and recycles old red blood cells."
                            >spleen</SpecialTerm
                        >
                    </li>
                    <li>Increased risk of infection</li>
                    <li>Episodes of sudden pain, ranging in severity</li>
                </ul>
            </div>
            <div slot="second">
                <InlineImage
                    url="https://www.genome.gov/sites/default/files/tg/en/illustration/sickle_cell_disease.jpg"
                />
            </div>
        </TwoColumn>
        <TwoColumn split={70}>
            <div slot="first">
                <h3>Traditional Treatments for Sickle Cell Disease</h3>
                <p>
                    The most common form of treatment for sickle cell anemia patients involves bone marrow transplant.
                    Bone marrow is responsible for producing the red blood cells in your body, and in patients with SCD,
                    the bone marrow tissue contains the faulty genetics responsible for producing malformed red blood
                    cells. In a bone marrow transplant, healthy bone marrow tissue is taken from a donor and inserted
                    into the patient's bone marrow.
                </p>
                <p>
                    Unfortunately, this treatment is prone to issues such as the body <SpecialTerm
                        definition="When foreign tissue is inserted into your body, such as in the case of a bone marrow transplant, your body may reject it, meaning that your immune system recognizes it as foreign and tries to destroy it."
                        >rejecting</SpecialTerm
                    > the new bone tissue; finding donors with a compatible <SpecialTerm
                        definition="A person's blood type is determined by the presence of immune proteins in their blood. Incompatible blood types can lead to complications."
                        >blood type</SpecialTerm
                    > can be difficult. Additionally, the procedure may cause other unintended side effects such as infection,
                    or damage to nearby blood vessels.
                </p>
            </div>
            <div slot="second">
                <InlineImage
                    url="https://www.ohsu.edu/sites/default/files/2019-03/stem-cell-transplant-w-captions-fullsize.jpg"
                />
            </div>
        </TwoColumn>
        <h1>What Causes Sickle Cell Disease?</h1>
        <TwoColumn split={20}>
            <div slot="first">
                <InlineImage url="https://medlineplus.gov/images/PX000154_PRESENTATION.jpeg" />
            </div>
            <div slot="second">
                <TwoColumn split={80}>
                    <div slot="first">
                        <h3>What is Hemoglobin?</h3>
                        Hemoglobin (also spelled&nbsp<i>haemoglobin</i>) is a <SpecialTerm
                            definition="A very large organic molecule that serves a variety of purposes in the body"
                            >protein</SpecialTerm
                        > in your red blood cells that is responsible for carrying oxygen to your organs. Oxygen is essential
                        for your cells to function, and without it, large groups of cells called tissues will die, potentially
                        causing organ damage. Additionally, hemoglobin contains large amounts of iron, which gives blood
                        its distinctive red color and metallic smell.
                    </div>
                    <div slot="second">
                        <InlineImage url="https://upload.wikimedia.org/wikipedia/commons/3/3d/1GZX_Haemoglobin.png" />
                    </div>
                </TwoColumn>
                <h3>DNA, Hemoglobin, and Sickle Cell Disease</h3>
                <p>
                    DNA is a large, double-stranded organic molecule made up of long sequences of <SpecialTerm
                        definition={'A sugar-based molecule that consists the "rungs" on the ladder-shaped model of DNA that is commonly seen in scientific literature.'}
                        >nucleobases</SpecialTerm
                    > that arrange themselves in units called genes. Many genes, such as the one affected by SCD correspond
                    to sequences of molecules that make up proteins. As mentioned before, SCD is caused by a defective gene
                    in one's body. This gene, called the <SpecialTerm
                        definition={'Short for "Hemoglobin Subunit Beta" gene.'}>HBB gene</SpecialTerm
                    >, is responsible for producing parts of the protein that produces hemoglobin in your blood. The <SpecialTerm
                        definition="An unintended change in one's DNA. Mutations happen in the body frequently, but most are harmless and are automatically fixed by your cells. Some mutations, such as in the case of SCD, are harmful and can be passed on from generation to generation."
                        >mutation</SpecialTerm
                    > in this gene that causes SCD deforms the hemoglobin protein, turning it into a faulty type of hemoglobin
                    referred to as <i>hemoglobin S</i>. These abnormally shaped hemoglobin proteins cause the red blood
                    cell to <i>sickle</i>, or deform, causing their characteristic <SpecialTerm
                        definition="A sickle is a farm implement similar to a scythe. Sickled red blood cells have a crescent shape resembling the blade of a sickle."
                        >sickle-shaped</SpecialTerm
                    > appearance.
                </p>
            </div>
        </TwoColumn>
        <div>
            <h1>CRISPR Genome Editing</h1>
            <h3>What is CRISPR/Cas9?</h3>
            <p>
                You may have heard about a fairly new gene-editing technology in the news commonly referred to as
                <SpecialTerm
                    definition="An acronym for Clustered Regularly Interspaced Short Palindromic Repeats. Refers to sequences of DNA that can be identified and destroyed by cells. More information below."
                    >CRISPR</SpecialTerm
                >. <SpecialTerm
                    definition="Past gene-editing techniques were often imprecise or unreliable and could lead to unintended side effects in the target organism."
                    >Ideally</SpecialTerm
                >, gene editing allows scientists to precisely and accurately add, modify, or remove sequences of bases
                in an organism's DNA. In doing so, scientists are given precise control over the genes that dictate the
                creation of proteins or the expression of traits such eye color, hair color, height, resistance to
                certain diseases, and much more. Cas9 refers to the protein that allows CRISPR to work. Cas9 itself
                stands for <i>CRISPR-associated endonuclease 9</i>. The Cas9 protein exists naturally in bacteria as a
                way to identify and cut viral DNA, acting as a defense mechanism against viruses. In using CRISPR/Cas9
                for gene-editing, we use the Cas9 protein to cut the cell's own DNA rather than that of a virus or other
                foreign body.
            </p>
            <p>
                To identify the DNA Cas9 protein carries a segment of <i>guide RNA</i>, sometimes called <SpecialTerm
                    definition={'Short for "single guide RNA"'}>sgRNA</SpecialTerm
                >. RNA is similar to DNA in that it is a large organic molecule made up of four unique bases. RNA in
                general acts as a complementary molecule to DNA. It can be used to store copies of genetic sequences and
                be used to replicate or identify them, as it is used in this case. Once Cas9 identifies the target
                sequence of DNA as a complementary match to its guide RNA, the Cas9 protein cuts the DNA, prompting the
                cell to repair the strand.
            </p>
            <h3>Homology-Directed Repair</h3>
            <p>
                <SpecialTerm
                    definition="Homology, in genetics, refers to a state of similarity, or having a similar structure."
                    >Homology-Directed</SpecialTerm
                > Repair (HDR) is a mechanism whereby DNA strands that were broken by the Cas9 protein can be repaired. When
                the cell detects a <SpecialTerm
                    definition="Remember DNA is double-stranded. A break in the DNA sequence such as that induced by the Cas9 protein sever both strands of the molecule, initiating a repair."
                    >double strand break</SpecialTerm
                > (DSB) in one of its DNA strands, the cell looks for a nearby segment of DNA that it can use to patch the
                break in the DNA. Specifically, it looks for strands of DNA that contain matching sequences of DNA to the
                ends that were just cut. This is where the term "homology" in homology directed repair comes into play. The
                cell then uses these sequences as templates with which to fill in the gap created by the Cas9 protein.
            </p>
            <p>
                This mechanism allows scientists, by means of intentionally cutting parts of the DNA and providing large
                amounts of template/donor DNA strands along with the engineered Cas9 proteins, to insert or modify
                specific parts of a genetic sequence. A diagram for homology-directed repair is illustrated below.
            </p>
            <HdrDiagram />
        </div>
        <h1>CRISPR Applications in Treating Sickle Cell Disease</h1>
        <p>
            The mechanisms by which scientists are able to precisely edit DNA can be used to treat genetic disorders
            such as sickle cell anemia. As mentioned before, with traditional methods involving bone marrow
            transplantation, in can be difficult to find a sufficient bone marrow donor. In the United States, less than
            20% of patients are able to find a donor to sustain this treatment (Jean-Antoine Ribeil, M.D., et. al.).
            This is why finding an alternative method that can be generalized to more people is essential.
        </p>
        <h3>What About the Sickle-Cell Gene Causes Sickle Cell?</h3>
        <p>
            More specifically, CRISPR allows scientists to edit the HBB gene (described above). In this gene, a specific
            sequence of bases (<SpecialTerm definition="Short for the chemical adenine">A</SpecialTerm>, <SpecialTerm
                definition="Short for the chemical guanine">G</SpecialTerm
            >, <SpecialTerm definition="Short for the chemical cytosine">C</SpecialTerm>, and <SpecialTerm
                definition="Short for the chemical thymine">T</SpecialTerm
            >) defines the structure of the hemoglobin protein. Each pair of three bases, or letters, corresponds to an
            <SpecialTerm
                definition="A building block of protein. Every protein is made up of a specific sequence of amino acids that defines the structure and function of that protein."
                >amino acid</SpecialTerm
            > that is used to construct the protein. In the case of the faulty HBB gene, a single letter near the middle
            of the genetic sequence is <SpecialTerm
                definition="This changes a single amino acid in the hemoglobin protein from glutamic acid to valine."
                >changed from a A to a T</SpecialTerm
            >. This single modification, as small is it may seem in comparison to the billions of letters that make up
            the complete human genome, has dramatic ramifications.
        </p>
        <h3>CRISPR Treatment of the Sickle Cell Gene</h3>
        <p>
            As mentioned before, CRISPR allows scientists to precisely and accurately modify sequences of DNA. If the
            process of Cas9 DNA-cutting and homology directed repair were used to edit the T back into an A, then the
            proteins produced by these modified cells would not be conducive to producing sickled red blood cells.
        </p>
        <h3>Methodology</h3>
        <p>
            As CRISPR technology is still fairly new, and the safety of genenome editing in human patients is still not
            completely understood, current scases where CRISPR is used to treat sickle cell anemia, despite showing
            promise for being useful in the future, are rare. In one case study, <SpecialTerm
                definition="Stem cells are unspecialized cells in the body that can turn into any other type of cell in the body. In the context of bone marrow, stem cells are the raw ingredients for red blood cells."
                >stem cells</SpecialTerm
            > were collected from a patient's bone marrow to be genetically modified in a lab. After the process of CRISPR
            gene editing was applied on these cells, the modified tissue was inserted back into the patients bone marrow.
            In a period of fifteen months after the gene treatment had occurred, no notable sickle-cell-related events such
            as <SpecialTerm
                definition="Anemia can cause episodic pain that can range from mild to severe. More information above."
                >pain crises</SpecialTerm
            > were observed, and the patient was discharged with <SpecialTerm
                definition="Most of the side effects that did occur were related to infection, not gene editing, due to the process of drilling into the bone, an invasive and somewhat risky process."
                >minimal side effects</SpecialTerm
            >.
        </p>
        <i
            >The full case study, as it was described here, can be found <a
                href="https://www.nejm.org/doi/full/10.1056/NEJMoa1609677">here</a
            > or in the references section below.</i
        >
        <h3>More Information</h3>
        <p>
            Here is a video by the <a href="https://www.genome.gov/">National Human Genome Research Institute</a> explaining
            the details of this treatment in more detail
        </p>
        <iframe
            title="Embedded Youtube Video"
            src="https://www.youtube.com/embed/3mKj8iLcHKg"
            frameborder="0"
            style="width: 60vh; height: 40vh;"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
        />
        <h3>Conclusion</h3>
        <p>
            Gene therapy using CRISPR/Cas9 technology can be a very effective and far more accessible method of treating
            sickle cell disease, a condition that was previously incurable. This is not to say that there are not
            drawbacks of using this method. As mentioned before, the side effects of gene editing are not well
            understood, especially in humans. Although CRISPR is far more precise in gene editing than some earlier
            methods, unintended edits to the genetic sequence can cause harmful results, including cancer.
        </p>
        <p>
            Despite this, gene therapy continues to evolve, and current research shows promise that, with time, gene therapy
            will be used as a new way to treat the millions around the world who continue to suffer from genetic
            disorders.
        </p>
        <Bibliography websiteSources={sources} />
        <p style="font-size: 12pt; opacity: 0.5; font-style: italic;">
            The information and resources on this site are not intended to treat, diagnose, or serve as a replacement
            for advice from a qualified medical professional.
        </p>
    </div>
    <div class="footer">
        I built this website from scratch! Check out the source code <a href="https://github.com/iahuang/crispr-project"
            >here</a
        >.
    </div>
</main>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Raleway:wght@100&display=swap");
    .header {
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        /* background-color: #17222b; */
        color: white;
        padding-bottom: 10px;
        background-image: url(https://frontlinegenomics.com/wp-content/uploads/2020/12/bioengineering-scaled.jpg);
        background-position: right;
        background-size: cover;
        padding-bottom: 50px;
    }

    .header > h1 {
        color: white;
        user-select: none;
        padding-top: 10px;
        font-family: "Raleway", sans-serif;
        font-weight: 100;
        font-size: 5vw;
        text-shadow: 0px 0px 40px white, 0px 0px 30px white, 0px 0px 20px white, 0px 0px 10px white;
    }

    .main {
        padding-left: 10vw;
        padding-right: 10vw;
    }

    .footer {
        width: 100%;
        background-color: rgba(0, 0, 0, 0.05);
        bottom: 0;
        padding: 20px;
    }
</style>
