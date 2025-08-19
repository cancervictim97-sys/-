import { useState } from "react";

export default function App() {
  const [email, setEmail] = useState("");

  const handleSubmit = (e) => {
    e.preventDefault();
    alert(`Thanks for signing up, ${email}!`);
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-indigo-50 to-white text-gray-800">
      {/* Hero Section */}
      <header className="text-center py-20">
        <h1 className="text-4xl md:text-6xl font-bold mb-4">
          AI Social Translator
        </h1>
        <p className="text-lg md:text-xl text-gray-600 max-w-2xl mx-auto">
          Connect with people worldwide. Real-time translation for dating &
          social apps. Break language barriers instantly.
        </p>
      </header>

      {/* How it works */}
      <section className="max-w-4xl mx-auto px-6 py-10">
        <h2 className="text-2xl font-semibold mb-6 text-center">
          How it Works
        </h2>
        <div className="grid md:grid-cols-3 gap-6">
          <div className="p-6 rounded-2xl shadow bg-white">
            <h3 className="font-semibold mb-2">1. Paste or Connect</h3>
            <p className="text-gray-600">Copy chat text or link your app.</p>
          </div>
          <div className="p-6 rounded-2xl shadow bg-white">
            <h3 className="font-semibold mb-2">2. Instant Translate</h3>
            <p className="text-gray-600">
              AI translates in real-time with context.
            </p>
          </div>
          <div className="p-6 rounded-2xl shadow bg-white">
            <h3 className="font-semibold mb-2">3. Reply Smoothly</h3>
            <p className="text-gray-600">
              Get natural, flirty, or casual responses instantly.
            </p>
          </div>
        </div>
      </section>

      {/* Features */}
      <section className="bg-indigo-50 py-16 px-6">
        <h2 className="text-2xl font-semibold text-center mb-10">Features</h2>
        <div className="grid md:grid-cols-2 gap-8 max-w-5xl mx-auto">
          <div className="p-6 rounded-2xl shadow bg-white">
            🌍 Multilingual support
          </div>
          <div className="p-6 rounded-2xl shadow bg-white">
            💬 Natural conversation tone
          </div>
          <div className="p-6 rounded-2xl shadow bg-white">
            🔒 Privacy-friendly
          </div>
          <div className="p-6 rounded-2xl shadow bg-white">
            ⚡ Super fast responses
          </div>
        </div>
      </section>

      {/* Call to Action */}
      <section className="py-16 text-center px-6">
        <h2 className="text-2xl md:text-3xl font-bold mb-4">
          Be the first to try it!
        </h2>
        <p className="text-gray-600 mb-6">
          Sign up to get early access when we launch.
        </p>
        <form
          onSubmit={handleSubmit}
          className="flex flex-col sm:flex-row items-center justify-center gap-4 max-w-lg mx-auto"
        >
          <input
            type="email"
            required
            placeholder="Enter your email"
            className="w-full sm:flex-1 px-4 py-3 rounded-xl border focus:outline-none focus:ring-2 focus:ring-indigo-400"
            value={email}
            onChange={(e) => setEmail(e.target.value)}
          />
          <button
            type="submit"
            className="px-6 py-3 rounded-xl bg-indigo-600 text-white font-semibold hover:bg-indigo-700"
          >
            Join Waitlist
          </button>
        </form>
      </section>
    </div>
  );
}
