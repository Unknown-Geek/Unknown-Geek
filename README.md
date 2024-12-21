import React from 'react';
import { Github, Instagram, Linkedin, Coffee, CreditCard, Code, Star, GitFork } from 'lucide-react';
import { BarChart, Bar, XAxis, YAxis, CartesianGrid, Tooltip, ResponsiveContainer } from 'recharts';

const TechBadge = ({ text }) => (
  <span className="px-3 py-1 text-sm rounded-full bg-gray-800 text-gray-200 mr-2 mb-2 inline-flex items-center hover:bg-gray-700 transition-colors">
    {text}
  </span>
);

const StatCard = ({ title, value, icon: Icon }) => (
  <div className="bg-gray-800 p-6 rounded-lg shadow-lg hover:bg-gray-700 transition-colors">
    <div className="flex items-center justify-between">
      <div>
        <h3 className="text-gray-400 text-sm">{title}</h3>
        <p className="text-2xl font-semibold text-white mt-1">{value}</p>
      </div>
      <Icon className="w-8 h-8 text-gray-500" />
    </div>
  </div>
);

const LanguageStats = () => {
  const data = [
    { name: 'Python', value: 35 },
    { name: 'JavaScript', value: 25 },
    { name: 'Java', value: 20 },
    { name: 'HTML/CSS', value: 15 },
    { name: 'Other', value: 5 },
  ];

  return (
    <ResponsiveContainer width="100%" height={200}>
      <BarChart data={data}>
        <CartesianGrid strokeDasharray="3 3" stroke="#374151" />
        <XAxis dataKey="name" stroke="#9CA3AF" />
        <YAxis stroke="#9CA3AF" />
        <Tooltip 
          contentStyle={{ backgroundColor: '#1F2937', border: 'none', borderRadius: '8px' }}
          labelStyle={{ color: '#F9FAFB' }}
        />
        <Bar dataKey="value" fill="#60A5FA" radius={[4, 4, 0, 0]} />
      </BarChart>
    </ResponsiveContainer>
  );
};

export default function ModernProfile() {
  const techCategories = {
    "Languages": ["Python", "JavaScript", "Java", "C", "HTML5", "CSS3", "Dart", "Markdown"],
    "Frameworks & Libraries": ["React", "Flutter", "Flask", "TailwindCSS", "TensorFlow", "PyTorch", "Keras"],
    "Tools & Platforms": ["Git", "Docker", "Figma", "MongoDB", "MySQL", "Google Cloud", "Azure"],
    "Design": ["UI/UX Design", "Graphic Design", "Adobe Creative Suite", "Figma", "Canva"]
  };

  return (
    <div className="max-w-4xl mx-auto p-6 space-y-8 bg-gray-900 text-white min-h-screen">
      {/* Header Section */}
      <div className="space-y-4">
        <h1 className="text-4xl font-bold bg-gradient-to-r from-blue-400 to-purple-500 text-transparent bg-clip-text">
          Shravan Pandala
        </h1>
        <p className="text-gray-400 text-lg">
          Full-Stack Developer & Creative Designer
        </p>
        
        {/* Social Links */}
        <div className="flex space-x-4">
          <a href="https://github.com/Unknown-Geek" className="text-gray-400 hover:text-white transition-colors">
            <Github className="w-6 h-6" />
          </a>
          <a href="https://linkedin.com/in/shravanpandala" className="text-gray-400 hover:text-blue-400 transition-colors">
            <Linkedin className="w-6 h-6" />
          </a>
          <a href="https://instagram.com/_.shra1._" className="text-gray-400 hover:text-pink-400 transition-colors">
            <Instagram className="w-6 h-6" />
          </a>
        </div>
      </div>

      {/* About Section */}
      <div className="bg-gray-800 rounded-xl p-6 shadow-lg">
        <h2 className="text-xl font-semibold mb-4 text-blue-400">About Me</h2>
        <p className="text-gray-300">
          I'm a versatile developer who enjoys bridging the gap between technical and creative domains. 
          With expertise in AI/ML and Web Development, coupled with a strong foundation in UI/UX and 
          Graphic Design, I bring a unique blend of skills to every project.
        </p>
      </div>

      {/* GitHub Stats Cards */}
      <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
        <StatCard title="Repositories" value="25+" icon={Code} />
        <StatCard title="Total Stars" value="100+" icon={Star} />
        <StatCard title="Total Forks" value="50+" icon={GitFork} />
      </div>

      {/* Language Stats */}
      <div className="bg-gray-800 rounded-xl p-6 shadow-lg">
        <h2 className="text-xl font-semibold mb-6 text-blue-400">Language Distribution</h2>
        <LanguageStats />
      </div>

      {/* Tech Stack Section */}
      <div className="space-y-6">
        {Object.entries(techCategories).map(([category, technologies]) => (
          <div key={category} className="bg-gray-800 rounded-xl p-6 shadow-lg">
            <h2 className="text-xl font-semibold mb-4 text-blue-400">{category}</h2>
            <div className="flex flex-wrap gap-2">
              {technologies.map(tech => (
                <TechBadge key={tech} text={tech} />
              ))}
            </div>
          </div>
        ))}
      </div>

      {/* Support Section */}
      <div className="flex justify-center space-x-4 pt-6">
        <a href="https://buymeacoffee.com/ShravanPandala" 
           className="flex items-center px-4 py-2 bg-yellow-500 text-gray-900 rounded-lg hover:bg-yellow-400 transition">
          <Coffee className="w-5 h-5 mr-2" />
          Buy me a coffee
        </a>
        <a href="https://paypal.me/MojoManiac" 
           className="flex items-center px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-500 transition">
          <CreditCard className="w-5 h-5 mr-2" />
          PayPal
        </a>
      </div>
    </div>
  );
}
## 📊 GitHub Stats:
![](https://github-readme-stats.vercel.app/api?username=Unknown-Geek&theme=dark&hide_border=false&include_all_commits=true&count_private=false)<br/>
![](https://github-readme-streak-stats.herokuapp.com/?user=Unknown-Geek&theme=dark&hide_border=false)<br/>
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Unknown-Geek&theme=dark&hide_border=false&include_all_commits=true&count_private=false&layout=compact)

### 🔝 Top Contributed Repo
![](https://github-contributor-stats.vercel.app/api?username=Unknown-Geek&limit=5&theme=dark&combine_all_yearly_contributions=true)

---
[![](https://visitcount.itsvg.in/api?id=Unknown-Geek&icon=5&color=9)](https://visitcount.itsvg.in)


  
