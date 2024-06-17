<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import FormattedDate from "$lib/FormattedDate.svelte";
</script>

<Path pathSegments={["Home", "Community"]}></Path>
<Logo />
<MainContent>
    <h1>Verify your eligibility to participate in the HTwins STEM community</h1>
    <SubContent>
        <h2>Overview</h2>
        <p>
            Starting <FormattedDate date={new Date(2024, 5, 17)} />, both new and existing HTSTEM members will need to
            pass a heterosexuality assessment form to talk in our community. The form must be completed by
            <FormattedDate date={new Date(2024, 5, 23)} />, after which people that have not completed the form will
            not be able to speak in the server until they do.
        </p>
        <Button href="/community/assessment" text="Take the self-assessment form"/>
    </SubContent>
    <SubContent>
        <h2>What is the heterosexuality assessment form?</h2>
        <p>
            The heterosexuality assessment form is a brief questionnaire designed to protect the community and foster a more inclusive
            environment. The multiple-choice format ensures a quick and easy process.
        </p>
    </SubContent>
    <SubContent>
        <h2>Why do I need to complete the heterosexuality assessment form?</h2>
        <p>
            At HTwins STEM, we are proud to celebrate Pride Month and stand firmly in our commitment to cultivating a diverse
            and inclusive environment for all STEM enthusiasts. We recognize the invaluable contributions of LGBTQ+ individuals
            to science, technology, engineering, and mathematics throughout history and in the present day. We believe that
            Pride shouldn't just last for the month of June. We believe that Pride should be year-round, which is why we're
            introducing this self-assessment form to ensure that HTwins STEM is as inclusive as possible.
        </p>
        <p>
            Our core values include fostering a respectful and inclusive space. We have zero tolerance for discrimination or
            harassment based on sexual orientation or gender identity. We provide clear guidelines and resources to ensure all
            members feel valued and secure.
        </p>
        <p>
            We actively celebrate the achievements of LGBTQ+ individuals in STEM fields through various initiatives. This may
            involve sharing profiles of prominent LGBTQ+ figures, curating articles highlighting their contributions, or hosting
            discussions focused on their accomplishments.
        </p>
        <p>
            Furthermore, we offer dedicated resources and support groups specifically tailored to the needs of our LGBTQ+
            members. This can include online forums or designated channels for members to connect, share experiences,
            and build a strong sense of community.
        </p>
        <p>
            We understand the importance of education and strive to raise awareness about LGBTQ+ issues within STEM fields. This
            may involve hosting webinars featuring LGBTQ+ professionals, sharing informative articles, or creating content that
            explores the challenges and opportunities faced by LGBTQ+ individuals in STEM careers.
        </p>
    </SubContent>
</MainContent>
