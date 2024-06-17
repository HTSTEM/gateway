<script>
    import Button from "$lib/Button.svelte";
    import Logo from "$lib/Logo.svelte";
    import Path from "$lib/Path.svelte";
    import MainContent from "$lib/MainContent.svelte";
    import SubContent from "$lib/SubContent.svelte";
    import FormattedDate from "$lib/FormattedDate.svelte";
    import Label from "$lib/Label.svelte";
</script>

<Path pathSegments={["Home", "Press releases"]}></Path>
<Logo/>
<MainContent>
    <SubContent>
        <h1>HTwins STEM issues statement regarding recent allegations of homophobia</h1>
        <Label><FormattedDate date={new Date(2021, 11, 23)}/></Label>
    </SubContent>
    <SubContent>
        <p>
            It is with a heavy heart that HTwins STEM acknowledges recent developments surrounding allegations of a
            less-than-inclusive community environment for members of the LGBTQ+ community. These claims are
            fundamentally misaligned with our core values of synergy and collaborative excellence.
        </p>
        <p>
            We, at HTwins STEM, are committed to fostering a culture of open communication and psychological safety.
            Homophobic behavior is simply not accretive to our bottom line, nor does it synergize with our mission of
            connecting users from all across the globe.
        </p>
        <p>
            While the specifics of this internal investigation remain confidential to protect the integrity of the
            process, rest assured, we are laser-focused on identifying any potential roadblocks to achieving an optimal
            work environment. Transparency and accountability are paramount as we navigate this situation.
        </p>
        <p>
            Regaining the trust of our valued team members is a top priority. Further communication will be disseminated
            internally through the appropriate channels at a later date to outline the action plan for achieving this
            objective. It is our sincere desire to ensure HTwins STEM remains a best-in-class community where all
            individuals can leverage their unique skillsets and contribute to our collective success.
        </p>
        <p>
            Diversity and inclusion are not just buzzwords at HTwins STEM; they are the cornerstones of the
            thriving and welcoming community we strive to be. We are dedicated to cultivating a community that
            reflects the rich tapestry of diverse people from all across the globe.
        </p>
        <p>
            Sincerely,
        </p>
        <p>
            The HTwins STEM team
        </p>
    </SubContent>
</MainContent>
