import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const HAECHANSTRM = () => {
  return (
    <div className="min-h-screen bg-gray-100 flex flex-col items-center py-10">
      {/* Header */}
      <header className="text-center mb-10">
        <h1 className="text-4xl font-bold text-gray-800">HAECHANSTRM</h1>
        <p className="text-lg text-gray-600 mt-2">NCT HAECHAN 스트리밍 음원 총공팀</p>
      </header>

      {/* YouTube Video */}
      <Card className="max-w-4xl w-full mb-10 shadow-lg">
        <CardContent>
          <div className="aspect-w-16 aspect-h-9">
            <iframe
              src="https://www.youtube.com/embed/0yzxJz-hHcc"
              title="HAECHANSTRM Video"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowFullScreen
              className="w-full h-full rounded-lg"
            ></iframe>
          </div>
        </CardContent>
      </Card>

      {/* Buttons */}
      <div className="flex flex-wrap gap-4">
        <Button className="bg-blue-500 text-white px-6 py-3 rounded-lg shadow-md hover:bg-blue-600">
          Streaming Guideline
        </Button>
        <Button className="bg-green-500 text-white px-6 py-3 rounded-lg shadow-md hover:bg-green-600">
          ID Creation
        </Button>
        <Button className="bg-purple-500 text-white px-6 py-3 rounded-lg shadow-md hover:bg-purple-600">
          Playlist
        </Button>
      </div>

      {/* Footer */}
      <footer className="text-center mt-10 text-gray-500">
        <p>2025 HAECHANSTRM. All Rights Reserved.</p>
      </footer>
    </div>
  );
};

export default HAECHANSTRM;
