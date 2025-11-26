import { Code2, Sparkles, Users, Rocket } from "lucide-react";
import TeamMember from "@/components/TeamMember";
import { Card } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import heroBg from "@/assets/hero-bg.jpg";
import arkoProfile from "@/assets/arko-profile.png";

const Index = () => {
  const teamMembers = [
    { name: "Arko Ahsan", id: "2221858", profileLink: "/profile", image: arkoProfile },
    { name: "Israt Jahan", id: "2230968" },
    { name: "Md Ibrahim Khan", id: "2330982" },
    { name: "Israt Jahan Antu", id: "2110694" },
    { name: "Ahsanul Haque Mahi", id: "2321373" },
  ];

  return (
    <div className="min-h-screen bg-background">
      {/* Hero Section */}
      <section 
        className="relative min-h-screen flex items-center justify-center overflow-hidden"
        style={{
          backgroundImage: `url(${heroBg})`,
          backgroundSize: 'cover',
          backgroundPosition: 'center',
        }}
      >
        {/* Overlay */}
        <div className="absolute inset-0 bg-background/80 backdrop-blur-sm" />
        
        {/* Content */}
        <div className="relative z-10 container mx-auto px-4 text-center space-y-8 animate-in fade-in duration-1000">
          <div className="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-primary/10 border border-primary/20 text-primary mb-4">
            <Code2 className="w-5 h-5" />
            <span className="text-sm font-medium">Tech Innovation Team</span>
          </div>
          
          <h1 className="text-6xl md:text-8xl font-bold bg-gradient-primary bg-clip-text text-transparent animate-in slide-in-from-bottom duration-1000 delay-150">
            Quantum Crew
          </h1>
          
          <p className="text-2xl md:text-3xl text-foreground/90 font-light max-w-3xl mx-auto animate-in slide-in-from-bottom duration-1000 delay-300">
            Infinite Code, Infinite Possibilities
          </p>
          
          <div className="flex items-center justify-center gap-4 pt-8 animate-in slide-in-from-bottom duration-1000 delay-500">
            <Button size="lg" className="bg-gradient-primary hover:shadow-glow-cyan transition-all duration-300">
              <Sparkles className="mr-2 h-5 w-5" />
              Explore Our Work
            </Button>
          </div>
        </div>
        
        {/* Scroll indicator */}
        <div className="absolute bottom-8 left-1/2 -translate-x-1/2 animate-bounce">
          <div className="w-6 h-10 border-2 border-primary rounded-full flex justify-center">
            <div className="w-1 h-3 bg-primary rounded-full mt-2 animate-pulse" />
          </div>
        </div>
      </section>

      {/* About Section */}
      <section className="py-24 px-4 bg-gradient-hero">
        <div className="container mx-auto max-w-4xl">
          <div className="text-center space-y-6 animate-in fade-in duration-1000">
            <div className="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-primary/10 border border-primary/20 text-primary mb-4">
              <Users className="w-5 h-5" />
              <span className="text-sm font-medium">About Us</span>
            </div>
            
            <h2 className="text-4xl md:text-5xl font-bold text-foreground">
              Who We Are
            </h2>
            
            <p className="text-lg text-muted-foreground leading-relaxed">
              Quantum Crew is a dynamic team of innovative developers and tech enthusiasts 
              pushing the boundaries of what's possible with code. We believe in the power 
              of collaboration, continuous learning, and creating solutions that make a 
              real-world impact. Our motto, "Infinite Code, Infinite Possibilities," 
              reflects our commitment to exploring new technologies and building the future.
            </p>
          </div>
        </div>
      </section>

      {/* Team Section */}
      <section className="py-24 px-4 bg-background">
        <div className="container mx-auto">
          <div className="text-center space-y-6 mb-16">
            <div className="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-primary/10 border border-primary/20 text-primary mb-4">
              <Users className="w-5 h-5" />
              <span className="text-sm font-medium">Our Team</span>
            </div>
            
            <h2 className="text-4xl md:text-5xl font-bold text-foreground">
              Meet the Crew
            </h2>
            
            <p className="text-lg text-muted-foreground max-w-2xl mx-auto">
              A talented group of individuals united by passion for technology and innovation
            </p>
          </div>
          
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 max-w-5xl mx-auto">
            {teamMembers.map((member, index) => (
              <TeamMember
                key={member.id}
                name={member.name}
                id={member.id}
                profileLink={member.profileLink}
                image={member.image}
                index={index}
              />
            ))}
          </div>
        </div>
      </section>

      {/* Project Section */}
      <section className="py-24 px-4 bg-gradient-hero">
        <div className="container mx-auto max-w-5xl">
          <div className="text-center space-y-6 mb-16">
            <div className="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-primary/10 border border-primary/20 text-primary mb-4">
              <Rocket className="w-5 h-5" />
              <span className="text-sm font-medium">Featured Project</span>
            </div>
            
            <h2 className="text-4xl md:text-5xl font-bold text-foreground">
              NEXUS
            </h2>
            
            <p className="text-xl text-primary font-medium">
              Smart City Dashboard Platform
            </p>
          </div>
          
          <Card className="overflow-hidden bg-card border-border hover:border-primary transition-all duration-500 hover:shadow-glow-cyan">
            <div className="p-8 md:p-12 space-y-6">
              <div className="space-y-4">
                <h3 className="text-2xl font-semibold text-foreground">
                  Real-time Urban Intelligence
                </h3>
                
                <p className="text-muted-foreground leading-relaxed">
                  NEXUS is a comprehensive real-time smart city dashboard that brings together 
                  critical urban data into one powerful platform. With live monitoring capabilities 
                  and intelligent analytics, cities can make data-driven decisions faster than ever.
                </p>
              </div>
              
              <div className="grid md:grid-cols-2 gap-6 pt-4">
                <div className="space-y-3">
                  <h4 className="text-lg font-semibold text-primary">Core Features</h4>
                  <ul className="space-y-2 text-muted-foreground">
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Live traffic monitoring & optimization</span>
                    </li>
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Energy consumption analytics</span>
                    </li>
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Waste management tracking</span>
                    </li>
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Public safety monitoring</span>
                    </li>
                  </ul>
                </div>
                
                <div className="space-y-3">
                  <h4 className="text-lg font-semibold text-primary">Technical Highlights</h4>
                  <ul className="space-y-2 text-muted-foreground">
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Interactive maps with real-time data</span>
                    </li>
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Emergency alert system</span>
                    </li>
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Role-based access control</span>
                    </li>
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Dark/Light mode support</span>
                    </li>
                    <li className="flex items-start gap-2">
                      <span className="text-primary mt-1">•</span>
                      <span>Fully mobile optimized</span>
                    </li>
                  </ul>
                </div>
              </div>
              
              <div className="pt-6 border-t border-border">
                <p className="text-sm text-muted-foreground italic">
                  Built with cutting-edge web technologies to ensure scalability, 
                  performance, and an exceptional user experience.
                </p>
              </div>
            </div>
          </Card>
        </div>
      </section>

      {/* Footer */}
      <footer className="py-12 px-4 bg-background border-t border-border">
        <div className="container mx-auto text-center space-y-4">
          <div className="flex items-center justify-center gap-2">
            <Code2 className="w-6 h-6 text-primary" />
            <span className="text-xl font-bold text-foreground">Quantum Crew</span>
          </div>
          <p className="text-muted-foreground">
            Infinite Code, Infinite Possibilities
          </p>
          <p className="text-sm text-muted-foreground/60">
            © 2024 Quantum Crew. All rights reserved.
          </p>
        </div>
      </footer>
    </div>
  );
};

export default Index;
