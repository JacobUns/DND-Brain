<%*
const malePrefixes = ["Ae", "Alar", "Cael", "Elen", "Faer", "Galan", "Ilar", "Laer", "Myr", "Naer", "Olor", "Pael", "Quel", "Rael", "Sael", "Thael", "Vael", "Wyn", "Yll", "Zae"];
const maleSuffixes = ["ion", "thir", "ionel", "aros", "amir", "eth", "ionis", "ionan", "andir", "hael", "mir", "anis", "oril", "ien", "thoril", "vorin", "eren", "las", "nor", "andor"];

const femalePrefixes = ["Aela", "Alae", "Caeri", "Elira", "Faele", "Galas", "Ilia", "Lirae", "Myrae", "Naela", "Orae", "Paera", "Quaela", "Rhae", "Saela", "Thalia", "Vaena", "Wylira", "Ysira", "Zirae"];
const femaleSuffixes = ["riel", "wyn", "iel", "thien", "annis", "ael", "lara", "enya", "isyl", "ethys", "vanna", "lyn", "sera", "elune", "indra", "ira", "lith", "thaea", "mera", "iel"];

const surnamePrefixes = ["Moon", "Star", "Silver", "Wind", "Night", "Dawn", "Mist", "Sun", "Willow", "Thalor", "Lune", "Fael", "Eth", "Aether", "Autumn", "Vel", "Shael", "Quel", "Glimmer", "Tir"];
const surnameSuffixes = ["whisper", "bloom", "shade", "dancer", "gleam", "watcher", "weaver", "song", "branch", "ien", "vale", "syl", "mir", "breeze", "shroud", "lithar", "wynne", "varin", "leaf", "dorei"];

function pick(list) {
  return list[Math.floor(Math.random() * list.length)];
}

const gender = tp.user.prompt("Choose gender: male or female", "male");
let firstName = "";

if (gender.toLowerCase() === "female") {
  firstName = pick(femalePrefixes) + pick(femaleSuffixes);
} else {
  firstName = pick(malePrefixes) + pick(maleSuffixes);
}

const surname = pick(surnamePrefixes) + pick(surnameSuffixes);

tR += `**Name:** ${firstName} ${surname}`
%>
