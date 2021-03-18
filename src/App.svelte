<script lang="ts">
    import Bibliography from "./components/Bibliography.svelte";
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
            <h1>CRISPR Gene Therapy for Sickle Cell Disease</h1>
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
                > Repair is a mechanism whereby DNA strands that were broken by the Cas9 protein can be repaired.
            </p>
        </div>
        <Bibliography websiteSources={sources} />
        <p style="font-size: 10pt; opacity: 0.5; font-style: italic;">
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
