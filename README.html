import React, { useState, useEffect, useRef } from 'react';

// Main App component
const App = () => {
    return (
        <div className="min-h-screen bg-gradient-to-br from-blue-500 to-purple-600 flex items-center justify-center p-4 font-inter">
            <div className="bg-white bg-opacity-90 rounded-3xl shadow-2xl p-8 w-full max-w-4xl transform transition-all duration-300 hover:scale-[1.01]">
                <h1 className="text-4xl font-extrabold text-center text-gray-800 mb-10">تطبيق الوقت</h1>
                <div className="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <CurrentTime />
                    <CountdownTimer />
                    <Stopwatch />
                </div>
                {/* New component for LLM-powered time management tips */}
                <div className="mt-8">
                    <TimeManagementAssistant />
                </div>
            </div>
        </div>
    );
};

// Component for displaying the current time
const CurrentTime = () => {
    const [currentTime, setCurrentTime] = useState(new Date());

    useEffect(() => {
        const timer = setInterval(() => {
            setCurrentTime(new Date());
        }, 1000);
        // Cleanup interval on component unmount
        return () => clearInterval(timer);
    }, []);

    const formatTime = (date) => {
        const options = {
            hour: '2-digit',
            minute: '2-digit',
            second: '2-digit',
            hour12: true
        };
        return date.toLocaleTimeString('ar-EG', options); // Format time in Arabic locale
    };

    const formatDate = (date) => {
        const options = {
            weekday: 'long',
            year: 'numeric',
            month: 'long',
            day: 'numeric'
        };
        return date.toLocaleDateString('ar-EG', options); // Format date in Arabic locale
    };

    return (
        <div className="bg-gradient-to-r from-green-400 to-blue-500 text-white p-6 rounded-xl shadow-lg flex flex-col items-center justify-center text-center transform transition-transform duration-300 hover:scale-105">
            <h2 className="text-2xl font-bold mb-4">الوقت الحالي</h2>
            <p className="text-5xl font-extrabold mb-2">{formatTime(currentTime)}</p>
            <p className="text-lg">{formatDate(currentTime)}</p>
        </div>
    );
};

// Component for the countdown timer
const CountdownTimer = () => {
    const [hours, setHours] = useState(0);
    const [minutes, setMinutes] = useState(0);
    const [seconds, setSeconds] = useState(0);
    const [remainingTime, setRemainingTime] = useState(0);
    const [isRunning, setIsRunning] = useState(false);
    const timerRef = useRef(null);
    const [message, setMessage] = useState('');

    useEffect(() => {
        if (isRunning && remainingTime > 0) {
            timerRef.current = setInterval(() => {
                setRemainingTime(prevTime => prevTime - 1);
            }, 1000);
        } else if (remainingTime === 0 && isRunning) {
            setIsRunning(false);
            clearInterval(timerRef.current);
            setMessage("انتهى الوقت!");
            // Play a subtle sound or vibration if possible (not directly supported in iframe without user interaction)
        }
        // Cleanup interval on component unmount or when not running
        return () => clearInterval(timerRef.current);
    }, [isRunning, remainingTime]);

    const startTimer = () => {
        const totalSeconds = hours * 3600 + minutes * 60 + seconds;
        if (totalSeconds > 0) {
            setRemainingTime(totalSeconds);
            setIsRunning(true);
            setMessage('');
        } else {
            setMessage("الرجاء إدخال وقت صالح.");
        }
    };

    const pauseTimer = () => {
        setIsRunning(false);
        clearInterval(timerRef.current);
    };

    const resetTimer = () => {
        setIsRunning(false);
        clearInterval(timerRef.current);
        setRemainingTime(0);
        setHours(0);
        setMinutes(0);
        setSeconds(0);
        setMessage('');
    };

    const formatRemainingTime = (time) => {
        const h = Math.floor(time / 3600);
        const m = Math.floor((time % 3600) / 60);
        const s = time % 60;
        return `${String(h).padStart(2, '0')}:${String(m).padStart(2, '0')}:${String(s).padStart(2, '0')}`;
    };

    return (
        <div className="bg-gradient-to-r from-yellow-400 to-orange-500 text-white p-6 rounded-xl shadow-lg flex flex-col items-center justify-center text-center transform transition-transform duration-300 hover:scale-105">
            <h2 className="text-2xl font-bold mb-4">العد التنازلي</h2>
            <div className="flex items-center space-x-2 mb-4">
                <input
                    type="number"
                    value={hours}
                    onChange={(e) => setHours(Math.max(0, parseInt(e.target.value) || 0))}
                    className="w-20 p-2 text-center rounded-lg bg-white bg-opacity-20 text-white placeholder-white focus:outline-none focus:ring-2 focus:ring-white"
                    placeholder="ساعات"
                    min="0"
                    disabled={isRunning}
                />
                <span className="text-2xl">:</span>
                <input
                    type="number"
                    value={minutes}
                    onChange={(e) => setMinutes(Math.max(0, Math.min(59, parseInt(e.target.value) || 0)))}
                    className="w-20 p-2 text-center rounded-lg bg-white bg-opacity-20 text-white placeholder-white focus:outline-none focus:ring-2 focus:ring-white"
                    placeholder="دقائق"
                    min="0"
                    max="59"
                    disabled={isRunning}
                />
                <span className="text-2xl">:</span>
                <input
                    type="number"
                    value={seconds}
                    onChange={(e) => setSeconds(Math.max(0, Math.min(59, parseInt(e.target.value) || 0)))}
                    className="w-20 p-2 text-center rounded-lg bg-white bg-opacity-20 text-white placeholder-white focus:outline-none focus:ring-2 focus:ring-white"
                    placeholder="ثواني"
                    min="0"
                    max="59"
                    disabled={isRunning}
                />
            </div>
            <p className="text-5xl font-extrabold mb-4">{formatRemainingTime(remainingTime)}</p>
            <div className="flex space-x-4">
                {!isRunning ? (
                    <button
                        onClick={startTimer}
                        className="bg-green-600 hover:bg-green-700 text-white font-bold py-3 px-6 rounded-full shadow-lg transition-all duration-300 transform hover:scale-105"
                    >
                        بدء
                    </button>
                ) : (
                    <button
                        onClick={pauseTimer}
                        className="bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-6 rounded-full shadow-lg transition-all duration-300 transform hover:scale-105"
                    >
                        إيقاف مؤقت
                    </button>
                )}
                <button
                    onClick={resetTimer}
                    className="bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-6 rounded-full shadow-lg transition-all duration-300 transform hover:scale-105"
                >
                    إعادة تعيين
                </button>
            </div>
            {message && <p className="mt-4 text-lg font-semibold">{message}</p>}
        </div>
    );
};

// Component for the stopwatch
const Stopwatch = () => {
    const [elapsedTime, setElapsedTime] = useState(0);
    const [isRunning, setIsRunning] = useState(false);
    const [laps, setLaps] = useState([]);
    const intervalRef = useRef(null);

    useEffect(() => {
        if (isRunning) {
            intervalRef.current = setInterval(() => {
                setElapsedTime(prevTime => prevTime + 10); // Update every 10ms for smoother display
            }, 10);
        }
        // Cleanup interval on component unmount or when not running
        return () => clearInterval(intervalRef.current);
    }, [isRunning]);

    const startStopwatch = () => {
        setIsRunning(true);
    };

    const pauseStopwatch = () => {
        setIsRunning(false);
        clearInterval(intervalRef.current);
    };

    const resetStopwatch = () => {
        setIsRunning(false);
        clearInterval(intervalRef.current);
        setElapsedTime(0);
        setLaps([]);
    };

    const recordLap = () => {
        setLaps(prevLaps => [...prevLaps, elapsedTime]);
    };

    const formatTime = (time) => {
        const milliseconds = String(Math.floor((time % 1000) / 10)).padStart(2, '0');
        const totalSeconds = Math.floor(time / 1000);
        const minutes = String(Math.floor(totalSeconds / 60)).padStart(2, '0');
        const seconds = String(totalSeconds % 60).padStart(2, '0');
        return `${minutes}:${seconds}.${milliseconds}`;
    };

    return (
        <div className="bg-gradient-to-r from-purple-400 to-pink-500 text-white p-6 rounded-xl shadow-lg flex flex-col items-center justify-center text-center transform transition-transform duration-300 hover:scale-105">
            <h2 className="text-2xl font-bold mb-4">المؤقت</h2>
            <p className="text-5xl font-extrabold mb-4">{formatTime(elapsedTime)}</p>
            <div className="flex space-x-4 mb-4">
                {!isRunning ? (
                    <button
                        onClick={startStopwatch}
                        className="bg-green-600 hover:bg-green-700 text-white font-bold py-3 px-6 rounded-full shadow-lg transition-all duration-300 transform hover:scale-105"
                    >
                    بدء
                    </button>
                ) : (
                    <button
                        onClick={pauseStopwatch}
                        className="bg-blue-600 hover:bg-blue-700 text-white font-bold py-3 px-6 rounded-full shadow-lg transition-all duration-300 transform hover:scale-105"
                    >
                        إيقاف مؤقت
                    </button>
                )}
                <button
                    onClick={resetStopwatch}
                    className="bg-red-600 hover:bg-red-700 text-white font-bold py-3 px-6 rounded-full shadow-lg transition-all duration-300 transform hover:scale-105"
                >
                    إعادة تعيين
                </button>
                <button
                    onClick={recordLap}
                    disabled={!isRunning}
                    className="bg-gray-600 hover:bg-gray-700 text-white font-bold py-3 px-6 rounded-full shadow-lg transition-all duration-300 transform hover:scale-105 disabled:opacity-50 disabled:cursor-not-allowed"
                >
                    تسجيل لفة
                </button>
            </div>
            {laps.length > 0 && (
                <div className="w-full max-h-40 overflow-y-auto bg-white bg-opacity-10 rounded-lg p-3 mt-4">
                    <h3 className="text-xl font-semibold mb-2 text-white">اللفات:</h3>
                    <ul className="list-none p-0">
                        {laps.map((lap, index) => (
                            <li key={index} className="text-lg text-white mb-1">
                                لفة {index + 1}: {formatTime(lap)}
                            </li>
                        ))}
                    </ul>
                </div>
            )}
        </div>
    );
};

// New component for LLM-powered time management assistant
const TimeManagementAssistant = () => {
    const [tip, setTip] = useState('');
    const [loading, setLoading] = useState(false);
    const [error, setError] = useState('');

    const getGeminiTip = async () => {
        setLoading(true);
        setError('');
        setTip('');
        try {
            const prompt = "قدم نصيحة قصيرة وملهمة حول إدارة الوقت أو الإنتاجية.";
            let chatHistory = [];
            chatHistory.push({ role: "user", parts: [{ text: prompt }] });
            const payload = { contents: chatHistory };
            const apiKey = ""; // If you want to use models other than gemini-2.0-flash or imagen-3.0-generate-002, provide an API key here. Otherwise, leave this as-is.
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.0-flash:generateContent?key=${apiKey}`;

            const response = await fetch(apiUrl, {
                method: 'POST',
                headers: { 'Content-Type': 'application/json' },
                body: JSON.stringify(payload)
            });

            const result = await response.json();
            if (result.candidates && result.candidates.length > 0 &&
                result.candidates[0].content && result.candidates[0].content.parts &&
                result.candidates[0].content.parts.length > 0) {
                const text = result.candidates[0].content.parts[0].text;
                setTip(text);
            } else {
                setError("عذرًا، لم أتمكن من الحصول على نصيحة. الرجاء المحاولة مرة أخرى.");
                console.error("Unexpected API response structure:", result);
            }
        } catch (err) {
            setError("حدث خطأ أثناء جلب النصيحة. الرجاء التحقق من اتصالك بالإنترنت.");
            console.error("Error fetching Gemini tip:", err);
        } finally {
            setLoading(false);
        }
    };

    return (
        <div className="bg-gradient-to-r from-teal-400 to-cyan-500 text-white p-6 rounded-xl shadow-lg flex flex-col items-center justify-center text-center transform transition-transform duration-300 hover:scale-105">
            <h2 className="text-2xl font-bold mb-4">مساعد إدارة الوقت ✨</h2>
            <button
                onClick={getGeminiTip}
                className="bg-indigo-600 hover:bg-indigo-700 text-white font-bold py-3 px-6 rounded-full shadow-lg transition-all duration-300 transform hover:scale-105"
                disabled={loading}
            >
                {loading ? 'جارٍ التحميل...' : 'احصل على نصيحة ✨'}
            </button>
            {tip && (
                <p className="mt-4 text-lg font-semibold bg-white bg-opacity-10 p-4 rounded-lg w-full">
                    {tip}
                </p>
            )}
            {error && (
                <p className="mt-4 text-lg font-semibold text-red-300">
                    {error}
                </p>
            )}
        </div>
    );
};

export default App;
