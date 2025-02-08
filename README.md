import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const HAECHANSTRM = () => {
  return (
    <div className="min-h-screen bg-black flex flex-col items-center py-10">
      {/* Header */}
      <header className="text-center mb-10">
        <h1 className="text-4xl font-bold text-white">HAECHANSTRM</h1>
        <p className="text-lg text-gray-400 mt-2">Support and Stream with Love</p>
      </header>

      {/* YouTube Video */}
      <Card className="max-w-md w-full mb-10 shadow-lg">
        <CardContent>
          <div className="relative w-full h-0 pb-[56.25%]">
            <iframe
              src="https://www.youtube.com/embed/0yzxJz-hHcc"
              title="HAECHANSTRM Video"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowFullScreen
              className="absolute top-0 left-0 w-full h-full rounded-lg"
            ></iframe>
          </div>
        </CardContent>
      </Card>

      {/* Buttons */}
      <div className="flex flex-wrap gap-4">
        <button className="bg-white text-black px-6 py-3 rounded-lg shadow-md hover:bg-gray-300 transition-all">
          Streaming Guideline
        </button>
        <button className="bg-white text-black px-6 py-3 rounded-lg shadow-md hover:bg-gray-300 transition-all">
          ID Creation
        </button>
        <button className="bg-white text-black px-6 py-3 rounded-lg shadow-md hover:bg-gray-300 transition-all">
          Playlist
        </button>
      </div>

      {/* Footer */}
      <footer className="text-center mt-10 text-gray-500">
        <p>2025 HAECHANSTRM. All Rights Reserved.</p>
      </footer>
    </div>
  );
};

export default HAECHANSTRM;
