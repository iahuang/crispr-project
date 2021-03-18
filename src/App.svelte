<script lang="ts">
    import Bibliography from "./components/Bibliography.svelte";
    import InlineImage from "./components/InlineImage.svelte";
    import SpecialTerm from "./components/SpecialTerm.svelte";
    import TwoColumn from "./components/TwoColumn.svelte";
    import type { MLASource } from "./mla";

    const sources: MLASource[] = [
        {
            author: "Suzan Howler",
            title: "Top 10 Anime Deaths",
            organization: "Harvard University",
            url: "https://urmom.com",
        },
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
                        <h3>Hemoglobin</h3>
                        Hemoglobin (also spelled <i>haemoglobin</i>) is a <SpecialTerm
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
                <h3>The Genetics of Sickle Cell Disease</h3>
                <p>
                    As mentioned before, SCD is caused by a defective gene in one's body. This gene, called the <SpecialTerm
                        definition={'Short for "Hemoglobin Subunit Beta" gene'}>HBB gene</SpecialTerm
                    >, is responsible for producing parts of the protein that produces hemoglobin in your blood. The <SpecialTerm
                        >mutation</SpecialTerm
                    > in this gene that causes SCD deforms the hemoglobin protein, turning it into a faulty type of hemoglobin
                    referred to as <i>hemoglobin S</i>
                </p>
            </div>
        </TwoColumn>
        <Bibliography websiteSources={sources} />
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
        padding: 40px;
    }

    .footer {
        width: 100%;
        background-color: rgba(0, 0, 0, 0.05);
        bottom: 0;
        padding: 20px;
    }
</style>
