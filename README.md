# aksa_
{
            id: "murabit-ilim-halkasi",
            name: "Mescid-i Aksa Seher İlim Halkası",
            era: "Sivil Direniş & Nöbet",
            desc: "Kıble Mescidi ve Kubbetü's-Sahre avlusunda kesintisiz sabah namazı ve ilim halkası kur.",
            cost: { spirit: 30, lore: 15, defense: 15 },
            rewardDays: 30,
            bonusText: "+30 Gün Sefer İlerlemesi • Nihai Seher Kapısını Aç"
        }
    ];

    // --- 6 ÇAĞ / SEZON VERİSİ ---
    const seasonsData = [
        { id: 1, title: "1. Çağ: Surlar ve Kapılar", startDay: 1, endDay: 30 },
        { id: 2, title: "2. Çağ: Eyyubi İhyası", startDay: 31, endDay: 60 },
        { id: 3, title: "3. Çağ: Osmanlı Emaneti", startDay: 61, endDay: 90 },
        { id: 4, title: "4. Çağ: Tapu ve Hukuk", startDay: 91, endDay: 120 },
        { id: 5, title: "5. Çağ: Murabit Nöbeti", startDay: 121, endDay: 150 },
        { id: 6, title: "6. Çağ: Seher Buluşması", startDay: 151, endDay: 180 }
    ];

    // --- HARİTA BÖLGELERİ ---
    const mapZones = [
        { tag: "Bölge 1 • Osmanlı Surları (1537)", name: "Şam Kapısı (Babü'l-Amud)", desc: "Kanuni Sultan Süleyman'ın inşa ettirdiği en görkemli sur kapısı. Kudüs'ün kalbine açılan ana giriş." },
        { tag: "Bölge 2 • Kudüs Kuzey Hattı", name: "Şeyh Cerrah Mahallesi", desc: "Osmanlı vakıf arazileri ve tarihi evleriyle Kudüs'ün hukuki direniş hattı." },
        { tag: "Bölge 3 • Güney Surları", name: "Meğaribe Vakfı & Burak Duvarı", desc: "Salahaddin Eyyubi vakfı olan ve asırlardır İslam hafızasında yer eden kutsal mahalle." },
        { tag: "Bölge 4 • Harem-i Şerif Güney", name: "Kıble Mescidi", desc: "Hz. Ömer'den bu yana cemaatle dolup taşan, Mescid-i Aksa'nın ana ibadethane merkezi." },
        { tag: "Bölge 5 • Harem-i Şerif Kalbi", name: "Kubbetü's-Sahre & Mübarek Kaya", desc: "Miracın başladığı kutlu Muallak Taşının bulunduğu İslam Mimarisi şaheseri." }
    ];

    // --- TARİHİ FERMANLAR VE KRİZ SENARYOLARI ---
    const scenariosData = [
        {
            year: "1516",
            era: "Osmanlı Dönemi • Emanet",
            title: "Yavuz Sultan Selim'in Kudüs'e Girişi",
            story: "Osmanlı ordusu Kudüs kapılarına dayandığında, şehir anahtarları kan dökülmeden teslim alınır. Şehrin alimleri ve kadısı Sultan Selim'i 'Hâdimü'l-Haremeyn' unvanıyla karşılar. Bu tarihi kavşakta ilk kararınız ne olacaktır?",
            choices: [
                {
                    text: "Şehrin idaresini yerel vakıflara ve şeri hukuka bırak, medreseleri onar.",
                    effectText: "Doğru karar! Kudüs'ün ilmi hafızası güçlendi.",
                    rewards: { spirit: +15, lore: +20, defense: +10, days: +10 }
                },
                {
                    text: "Sadece askeri kaleleri tahkim et, iç siyasete karışma.",
                    effectText: "Savunma arttı ancak manevi bağlar zayıf kaldı.",
                    rewards: { spirit: +5, lore: +5, defense: +20, days: +5 }
                }
            ]
        },
        {
            year: "1876",
            era: "Osmanlı İdaresi • Hazine-i Hassa",
            title: "Sultan II. Abdülhamid'in Tapu Hamlesi",
            story: "Avrupalı fonların ve gayrimenkul şirketlerinin Kudüs arazilerini toplamak için diplomatik baskı yaptığı dönemde, Saray'dan özel bir ferman gelir: 'Kudüs toprakları satılamaz, Hazine-i Hassa adına tescillenecektir.'",
            choices: [
                {
                    text: "Tüm tapu kayıtlarını Osmanlı arşivlerinde muhafaza et ve mahalleleri koru.",
                    effectText: "Tarihi hafıza mühürlendi! Hukuki zırh başarıyla kuruldu.",
                    rewards: { spirit: +10, lore: +25, defense: +15, days: +15 }
                },
                {
                    text: "Sadece ticari merkezleri koruma altına al, diğer bölgeleri akışına bırak.",
                    effectText: "Eksik koruma nedeniyle bazı bölgeler savunmasız kaldı.",
                    rewards: { spirit: +0, lore: +10, defense: +5, days: +5 }
                }
            ]
        },
        {
            year: "1969",
            era: "Direniş & Sabır Dönemi",
            title: "Kıble Mescidi Yangını ve Halkın Direnişi",
            story: "Kıble Mescidi'nde çıkarılan menfur yangın sonrasında Kudüslü hanımlar, gençler ve yaşlılar su kitaleriyle, elleriyle alevlere karşı durur. Mescidi korumak için seher vakti nöbetçiler çağrılmaktadır.",
            choices: [
                {
                    text: "Hemen 'Murabit' halkaları kurarak Mescid-i Aksa'nın kapılarında nöbet tutmaya başla.",
                    effectText: "Maneviyat zirve yaptı! Halk bilinci ve direniş kalkanı kenetlendi.",
                    rewards: { spirit: +25, lore: +15, defense: +20, days: +20 }
                },
                {
                    text: "Sadece uluslararası kınama mesajları yayınla, sahaya inme.",
                    effectText: "Pasif tutum maneviyatı ve direniş gücünü zayıflattı.",
                    rewards: { spirit: -10, lore: +5, defense: -5, days: +5 }
                }
            ]
        },
        {
            year: "2021",
            era: "Şeyh Cerrah Nöbeti",
            title: "Mahallelerin Tahliye Tehdidi ve Hukuki Mücadele",
            story: "Şeyh Cerrah mahallesindeki aileler evlerinden çıkarılmakla yüzyüzedir. Dünyanın dört bir yanından gelen aktivistler ve yerel halk ortak ses yükseltir.",
            choices: [
                {
                    text: "Osmanlı tapu belgelerini uluslararası mahkemelere ve basına taşı.",
                    effectText: "Hafıza kaynağı katlanarak arttı, adalet sesi duyuruldu.",
                    rewards: { spirit: +15, lore: +30, defense: +25, days: +20 }
                },
                {
                    text: "Sadece bireysel taşınma yardımı teklif et.",
                    effectText: "Mahalle direnişi zayıfladı.",
                    rewards: { spirit: -5, lore: +5, defense: -10, days: +5 }
                }
            ]
        },
        {
            year: "2026",
            era: "180. Gün • Seher Buluşması",
            title: "Kudüs Seferinin Zirvesi ve Özgürlük Ufku",
            story: "180 günlük tarih, ilim, strateji ve maneviyat seferinin son günündesin. Mescid-i Aksa'nın avlusunda ezan sesleri yankılanırken son iradeyi ortaya koyma vakti.",
            choices: [
                {
                    text: "Seher vaktinde tüm muhafızlarla birlikte Aksa avlusunda saf tut ve beratını al.",
                    effectText: "Elhamdülillah! Kudüs Seferi başarıyla tamamlandı.",
                    rewards: { spirit: +30, lore: +30, defense: +30, days: +30 }
                }
            ]
        }
    ];

    // --- KUDÜS ARŞİVİ (BELGELER) ---
    const archiveTerms = [
        { title: "Nâdiyü'l-Mescid (Mescid Halkası)", desc: "Mescid-i Aksa'nın ilim, irfan ve Kur'an halkalarıyla sürekli diri tutulması geleneği." },
        { title: "Hazine-i Hassa Tapuları", desc: "Sultan II. Abdülhamid Han'ın Kudüs topraklarını şahsi mülkiyetine alarak tapu devirlerini engellediği tarihi koruma kalkanı." },
        { title: "Eyyubi Vakfiyesi", desc: "Salahaddin Eyyubi'nin Kudüs'ü fethinden sonra kurduğu ve mahalleleri mukaddes kılan vakıf sitemi." },
        { title: "Murabitun / Murabitat", desc: "Mescid-i Aksa'yı nöbetleşe koruyan, ilim ve ibadetle makamı muhafaza eden gönüllüler topluluğu." }
    ];

    const namingComparisons = [
        { wrong: "Haremü'l-Hakim / Tapınak Dağı", correct: "Harem-i Şerif & Mescid-i Aksa (144 dönümlük mukaddes mabed kompleksi)" },
        { wrong: "Doğu Kudüs", correct: "Kudüs-ü Şerif (Tarihi Surlar İçi ve İslam Mirasının Kalbi)" },
        { wrong: "Ağlama Duvarı", correct: "Burak Duvarı (Hz. Muhammed'in Miraç gecesi Burak'ı bağladığı meşânik duvarı)" }
    ];

    // --- TONE.JS SES MOTORU ---
    let synth, ambientLoop;
    function initAudio() {
        if (!synth) {
            synth = new Tone.Synth({
                oscillator: { type: "sine" },
                envelope: { attack: 0.8, decay: 1.2, sustain: 0.4, release: 2.5 }
            }).toDestination();
        }
    }

    function toggleAmbientSound() {
        initAudio();
        const btn = document.getElementById("sound-toggle-btn");
        if (!state.soundPlaying) {
            Tone.start();
            state.soundPlaying = true;
            btn.innerText = "🔇 Sesi Kapat";
            btn.classList.replace("bg-white/10", "bg-amber-500/30");
            btn.classList.add("border-amber-400");
            
            // Huzurlu Seher Melodisi (Nihavend / Huzur makamı frekansları)
            const notes = ["C4", "E4", "G4", "B4", "C5", "G4", "E4"];
            let index = 0;
            ambientLoop = new Tone.Loop(time => {
                synth.triggerAttackRelease(notes[index], "2n", time);
                index = (index + 1) % notes.length;
            }, "2n").start(0);
            
            Tone.Transport.start();
            showToast("✨ Seher vakti manevi atmosfer sesi başlatıldı.", "success");
        } else {
            state.soundPlaying = false;
            Tone.Transport.stop();
            if (ambientLoop) ambientLoop.stop();
            btn.innerText = "🔊 Seher Atmosferini Başlat";
            btn.classList.replace("bg-amber-500/30", "bg-white/10");
            btn.classList.remove("border-amber-400");
            showToast("Ses kapatıldı.", "info");
        }
    }

    // --- OYUN FONKSİYONLARI ---
    function showToast(message, type = "success") {
        const container = document.getElementById("toast-container");
        const toast = document.createElement("div");
        const bgColor = type === "success" ? "bg-emerald-900/90 border-emerald-500/60 text-emerald-200" : "bg-amber-900/90 border-amber-500/60 text-amber-200";
        toast.className = `px-4 py-2.5 rounded-xl border ${bgColor} text-xs font-bold shadow-2xl backdrop-blur-md transition-all duration-300 translate-y-2 opacity-0`;
        toast.innerText = message;
        container.appendChild(toast);
        
        setTimeout(() => { toast.classList.remove("translate-y-2", "opacity-0"); }, 50);
        setTimeout(() => {
            toast.classList.add("translate-y-2", "opacity-0");
            setTimeout(() => toast.remove(), 300);
        }, 3500);
    }

    function updateHUD() {
        document.getElementById("stat-spirit").innerText = state.spirit;
        document.getElementById("stat-lore").innerText = state.lore;
        document.getElementById("stat-defense").innerText = state.defense;
        
        const pct = Math.min(100, Math.floor((state.currentDay / state.maxDays) * 100));
        document.getElementById("header-progress-text").innerText = `Gün ${state.currentDay} / ${state.maxDays} (%${pct})`;
        
        // Sezon / Çağ Belirleme
        let currentSeasonObj = seasonsData.find(s => state.currentDay >= s.startDay && state.currentDay <= s.endDay) || seasonsData[5];
        state.currentSeason = currentSeasonObj.id;
        document.getElementById("header-season-label").innerText = currentSeasonObj.title;

        // Rütbe Güncelleme
        let rankBadge = document.getElementById("user-rank-badge");
        if (state.currentDay < 30) rankBadge.innerText = "Aksa Talebesi";
        else if (state.currentDay < 60) rankBadge.innerText = "Eyyubi Nöbetçisi";
        else if (state.currentDay < 90) rankBadge.innerText = "Osmanlı Muhafızı";
        else if (state.currentDay < 120) rankBadge.innerText = "Hukuk Muhafızı";
        else if (state.currentDay < 150) rankBadge.innerText = "Murabit";
        else rankBadge.innerText = "Kudüs Başmuhafızı";

        renderSeasonsBar();
        renderMapZonesList();
        renderScenarioPanel();
        renderBuildingsPanel();
        renderTermsPanel();
        renderLeaderboard();

        // 180. Güne Ulaşıldıysa Otomatik Ödül Modalı
        if (state.currentDay >= 180) {
            document.getElementById("header-reward-btn").classList.remove("hidden");
        }
    }

    function renderSeasonsBar() {
        const bar = document.getElementById("seasons-bar");
        bar.innerHTML = "";
        seasonsData.forEach(season => {
            let isActive = state.currentSeason === season.id;
            let isPassed = state.currentDay > season.endDay;
            let bgClass = isActive ? "bg-amber-500 text-stone-950 font-bold border-amber-400 shadow-lg" : (isPassed ? "bg-emerald-950/70 text-emerald-300 border-emerald-600/40" : "bg-stone-900/60 text-stone-400 border-stone-800");
            
            bar.innerHTML += `
                <div class="px-3 py-1.5 rounded-xl border text-[11px] flex items-center gap-2 ${bgClass} shrink-0">
                    <span>${isActive ? '⏳' : (isPassed ? '✓' : '🔒')}</span>
                    <span>${season.title}</span>
                </div>
            `;
        });
    }

    function selectMapZone(index) {
        state.selectedZoneIndex = index;
        const zone = mapZones[index];
        document.getElementById("zone-tag").innerText = zone.tag;
        document.getElementById("zone-name").innerText = zone.name;
        document.getElementById("zone-desc").innerText = zone.desc;
        
        let defPct = state.zoneDefense[index];
        document.getElementById("zone-defense-pct").innerText = `%${defPct}`;
        document.getElementById("zone-defense-bar").style.width = `${defPct}%`;
        showToast(`${zone.name} seçildi.`, "info");
    }

    function renderMapZonesList() {
        for (let i = 0; i < 5; i++) {
            let ring = document.getElementById(`zone-ring-${i}`);
            if (ring) {
                if (state.zoneDefense[i] >= 80) ring.setAttribute("stroke", "#34d399");
                else if (state.zoneDefense[i] >= 40) ring.setAttribute("stroke", "#fbbf24");
                else ring.setAttribute("stroke", "#f87171");
            }
        }
        document.getElementById("conquered-zones-badge").innerText = `${state.zoneDefense.filter(d => d >= 80).length} / 5 Bölge`;
    }

    function fortifySelectedZone() {
        if (state.defense < 10) {
            showToast("Yetersiz Direniş Kaynağı! Arşiv belgelerini inceleyerek hafıza ve direniş topla.", "error");
            return;
        }
        state.defense -= 10;
        state.zoneDefense[state.selectedZoneIndex] = Math.min(100, state.zoneDefense[state.selectedZoneIndex] + 25);
        state.currentDay = Math.min(180, state.currentDay + 10);
        showToast(`${mapZones[state.selectedZoneIndex].name} tahkim edildi! (+10 Gün)`, "success");
        updateHUD();
    }

    function deployZoneMission() {
        switchTab('scenario');
        showToast("İlgili bölge ferman görevi açıldı.", "success");
    }

    function switchTab(tabName) {
        ['scenario', 'build', 'terms', 'leagues'].forEach(t => {
            document.getElementById(`panel-${t}`).classList.add('hidden');
            document.getElementById(`tab-${t}`).className = "py-2.5 px-2 rounded-xl text-xs font-semibold text-stone-400 hover:text-amber-200 transition cursor-pointer";
        });
        document.getElementById(`panel-${tabName}`).classList.remove('hidden');
        document.getElementById(`tab-${tabName}`).className = "py-2.5 px-2 rounded-xl text-xs font-bold bg-gradient-to-r from-amber-500 to-amber-600 text-stone-950 shadow transition cursor-pointer";
    }

    function renderScenarioPanel() {
        let scIndex = state.currentScenarioIndex;
        if (scIndex >= scenariosData.length) scIndex = scenariosData.length - 1;
        let sc = scenariosData[scIndex];

        document.getElementById("scenario-year-badge").innerText = sc.year;
        document.getElementById("scenario-era").innerText = sc.era;
        document.getElementById("scenario-title").innerText = sc.title;
        document.getElementById("scenario-story").innerText = sc.story;
        document.getElementById("scenario-counter").innerText = `Görev ${scIndex + 1} / ${scenariosData.length}`;

        let choicesContainer = document.getElementById("scenario-choices");
        choicesContainer.innerHTML = "";
        sc.choices.forEach((choice, idx) => {
            choicesContainer.innerHTML += `
                <button onclick="handleChoice(${scIndex}, ${idx})" class="w-full text-left p-3.5 rounded-xl parchment-box hover:border-amber-400 text-xs text-stone-200 transition cursor-pointer flex items-center justify-between gap-3 group">
                    <span><strong>${idx + 1}. Seçenek:</strong> ${choice.text}</span>
                    <span class="text-amber-400 shrink-0 group-hover:translate-x-1 transition">➔</span>
                </button>
            `;
        });
        document.getElementById("scenario-outcome").classList.add("hidden");
    }

    function handleChoice(scIndex, choiceIdx) {
        let sc = scenariosData[scIndex];
        let choice = sc.choices[choiceIdx];

        state.spirit += choice.rewards.spirit;
        state.lore += choice.rewards.lore;
        state.defense += choice.rewards.defense;
        state.currentDay = Math.min(180, state.currentDay + choice.rewards.days);

        let outcomeBox = document.getElementById("scenario-outcome");
        outcomeBox.className = "mt-5 p-4 rounded-xl border text-xs leading-relaxed bg-emerald-950/40 border-emerald-500/40 text-emerald-200";
        outcomeBox.innerHTML = `<strong>Tarihsel Netice:</strong> ${choice.effectText} <br><span class="text-amber-300 mt-1 block">✨ Kaynaklar güncellendi (+ Maneviyat, + Hafıza, + Direniş, +${choice.rewards.days} Gün Sefer).</span>`;
        outcomeBox.classList.remove("hidden");

        setTimeout(() => {
            if (state.currentScenarioIndex < scenariosData.length - 1) {
                state.currentScenarioIndex++;
                updateHUD();
            } else {
                showToast("Tüm tarihi ferman görevleri tamamlandı! Seher vaktine hazırsın.", "success");
            }
        }, 3000);
    }

    function renderBuildingsPanel() {
        let container = document.getElementById("buildings-container");
        container.innerHTML = "";
        let builtCount = state.builtStructures.length;
        document.getElementById("built-count-badge").innerText = `${builtCount} / ${structuresData.length} Vakıf Kuruldu`;

        structuresData.forEach(b => {
            let isBuilt = state.builtStructures.includes(b.id);
            container.innerHTML += `
                <div class="p-4 rounded-xl parchment-box flex flex-col justify-between gap-3">
                    <div>
                        <div class="text-[10px] uppercase font-bold text-amber-400">${b.era}</div>
                        <h3 class="text-xs font-bold text-white mt-0.5">${b.name}</h3>
                        <p class="text-[11px] text-stone-300 mt-1 leading-relaxed">${b.desc}</p>
                    </div>
                    <div class="border-t border-stone-800 pt-2.5 flex items-center justify-between gap-2">
                        <div class="text-[10px] text-stone-400">
                            Maliyet: ${b.cost.spirit > 0 ? b.cost.spirit + ' 🕌 ' : ''} ${b.cost.lore > 0 ? b.cost.lore + ' 📜 ' : ''} ${b.cost.defense > 0 ? b.cost.defense + ' 🛡️' : 'Ücretsiz'}
                        </div>
                        ${isBuilt ? 
                            '<span class="px-3 py-1 rounded-lg bg-emerald-950 text-emerald-300 text-[11px] font-bold border border-emerald-500/30">Kuruldu ✓</span>' : 
                            `<button onclick="buildStructure('${b.id}', ${b.rewardDays}, ${b.cost.spirit}, ${b.cost.lore}, ${b.cost.defense})" class="px-3 py-1.5 rounded-xl bg-amber-500 hover:bg-amber-400 text-stone-950 text-[11px] font-bold transition cursor-pointer">İnşa Et</button>`
                        }
                    </div>
                </div>
            `;
        });
    }

    function buildStructure(id, rewardDays, reqSpirit, reqLore, reqDefense) {
        if (state.spirit < reqSpirit || state.lore < reqLore || state.defense < reqDefense) {
            showToast("Yetersiz kaynak! Arşiv belgelerini oku veya ferman kararları ver.", "error");
            return;
        }
        state.spirit -= reqSpirit;
        state.lore -= reqLore;
        state.defense -= reqDefense;
        state.currentDay = Math.min(180, state.currentDay + rewardDays);
        state.builtStructures.push(id);
        showToast("Vakıf başarıyla inşa edildi ve ihya edildi!", "success");
        updateHUD();
    }

    function renderTermsPanel() {
        let list = document.getElementById("terms-list");
        list.innerHTML = "";
        archiveTerms.forEach((term, idx) => {
            let isRead = state.readTerms.includes(idx);
            list.innerHTML += `
                <div onclick="readTerm(${idx})" class="p-3.5 rounded-xl parchment-box cursor-pointer hover:border-amber-400/60 transition flex items-center justify-between gap-3">
                    <div>
                        <h4 class="text-xs font-bold text-amber-300">${term.title}</h4>
                        <p class="text-[11px] text-stone-300 mt-0.5">${term.desc}</p>
                    </div>
                    <span class="text-xs font-bold shrink-0 ${isRead ? 'text-emerald-400' : 'text-amber-400'}">${isRead ? 'Okundu ✓' : '+15 Hafıza ➔'}</span>
                </div>
            `;
        });

        let namingList = document.getElementById("naming-comparison-list");
        namingList.innerHTML = "";
        namingComparisons.forEach(item => {
            namingList.innerHTML += `
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-2 text-[11px] p-3 rounded-xl bg-black/40 border border-stone-800">
                    <div class="text-red-400">❌ <strong>İşgal / Yanlış Dil:</strong> ${item.wrong}</div>
                    <div class="text-emerald-300">✅ <strong>Kudüs Hakikati:</strong> ${item.correct}</div>
                </div>
            `;
        });
    }

    function readTerm(idx) {
        if (!state.readTerms.includes(idx)) {
            state.readTerms.push(idx);
            state.lore += 15;
            state.currentDay = Math.min(180, state.currentDay + 5);
            showToast("Arşiv belgesi incelendi (+15 Hafıza, +5 Gün).", "success");
            updateHUD();
        }
    }

    function changeGuild(val) {
        state.userGuild = val;
        document.getElementById("selected-guild-name").innerText = val;
        showToast(`Muhafız Sancağın '${val}' olarak güncellendi.`, "success");
    }

    function renderLeaderboard() {
        const guilds = [
            { name: "Hıttin Muhafız Birliği", days: Math.min(180, state.currentDay + 15), members: "1.420 Muhafız" },
            { name: "Şam Kapısı Nöbetçileri", days: Math.min(180, state.currentDay + 10), members: "1.280 Muhafız" },
            { name: "Zeytin Dağı Sancağı", days: state.currentDay, members: "950 Muhafız" },
            { name: "Babü'r-Rahme Halkası", days: Math.max(1, state.currentDay - 10), members: "820 Muhafız" }
        ];

        let list = document.getElementById("leaderboard-list");
        list.innerHTML = "";
        guilds.forEach((g, i) => {
            let isUser = g.name === state.userGuild;
            list.innerHTML += `
                <div class="p-3 rounded-xl parchment-box flex items-center justify-between gap-3 ${isUser ? 'border-amber-400 bg-amber-950/20' : ''}">
                    <div class="flex items-center gap-3">
                        <span class="font-bold text-amber-400 text-xs">#${i + 1}</span>
                        <div>
                            <div class="text-xs font-bold text-white">${g.name} ${isUser ? '(Senin Sancağın)' : ''}</div>
                            <div class="text-[10px] text-stone-400">${g.members}</div>
                        </div>
                    </div>
                    <div class="text-right">
                        <div class="text-xs font-bold text-emerald-400">Gün ${g.days} / 180</div>
                        <div class="text-[10px] text-stone-400">Ortak İlerleme</div>
                    </div>
                </div>
            `;
        });
    }

    function openRewardModal() {
        document.getElementById("reward-modal").classList.remove("hidden");
        document.getElementById("reward-modal").classList.add("flex");
        showToast("✨ Mescid-i Aksa Seher Buluşması simülasyonu açıldı.", "success");
    }

    function closeRewardModal() {
        document.getElementById("reward-modal").classList.remove("flex");
        document.getElementById("reward-modal").classList.add("hidden");
    }

    function downloadCertificate() {
        showToast("📜 Kudüs Muhafızı Beratınız başarıyla indirildi!", "success");
    }

    // İlk yükleme
    window.onload = function() {
        updateHUD();
    };
</script>
