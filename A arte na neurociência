import React, { useState, useEffect } from 'react';
import { 
  Palette, 
  Brain, 
  MessageSquare, 
  Lightbulb, 
  ChevronRight, 
  ChevronLeft, 
  Target, 
  Sparkles, 
  BookOpen,
  Image as ImageIcon,
  RefreshCw
} from 'lucide-react';

// Dados das obras com URLs de alta fidelidade e redundância
const ART_DATA = [
  {
    id: 1,
    title: "A Persistência da Memória",
    artist: "Salvador Dalí",
    image: "https://upload.wikimedia.org/wikipedia/en/d/dd/The_Persistence_of_Memory.jpg", 
    symbolism: "Relógios derretendo simbolizam a relatividade do tempo e a maleabilidade da realidade interior.",
    competence: "Autorregulação e Flexibilidade Cognitiva",
    exercise: "Identifique em quais áreas da sua vida sente que o tempo 'derrete' ou escapa do seu controle.",
    realLife: "Crie blocos de 15 minutos para tarefas que costuma procrastinar, focando no 'agora'."
  },
  {
    id: 2,
    title: "A Noite Estrelada",
    artist: "Vincent van Gogh",
    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/e/ea/Van_Gogh_-_Starry_Night_-_Google_Art_Project.jpg/1280px-Van_Gogh_-_Starry_Night_-_Google_Art_Project.jpg", 
    symbolism: "O movimento turbulento do céu e a presença do artista expressam emoções intensas e a busca por conexão.",
    competence: "Consciência Emocional e Expressão",
    exercise: "Desenhe linhas onduladas que representem o seu estado emocional atual: são calmas ou turbulentas?",
    realLife: "Durante uma conversa difícil, tente nomear a emoção exata que está a sentir antes de responder."
  },
  {
    id: 3,
    title: "Composição VIII",
    artist: "Wassily Kandinsky",
    image: "https://www.guggenheim.org/wp-content/uploads/1923/01/37.262_ph_web.jpg",
    symbolism: "Formas geométricas e cores puras organizando o caos numa estrutura lógica.",
    competence: "Atenção e Organização de Pensamento",
    exercise: "Observe as formas. Qual delas representa a sua maior prioridade hoje? Porquê?",
    realLife: "Organize a sua lista de tarefas por 'formas' (urgência/importância) para evitar a sobrecarga mental."
  }
];

const App = () => {
  const [step, setStep] = useState(0); 
  const [currentArtIndex, setCurrentArtIndex] = useState(0);
  const [methodStep, setMethodStep] = useState(0);
  const [imgError, setImgError] = useState(false);

  const currentArt = ART_DATA[currentArtIndex];

  useEffect(() => {
    setImgError(false);
  }, [currentArtIndex]);

  const methodologySteps = [
    { label: "Obra Artística", icon: <Palette className="w-6 h-6" />, content: currentArt.title, detail: `Artista: ${currentArt.artist}` },
    { label: "Interpretação Simbólica", icon: <BookOpen className="w-6 h-6" />, content: "O que isto diz?", detail: currentArt.symbolism },
    { label: "Competência Humana", icon: <Brain className="w-6 h-6" />, content: "Habilidade Relacionada", detail: currentArt.competence },
    { label: "Exercício Experiencial", icon: <Sparkles className="w-6 h-6" />, content: "Mãos à obra", detail: currentArt.exercise },
    { label: "Aplicação Real", icon: <Target className="w-6 h-6" />, content: "Mudança de Vida", detail: currentArt.realLife }
  ];

  return (
    <div className="min-h-screen bg-slate-50 text-slate-900 font-sans">
      <header className="bg-white border-b p-4 sticky top-0 z-10">
        <div className="max-w-4xl mx-auto flex justify-between items-center">
          <div className="flex items-center gap-2">
            <div className="bg-indigo-600 p-2 rounded-lg text-white">
              <Brain size={24} />
            </div>
            <h1 className="text-xl font-bold tracking-tight text-slate-800">A arte na neurociência</h1>
          </div>
          <nav className="flex gap-4">
            <button onClick={() => {setStep(0); setMethodStep(0);}} className={`text-sm font-medium transition-colors ${step === 0 ? 'text-indigo-600' : 'text-slate-500 hover:text-indigo-400'}`}>Início</button>
            <button onClick={() => {setStep(1); setMethodStep(0);}} className={`text-sm font-medium transition-colors ${step === 1 ? 'text-indigo-600' : 'text-slate-500'}`}>Metodologia</button>
          </nav>
        </div>
      </header>

      <main className="max-w-4xl mx-auto p-6">
        {step === 0 && (
          <section className="py-12 animate-in fade-in duration-700">
            <div className="text-center mb-12">
              <h2 className="text-4xl font-extrabold text-slate-800 mb-4 tracking-tight">Arte como Linguagem de Desenvolvimento Humano</h2>
              <p className="text-xl text-slate-600 max-w-2xl mx-auto">Transforme a leitura simbólica da arte em metodologia prática para o seu desenvolvimento emocional, cognitivo e comportamental.</p>
            </div>
            
            <div className="grid md:grid-cols-2 gap-8 mb-12">
              <div className="bg-white p-8 rounded-2xl shadow-sm border border-slate-100">
                <h3 className="text-lg font-bold mb-4 flex items-center gap-2"><Lightbulb className="text-amber-500" /> Proposta</h3>
                <p className="text-slate-600 leading-relaxed">
                  Metodologia prática para transformar a percepção estética em ferramentas de crescimento pessoal através dos fundamentos da neurociência aplicada.
                </p>
              </div>
              <div className="bg-white p-8 rounded-2xl shadow-sm border border-slate-100">
                <h3 className="text-lg font-bold mb-4 flex items-center gap-2"><Target className="text-indigo-500" /> Resultados Esperados</h3>
                <ul className="space-y-2 text-slate-600 text-sm">
                  <li>• Ampliação da consciência emocional</li>
                  <li>• Desenvolvimento da atenção e comunicação</li>
                  <li>• Fortalecimento da autorregulação</li>
                  <li>• Sentido pessoal e aprendizagem transformadora</li>
                </ul>
              </div>
            </div>

            <div className="flex justify-center">
              <button onClick={() => setStep(1)} className="bg-indigo-600 text-white px-8 py-4 rounded-full font-bold text-lg hover:bg-indigo-700 transition-all shadow-lg flex items-center gap-2">Iniciar Experiência <ChevronRight /></button>
            </div>
          </section>
        )}

        {step === 1 && (
          <section className="animate-in slide-in-from-bottom-4 duration-500">
            <div className="mb-8 flex justify-between items-end">
              <div>
                <span className="text-indigo-600 font-bold text-sm uppercase tracking-widest">Laboratório de Símbolos</span>
                <h2 className="text-3xl font-bold">Experiência Prática</h2>
              </div>
              <div className="flex gap-2">
                <button onClick={() => { setCurrentArtIndex((prev) => (prev > 0 ? prev - 1 : ART_DATA.length - 1)); setMethodStep(0); }} className="p-2 border rounded-full hover:bg-slate-100 transition-colors bg-white shadow-sm"><ChevronLeft /></button>
                <button onClick={() => { setCurrentArtIndex((prev) => (prev < ART_DATA.length - 1 ? prev + 1 : 0)); setMethodStep(0); }} className="p-2 border rounded-full hover:bg-slate-100 transition-colors bg-white shadow-sm"><ChevronRight /></button>
              </div>
            </div>

            <div className="grid lg:grid-cols-2 gap-8">
              <div className="space-y-4">
                <div className="aspect-[4/3] rounded-2xl overflow-hidden shadow-2xl relative group bg-slate-200 flex items-center justify-center border border-slate-100">
                  {!imgError ? (
                    <img 
                      src={currentArt.image} 
                      alt={currentArt.title} 
                      className="w-full h-full object-contain bg-black"
                      onError={() => setImgError(true)}
                    />
                  ) : (
                    <div className="flex flex-col items-center gap-4 text-slate-500 p-8 text-center bg-slate-100 w-full h-full justify-center">
                      <ImageIcon size={48} className="text-slate-300" />
                      <p className="text-xs">Falha ao carregar imagem.<br/>Tentando restaurar conexão...</p>
                      <button onClick={() => setImgError(false)} className="text-xs text-indigo-600 font-bold underline flex items-center gap-1"><RefreshCw size={12}/> Tentar novamente</button>
                    </div>
                  )}
                  <div className="absolute bottom-0 left-0 right-0 bg-gradient-to-t from-black/90 to-transparent p-6 text-white pointer-events-none">
                    <p className="text-xs uppercase tracking-widest opacity-80">Obra Atual</p>
                    <h3 className="text-2xl font-bold">{currentArt.title}</h3>
                    <p className="italic opacity-90 text-sm">{currentArt.artist}</p>
                  </div>
                </div>
                <div className="bg-indigo-50 p-4 rounded-xl border border-indigo-100 flex items-start gap-3">
                  <Lightbulb className="text-indigo-600 shrink-0 mt-0.5" size={18} />
                  <p className="text-indigo-800 text-sm leading-relaxed"><span className="font-bold">Dica:</span> Observe a obra por 30 segundos em silêncio antes de prosseguir para a análise.</p>
                </div>
              </div>

              <div className="flex flex-col gap-4">
                <div className="flex justify-between items-center px-2">
                   <h4 className="font-bold text-slate-400 uppercase text-xs tracking-wider">Metodologia</h4>
                   <span className="text-indigo-600 font-bold text-sm">{methodStep + 1} / 5</span>
                </div>
                
                <div className="flex gap-2 overflow-x-auto pb-2 scrollbar-hide">
                  {methodologySteps.map((s, idx) => (
                    <button 
                      key={idx} 
                      onClick={() => setMethodStep(idx)} 
                      className={`flex-shrink-0 w-10 h-10 rounded-full flex items-center justify-center transition-all ${
                        methodStep === idx ? 'bg-indigo-600 text-white ring-4 ring-indigo-100' : 
                        idx < methodStep ? 'bg-green-500 text-white' : 'bg-slate-200 text-slate-500 hover:bg-slate-300'
                      }`}
                    >
                      {idx < methodStep ? <Target size={16} /> : s.icon}
                    </button>
                  ))}
                </div>

                <div className="bg-white p-8 rounded-2xl shadow-xl border border-slate-100 flex-grow min-h-[350px] flex flex-col animate-in zoom-in-95 duration-300">
                  <div className="mb-6">
                    <span className="text-indigo-500 font-bold text-sm uppercase tracking-wide">{methodologySteps[methodStep].label}</span>
                    <h3 className="text-2xl font-extrabold text-slate-800 mt-1">{methodologySteps[methodStep].content}</h3>
                  </div>
                  <div className="bg-slate-50 p-6 rounded-xl border-l-4 border-indigo-500 flex-grow italic text-slate-700 text-lg leading-relaxed">
                    "{methodologySteps[methodStep].detail}"
                  </div>
                  <div className="mt-8 flex gap-3">
                    {methodStep > 0 && (
                      <button onClick={() => setMethodStep(prev => prev - 1)} className="flex-1 py-3 px-4 rounded-xl border font-bold text-slate-500 hover:bg-slate-50 transition-colors">
                        Anterior
                      </button>
                    )}
                    <button 
                      onClick={() => { 
                        if (methodStep < 4) { setMethodStep(prev => prev + 1); } 
                        else { setMethodStep(0); } 
                      }} 
                      className="flex-[2] py-3 px-4 rounded-xl bg-indigo-600 text-white font-bold hover:bg-indigo-700 transition-all shadow-md flex items-center justify-center gap-2"
                    >
                      {methodStep === 4 ? "Reiniciar Análise" : "Próximo Passo"} <ChevronRight size={18} />
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </section>
        )}
      </main>
      <footer className="mt-20 border-t bg-white py-8 text-center text-slate-400 text-xs">
        <p>© 2026 A arte na neurociência - Desenvolvimento Humano e Metodologia Prática</p>
      </footer>
    </div>
  );
};

export default App;
