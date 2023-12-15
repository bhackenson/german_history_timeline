<script>
    import { slide } from "svelte/transition";

    let text = "";

   let data = [
    {
        "id": 100,
        "year": "1815-1918",
        "period": "Age of Industrialization",
        "is_visible": true,
        "events": [
            {
                "id": 1,
                "year": "1814-1815",
                "title": "Congress of Vienna",
                "is_visible": true,
                "description": {
                    "definition":"The Congress of Vienna was a series of meetings held in Vienna to decide a new layout of Europe. Important historical figures included the representatives of the European powers as well as Austrian statesman Klemens von Metternich, the architect of the meetings. (96-104)",
                    "causes": "The downfall of the French emperor Napoleon Bonaparte left Europe in disarray. The meetings were designed to both to restore and balance state boundaries and prevent another large-scale war from occurring again. (96-104)",
                    "impact": "While the Congress of Vienna was successful in preventing major outbreaks for nearly a century, its conservative tendencies led to suppression of liberal movements that would lead to protests like those in 1848. (104)"
                }
            },
            {
                "id": 2,
                "year": "1848-1849",
                "title": "Revolutions of 1848",
                "is_visible": true,
                "description":{
                    "definition": "The revolutions of 1848 were a series of protests and insurrections across Europe involving social unrest, demanding old forms of regulation, liberal policies in a constitutional rule, economic freedom, and in Germany, calls for unification. (116)",
                    "causes": "Long-term effects throughout the 1840s culminated in social unrest, particularly mounting indebtedness over the decade. There were also false hopes of liberalization, where King Frederick Wilhelm IV proved to be a conservative monarch since his acquition of the throne in 1840. The moment that triggered the continent-wide protests was the February Revolution in France, toppling King Louis Philippe. (116-117)",
                    "impact": "The revolutions from 1848-1849 in Germany were not able to unite Germany or cause dramatic liberal changes. However, there were some consequences as a result of the revolutions, including the end of feudal social relations and a reorganized economic life that would lead to economic growth in the 1850s. (121)"
                }
            },
            {
                "id": 3,
                "year": "1866-1871",
                "title": "Unification of Germany",
                "is_visible": true,
                "description": {
                    "definition": "The unification of Germany was a process of building a nation-state for Germans. (122)",
                    "causes": "The Congress of Vienna established a German Confederation from the states of the Holy Roman Empire as part of its border restructuring. Austria was the center of this Confederation, but Prussia saw large economic growth throughout the mid-nineteenth century, which would raise the question of who would lead a unified Germany. Ultimately, as a result of Prussian expansionism and colonization, Prussia, guided by Otto von Bismarck, would claim victory. In 1866, a new federation called the North German Confederation was created, which excluded Austria and other South German states including Bavaria, Baden, Wurttemburg, and Hesse-Darmstadt. This Confederation went to war with Austria in 1866, which threatened France and its perceived dominance in Europe, leading to the Frano-Prussian War of 1870, which Prussia won. These conflicts ultimately led to the creation of a unified German empire led by Prussia in 1871. (127-131)",
                    "impact": "The unification of Germany resulted in the German Empire, which would last until the end of World War I. (127-131)"
                }
            },
            {
                "id": 4,
                "year": "1871-1914",
                "title": "The Road to World War I",
                "is_visible": true,
                "description": {
                    "definition": "The 'Road to World War' denotes a series of changes that occurred in the German Empire from 1871 to 1914 that would lead to the First World War. First, there was a shift in foreign policy after Bismarck, where Germany grew more ambitious in seeking world power status. Second, there became a formation of an alliance between Germany, Austria, and Italy, called the 'Triple Alliance'. There was also a formation of an alliance between France, Russia, and Britain, called the 'Triple Entente.' Third, there was an arms race. There grew a sense throughout Europe that war was imminent and prepared themselves accordingly. (148-155)",
                    "impact": "The above changes since the formation of the German Empire -- goals on world power status, forming alliances, and an arms race -- would create many of the conditions that would spark the beginning of World War I in 1914. (148-155)"
                }

            },
            {
                "id": 5,
                "year": "1914-1918",
                "title": "World War I",
                "is_visible": true,
                "description": {
                    "definition": "World War I was a global conflict from 1914 to 1918 between the Allied Powers, which included France, the United Kingdom, Russia, the United States, Italy, and Japan, and the Central Powers, which included Germany, Austria-Hungary, Bulgaria, and the Ottoman Empire. (148-154)",
                    "causes": "Alliances, militarism, nationalism, and imperialism are generally considered the causes of World War I, with the assassination of Austrian Archduke Franz Ferdinand in June 1914 triggering the global conflict. (148-154)",
                    "impact": "WWI effectively ended any existing empire in place of republicanism, including the German Empire, which was replaced with the Weimar Republic. (148-154)"
                }
            }
        ]
    },
    {
        "id": 101,
        "year": "1918-1945",
        "period": "The Weimar Republic and Nazi Germany",
        "is_visible": true,
        "events": [
            {
                "id": 6,
                "year": "1918-1924",
                "title": "The Weimar Republic Early Years",
                "is_visible": true,
                "description": {
                    "definition": "The Weimar Republic was established after the end of WWI. Prince Max von Baden implemented a series of reforms including the reform of suffrage and control of the armed forces by the civilian government instead of the monarchy. However, these reforms would soon be overtaken by more radical ideas. Germany would instead develop a series of compromises that would please neither left nor right. They also did not reform key elites including the army, bureaucracy, and religious institutions. Power was eventually handed over to Friedrich Ebert, who implemented two major compromises: the Ebert-Groener pact, which allowed Ebert to use General Groener's army to suppress radical movements as long as he stayed moderate himself, and the Stinnes-Legien agreement, which reorganized labor. This transition of power would also prove futile as Ebert still did not implement economic reform or reform the army. (156-167)",
                    "impact": "The Weimar Republic failed to address the radical movements early on. The Weimar government also included an extremely far-reaching law that allowed the right to rule by emergency decree. Both of these issues would help create the conditions in Germany that led to Hitler's rise to power. (156-167)"
                }
            },
            {
                "id": 7,
                "year": "1924-1928",
                "title": "Weimar Republic Stabilization and Society",
                "is_visible": true,
                "description": {
                    "definition": "In 1924-1928, there was a period of stabilization in the Weimar Republic. New pacts and treaties were signed, including the Dawes Plan of 1924, which combined German interests with American economic expansionism. Germany also became a member of the League of Nations. Culturally, the Weimar Republic had advancements in the natural sciences, psychology, and architecture. (167-172)",
                    "impact": "Despite these advancements, people in the Weimar Republic still were not committed to the political reform and yearned for the return of Imperial Germany. Nationalist hero Hindenburg was elected as the new President, who considered plans for the development of a right-wing government. (167-172)"
                }
            },
            {
                "id": 8,
                "year": "1929-1933",
                "title": "Collapse of the Weimar Republic",
                "is_visible": true,
                "description": {
                    "definition": "The collapse of the Wiemar Republic was an event that dismantled the parliamentary democracy in Germany in 1929. (172-179)",
                    "causes": "The global economic depression in 1929 is partly to blame for the collapse of the Weimar Republic, since Germany at the time depended on short-term loans from other countries. However, even before the depression, there were already plans by opposing parties to dismantle Weimar Germany. (172-179)",
                    "impact": "The attacks on Weimar Germany by the old elites, and additionally a large proportion of the population persuaded by a new leader figure Adolf Hitler, would lead to both the fall of the Republic and a consolidation of power led by Hitler for the rest of the decade. (172-179)"
                }
            },
            {
                "id": 9,
                "year": "1933-1939",
                "title": "The Rise of Hitler",
                "is_visible": true,
                "description": {
                    "definition": "The consolidation of Hitler's power was a period between the end of the Weimar Republic and World War II. Hitler was able to convice other parties to support his plans, and by preventing the communists and Social Democrats from attending the Reichstag on March 23, 1933, Hitler passed the Enabling Act, giving him total control over laws passed. The Nazi Party subsequently outlawed other parties and warped Germany in his image, changing trade unions to the 'German Labour Front', abolishing the parliament, and combining President and Chancellor to 'Fuhrer'. In March 1933 the first concentration camp was opened in Dachau, which was designed mainly for political opponents and minorities. Native Germans had to live a double life and express their true political views only in complete privacy, though some supported the new regime for its reduced unemployment and an improved standard of living albeit these restrictions on personal freedom. (179-187)",
                    "impact": "The Rise of Hitler would ultimately culminate in the invasion of Poland in 1939, beginning World War II. (179-187)"
                }
            },
            {
                "id": 10,
                "year": "1939-1945",
                "title": "World War II",
                "is_visible": true,
                "description": {
                    "definition": "World War II was a global conflict from 1939-1945 between the Allied Powers, which included the United Kingdom (from 1939), the United States (from 1941), and the Soviet Union (from 1941), and the Axis Powers, which included Nazi Germany, Italy, and Japan. The war began as a conflict in Western Europe, but Hitler did not anticipate the difficulty of taking down the United Kingdom. Regardless, Hitler wished to invade the east as well and began a two-front war, and the U.S.'s declaration of war against Japan led to Hitler declaring war on the U.S., even though Germany did not need to immediately come to Japan's defence. Hitler was now taking on three of the greatest powers in the world -- Great Britain, the U.S., and the Soviet Union -- at the same time, and would ultimately be defeated after his suicide in 1945. (179-187)",
                    "causes": "The immediate cause of WWII was Hitler's invasion of Poland in September 1939. During Hitler's rise to power, other countries noticed Germany's militarization, but did nothing to combat it. In particular, British Prime Minister Chamberlain led an 'appeasement policy' in hopes of preventing another global war. Hitler also made a strategic pact between Germany and the Soviet Union so he could prevent a two-front war, allowing him to more easily invade Poland and control Western Europe before turning east. (179-187)",
                    "impact": "World War II was the dealiest conflict in history. Hitler's goals were to not only claim world dominance with the German race at the top, but to also rid of what he considered a pollutant: the Jews. The Holocaust was a state-sponsored genocide that killed around 6 million Jews. (179-187)"
                }
            }
        ]
    },
    {
        "id": 102,
        "year": "1945-1990",
        "period": "The Cold War",
        "is_visible": true,
        "events": [
            {
                "id": 11,
                "year": "1945-1949",
                "title": "Creation of the Two Germanies",
                "is_visible": true,
                "description": {
                    "definition": "The creation of the two Germanies occurred following the end of World War II. It was agreed by the Allied Powers that Germany would be split into different zones of occupation, with the U.S., France, and Britain in West Germany, and the Soviet Union in East Germany. The city of Berlin was also similarly divided. The two sides rapidly divereged. The Soviets swiftly introduced a Communist-style party that would take control of East Germany, in addition to land reform and redistribution. Meanwhile, Britain, France, and the U.S. implemented a capitalist market economy. (205-212)",
                    "impact": "West Germany gained full sovereignty and became a member of NATO and experienced a significant economic recovery. Meanwhile, East Germany continued to undergo polical changes, and its centralized economy was not able to rival the market economy of West Germany. As a result, many people crossed to West Germany from East Germany, as well as to West Berlin from East Berlin, which led to East Germany building a wall around Berlin to prevent individuals from leaving the country. These political differences became understood as an 'Iron Curtain' between the West and East and would become a powerful symbol of the Cold War. (205-212)"
                }
            },
            {
                "id": 12,
                "year": "1961-1989",
                "title": "The Berlin Wall",
                "is_visible": true,
                "description": {
                    "definition": "The Berlin Wall was a physical barrier that surrounded West Berlin in East Germany. (213)",
                    "causes": "Due to the economic success of West Berlin and West Germany, and other factors like the restrictions on freedom in East Germany, many East German citizens hoped to cross to West Germany. Consequently, the Berlin Wall was built to prevent East Berliners from crossing to West Germany. (205-213)",
                    "impact": "The Berlin Wall became a symbol of the Cold War that created a literal barrier between the East and the West. It also symbolized the supression of the freedom of movement and expression by East Germany. (205-213)"
                }
            },
            {
                "id": 13,
                "year": "1950-1990",
                "title": "The Stasi",
                "is_visible": true,
                "description": {
                    "definition": "The Stasi was the secret police of East Germany from 1950-1990. (226)",
                    "causes": "The East German government was concerned of political opponents, so the secret police was established as a means of surveillance and intimidation to shut down opponents and have citizens conform to the wishes of the regime. (226)",
                    "impact": "The Stasi in addition to the Berlin Wall was a symbol of suppression in East Germany. Toward the end of the Cold War there were increasing numbers of demonstrations against the regime and calls for reunificaiton with West Germany. (226)"
                }
            },
            {
                "id": 14,
                "year": "1989",
                "title": "Revolution of 1989",
                "is_visible": true,
                "description": {
                    "definition": "The Revolution of 1989 was a series of significant changes in East Germany in 1989, including border openings in Soviet satellite states and mass demonstrations against the East German government. (243-250)",
                    "causes": "East Germany was suffering due to a weak Soviet economy, which could not maintain the defense spending. Gorbachev of the Soviet Union enacted several changes in the Soviet Union, including some levels of democratisation as well as economic reform. There were also external changes, including Hungary dismantling the fortified border it had with Austria. These changes triggered a movement of people wishing to cross to the West. On November 9, 1989, a government spokesman stated individuals would be allowed to travel freely between East and West Berlin, effectively ending the purpose of the Berlin Wall. The Wall would be destroyed soon after. (243-250)",
                    "impact": "The Revolution of 1989, and later the collapse of the Soviet Union, were monumental events in history and are the events that marked the end of the Cold War. The end of the Berlin Wall and the Soviet Union left the task of incorporating a collapsed Communist state with a capitalist one. (243-251)"
                }
            }
        ]
    }
]

let filters = [
    {
        "id": 1,
        "on": false,
        "title": "Wars and Conflicts",
        "events": [3, 5, 10]
    },
    {
        "id": 2,
        "on": false,
        "title": "Political Developments",
        "events": [1, 3, 4, 6, 7, 8, 9, 11, 12, 13]
    },
    {
        "id": 3,
        "on": false,
        "title": "Social Movements and Revolutions",
        "events": [2, 14]
    },
    {
        "id": 4,
        "on": false,
        "title": "Economic Developments",
        "events": [2, 3, 6, 7, 8, 11]
    }
]

function toggle_period(id) {
    let period = data.find(x => x.id == id);
    period.is_visible = !period.is_visible;
    for (let f of filters) { f.on = false; }
    data = data;
    filters=filters;
}

function toggle_event(pid, eid) {
    let period = data.find(x => x.id == pid);
    let event = period.events.find(x => x.id == eid);
    event.is_visible = !event.is_visible;
    for (let f of filters) { f.on = false; }
    data = data;
    filters=filters;
}

function split_str_by_substr(str, substr) {
    const index = str.indexOf(substr);

    if (index !== -1) {
        return [
            {id: 0, s: str.substring(0, index)},
            {id: 2, s: substr},
            {id: 3, s: str.substring(index + substr.length)}
        ];
    } else { return [
        {id: 0, s: str},
        {id: 2, s: ""},
        {id: 3, s: ""}
    ]; }
}

function filter_events(fid) {
    let f = filters.find(x => x.id == fid);
    if (f.on) {
        f.on = false;
        for (let p of data) {
            p.is_visible = true;
            for (let e of p.events) { e.is_visible = true; }
        }
    }
    else {
        f.on = true;
        for (let fltr of filters) { if (fltr.id != f.id) {fltr.on = false;} }
        const events_f = f.events;
        for (let p of data) {
            let p_flag = false;
            for (let e of p.events) {
                if (events_f.includes(e.id)) {
                    p_flag = true;
                    p.is_visible = true;
                }
            }
            if (!p_flag) { p.is_visible = false; }
        }
        const events = [...data[0].events, ...data[1].events, ...data[2].events]
        for (let e of events) { e.is_visible = events_f.includes(e.id) ? true : false; }
    }
    filters=filters;
    data=data;
}

function reset() {
    text = "";
    for (let p of data) {
        p.is_visible = true;
        for (let e of p.events) { e.is_visible = true; }
    }
    for (let f of filters) { f.on = false; }
    data=data;
    filters=filters;
}

</script>
<body>
    <div class='title'>
        <h1>Timeline of German History, 1815-1989</h1> <hr>
    </div>
        <div class='options'>
        <div class = 'filter'>
            <h1>Filter</h1> <br>
            {#each filters as f (f.id)}
                <button class='button {"clicked_" + f.on}' type='button' on:click={() => filter_events(f.id)}>{f.title}</button>
            {/each}
        </div>
        <div class='search'>
            <h1>Search</h1> <br>
            <input class = 'input' type="text" bind:value={text} name="Search" placeholder="Search" on:click={reset}>
        </div>
    </div>
    <div>
        {#each data as p (p.id)}
            <div class='period {"c" + p.id}'>
                <div class='cursor' on:click={() => toggle_period(p.id)} >
                    <h1>{p.period}</h1>
                    <h2>{p.year}</h2>
                </div> 
                {#if p.is_visible}
                    <div transition:slide="{{y: p.is_visible ? 0 : 100}}">
                        {#each p.events as e (e.id)}
                            <div class='event'>
                                <div class='cursor center' on:click={() => toggle_event(p.id, e.id)}>
                                    <h3>{e.title}</h3>
                                    <h4>{e.year}</h4>
                                </div>
                                {#if e.is_visible}
                                    <div transition:slide="{{y: e.is_visible ? 0 : 100}}">
                                        <li><b>Definition: </b>
                                            <!-- {e.description.definition} -->
                                            {#each split_str_by_substr(e.description.definition, text) as t (t.id)}
                                                {#if t.id == 2}
                                                    <mark>{t.s}</mark>
                                                {:else} {t.s}
                                                {/if}
                                            {/each}
                                        </li>
                                        {#if "causes" in e.description}
                                            <li><b>Causes: </b>
                                                <!-- {e.description.causes} -->
                                                {#each split_str_by_substr(e.description.causes, text) as t (t.id)}
                                                    {#if t.id == 2}
                                                        <mark>{t.s}</mark>
                                                    {:else} {t.s}
                                                    {/if}
                                                {/each}
                                            </li>
                                        {/if}
                                        <li><b>Impact: </b>
                                            <!-- {e.description.impact} -->
                                            {#each split_str_by_substr(e.description.impact, text) as t (t.id)}
                                                {#if t.id == 2}
                                                    <mark>{t.s}</mark>
                                                {:else} {t.s}
                                                {/if}
                                            {/each}
                                        </li>
                                    </div>
                                {/if}
                            </div>
                        {/each}
                    </div>
                {/if}
            </div>
        {/each}
    </div>
    <div class='references'>
        <br>
        <h1>References</h1>
        <p>Fulbrook, Mary. <i>A Concise History of Germany.</i> 3rd ed. Cambridge, England: Cambridge University Press, 2019.</p>

    </div>
</body>

<style>
    * {
        margin: 0.5;
        padding: 0.5;
        box-sizing: border-box;
        font-family: sans-serif;
    }

    h1, h2, h3, h4 {
        margin-top: 0;
        margin-bottom: 0;
        padding-top: 0;
        padding-bottom: 0;
    }

    .cursor {
        cursor: pointer;
    }

    .center {
        text-align: center;
    }
    
    .event {
        border-radius: 0.7rem;
        text-align: left;
        background-color: #f3f3f3;
        margin-top: 2rem;
        margin-bottom: 1rem;
        margin-left: 2rem;
        padding-left: 1.5rem;
        padding-right: 1.5rem;
        padding-top: 1rem;
        padding-bottom: 1rem;
        width: 95%;
    }

    .period {
        justify-content: center;
        text-align: center;
        padding-top: 0.5rem;
        padding-bottom: 0.5rem;
        border-radius: 0.5rem;
        margin-bottom: 1rem;
    }

    .options {
        display: flex;
    }

    .search, .filter {
    border-radius: 0.7rem;
    background-color: #eee;
    margin-top: 2rem;
    margin-left: 0.5rem;
    margin-right: 0.5rem;
    margin-bottom: 2rem;
    padding-left: 1.5rem;
    padding-right: 1.5rem;
    padding-top: 1rem;
    padding-bottom: 1rem;
    width: 100%; 
    max-width: 1500px;
    }

    .input {
    border-style: none;
    display: block;
    width: 100%;
    font-size: 1.125rem;
    padding: 1rem 1.5rem;
    background-color: rgb(255, 255, 255);
    border-radius: 0.5rem;
    margin-bottom: 1rem;
}

    .button {
        cursor: pointer;
        border-style: none;
        display: block;
        width: 100%;
        font-size: 1.125rem;
        padding: 1rem 1.5rem;
        color: #272741;
        background-color: rgb(255, 255, 255);
        border-radius: 0.5rem;
        margin-bottom: 1rem;
    }

    .button:hover {
        opacity: 0.7;
    }

    .clicked_true {
        background-color: #e3e3e3;
    }

    .c100 {
        background-color: rgb(244, 216, 244);
    }

    .c101 {
        background-color:rgb(201, 237, 226);
    }

    .c102 {
        background-color:rgb(201, 229, 238);
    }

    .title {
        text-align: center;
    }
    
    body {
        justify-content: center;
        align-items: center;
        width: 100%;
        max-width: 1450px;
    }
</style>