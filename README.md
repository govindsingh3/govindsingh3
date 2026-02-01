import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

export default function MatrixPortfolio() {
  return (
    <div className="min-h-screen bg-black text-green-400 font-mono">
      {/* Header */}
      <header className="text-center py-16 border-b border-green-500">
        <motion.h1
          initial={{ opacity: 0, y: -40 }}
          animate={{ opacity: 1, y: 0 }}
          transition={{ duration: 0.8 }}
          className="text-5xl font-bold tracking-widest"
        >
          GOVIND PRATAP SINGH
        </motion.h1>
        <p className="mt-4 text-green-300">
          Full Stack Developer | MERN | Java | Backend Systems
        </p>
      </header>

      {/* About */}
      <section className="max-w-5xl mx-auto px-6 py-16">
        <h2 className="text-3xl mb-6 border-b border-green-500 pb-2">
          &gt; About_Me
        </h2>
        <p className="text-green-300 leading-relaxed">
          Passionate Full Stack Developer experienced in building scalable web
          applications using MERN stack and Java backend systems. Strong
          foundation in Data Structures, OOP, and performance optimized backend
          architecture.
        </p>
      </section>

      {/* Skills */}
      <section className="max-w-6xl mx-auto px-6 py-16">
        <h2 className="text-3xl mb-10 border-b border-green-500 pb-2">
          &gt; Skill_Matrix
        </h2>
        <div className="grid md:grid-cols-4 gap-6">
          {[
            {
              title: "Languages",
              items: ["Java", "JavaScript"],
            },
            {
              title: "Frontend",
              items: ["React", "HTML", "CSS"],
            },
            {
              title: "Backend",
              items: ["Node.js", "Express.js"],
            },
            {
              title: "Database",
              items: ["MongoDB", "MySQL"],
            },
          ].map((skill, index) => (
            <Card
              key={index}
              className="bg-black border border-green-500 shadow-xl"
            >
              <CardContent className="p-6">
                <h3 className="text-xl mb-4 text-green-300">
                  {skill.title}
                </h3>
                <ul className="space-y-2">
                  {skill.items.map((item, i) => (
                    <li key={i}>&gt; {item}</li>
                  ))}
                </ul>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Projects */}
      <section className="max-w-6xl mx-auto px-6 py-16">
        <h2 className="text-3xl mb-10 border-b border-green-500 pb-2">
          &gt; Project_Database
        </h2>

        <div className="grid md:grid-cols-3 gap-8">
          {[
            {
              name: "React Studio IDE",
              desc: "Browser based React IDE with Sandpack and real-time execution",
            },
            {
              name: "Luxe Stay Booking",
              desc: "MERN hotel booking platform with admin dashboard",
            },
            {
              name: "Library Management",
              desc: "Java OOP system with file persistence and menu interface",
            },
          ].map((project, index) => (
            <Card
              key={index}
              className="bg-black border border-green-500 hover:shadow-green-500/50 transition"
            >
              <CardContent className="p-6">
                <h3 className="text-xl mb-3 text-green-300">
                  {project.name}
                </h3>
                <p className="text-green-400 text-sm">{project.desc}</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Contact */}
      <section className="text-center py-16 border-t border-green-500">
        <h2 className="text-3xl mb-6">&gt; Connect_With_Me</h2>
        <div className="flex justify-center gap-6 flex-wrap">
          <Button className="bg-green-500 text-black hover:bg-green-400">
            LinkedIn
          </Button>
          <Button className="bg-green-500 text-black hover:bg-green-400">
            GitHub
          </Button>
          <Button className="bg-green-500 text-black hover:bg-green-400">
            Email
          </Button>
        </div>
      </section>

      {/* Footer */}
      <footer className="text-center py-8 text-green-600 text-sm">
        SYSTEM STATUS: CONNECTED TO MATRIX
      </footer>
    </div>
  );
}
