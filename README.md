Inspiration: https://mirror.xyz/0xa81Da41fE8B5bB2ed22d2b209e7f97d3B7757a02 

https://poe.com/ScamGuardAI.V01 

https://vimeo.com/1099261111?share=copy#t=0

https://bbd4d9c2-26dd-45a3-aaee-983d9eba2f4c-00-ejx03e95nl0d.janeway.replit.dev/#

https://gemini.google.com/share/a7818ee56795;

# ScamGuardAI 

ScamGuardAI aims to be the world’s first truly adaptive, omni-channel shield against the full spectrum of digital fraud—from classic phishing links and social engineering to AI-cloned voices and deep-fake visuals. It leverages multi-modal AI (NLP, computer vision, behavior analytics) to detect, prevent, and neutralize emerging threats before they harm users.
It envisions a future where:
Every individual and organization is protected in real time across emails, social media, messaging apps, voice/video, and AI-generated content.
Defenses don’t lag threats — the system learns continuously from new scam patterns, evolving with the adversaries.
Reporting and community input feed directly into model updates, making protection crowdsourced, transparent, and collective.
Trust is restored online: people interact freely, engage in web3, chatbots, and digital platforms without fear of impersonation, manipulation, or fraud.
ScamGuardAI isn’t just a tool — it’s the backbone of digital trust for the next era.

Tech Stack Selection https://docs.google.com/document/d/1P922CCFlrf2p7w10aZYC5B3SlwHTEIIU8G88Sb0emPI/edit?usp =drivesdk

Diagram https://docs.google.com/document/d/1QGWqF1MC2eYkWP66FvoAEPDL6dOlkm5BdpMEz_MflC0/edi t?usp=drivesdk 

Cost estimate https://drive.google.com/file/d/1r9tl3t3KnjoK_x1ZPwogbDbJnSKD6chq/view?usp=drivesdk 

Impact Potential and Limitations https://docs.google.com/document/d/1R_1v_IovsJs-ZhD8IfXJKXmZux8SHnyLhd5opIvy80o/edit?usp=drivesdk 

Ethical & Security Considerations https://docs.google.com/document/d/15VLq8ANkJV1qDaX_U7lFIGr1ZXGttkVug09NzXcuSiQ/edit?usp=drivesdk

🛡️ ScamGuardAI — The AI-Powered Shield for Digital Trust
🔍 Problem
The digital world faces an explosion of scams:
Phishing, fake KYC requests, AI-cloned voices, and deepfake impersonations are spreading faster than humans or legacy tools can detect.
Over $10B+ in losses globally each year from digital scams.
Users lack real-time, cross-platform protection — most tools only react after damage is done.
💡 Solution
ScamGuardAI is an AI-driven fraud intelligence network that:
Detects and prevents scams in real time using multimodal AI (text, image, voice, and behavioral analysis).
Integrates seamlessly with email, chat, web3 wallets, and social apps.
Employs crowdsourced threat reporting to continuously retrain detection models.
Provides enterprise-grade APIs and a browser/extension app for individuals.
🚀 Vision
To become the universal AI defense layer that protects digital citizens and organizations across every platform and device — building a safer, scam-free digital ecosystem.
“Our mission is to make digital trust autonomous, adaptive, and accessible to everyone.”
⚙️ Core Technologies
Large Language Models (LLMs) for phishing intent and context analysis
Vision AI for deepfake and image-based scam detection
Voiceprint AI for audio impersonation detection
Blockchain traceability layer for verifying message or sender authenticity
Crowdsourced feedback engine for continuous model reinforcement
🌍 Impact
Protects users, companies, and governments from online fraud
Builds public trust in Web3, fintech, and AI ecosystems
Creates a global anti-scam intelligence network

import React, { useState, useEffect, createContext, useContext } from 'react';

// Create a context for language management
const LanguageContext = createContext();

// Mock API base URL (in a real app, this would be your API Gateway endpoint)
const API_BASE_URL = 'https://mock-api.scamguard.ai';

// Mock data for scams, with added focus on WEB3 and AI scams
const mockScams = [
  {
    id: 'scam001',
    title: {
      en: 'Phishing Email: Urgent Account Verification',
      vi: 'Email Lừa Đảo: Xác Minh Tài Khoản Khẩn Cấp',
    },
    category: {
      en: 'Online Phishing',
      vi: 'Lừa Đảo Trực Tuyến (Phishing)',
    },
    description: {
      en: 'Scammers send emails pretending to be from banks or popular services, asking you to click a link to "verify" your account or face suspension. The link leads to a fake website designed to steal your credentials.',
      vi: 'Kẻ lừa đảo gửi email giả mạo ngân hàng hoặc dịch vụ phổ biến, yêu cầu bạn nhấp vào liên kết để "xác minh" tài khoản hoặc đối mặt với việc bị đình chỉ. Liên kết dẫn đến một trang web giả mạo được thiết kế để đánh cắp thông tin đăng nhập của bạn.',
    },
    keywords: ['email', 'phishing', 'account', 'verification', 'fake website', 'traditional'],
    era: 'Old Day to AI Era',
    lastUpdated: '2025-06-29',
  },
  {
    id: 'scam002',
    title: {
      en: 'Romance Scam: Online Lover Needs Money',
      vi: 'Lừa Đảo Tình Cảm: Người Yêu Qua Mạng Cần Tiền',
    },
    category: {
      en: 'Social Engineering',
      vi: 'Thao Túng Tâm Lý (Social Engineering)',
    },
    description: {
      en: 'Scammers build emotional relationships online, often over long periods, then fabricate emergencies (medical, travel, business) to ask for money. They never meet in person.',
      vi: 'Kẻ lừa đảo xây dựng mối quan hệ tình cảm trực tuyến, thường trong thời gian dài, sau đó bịa đặt các trường hợp khẩn cấp (y tế, du lịch, kinh doanh) để yêu cầu tiền. Họ không bao giờ gặp mặt trực tiếp.',
    },
    keywords: ['romance', 'love', 'money', 'online dating', 'emergency', 'traditional'],
    era: 'Old Day to AI Era',
    lastUpdated: '2025-06-25',
  },
  {
    id: 'scam003',
    title: {
      en: 'AI Voice Cloning Scam: Impersonating a Family Member',
      vi: 'Lừa Đảo Bằng Giọng Nói AI: Giả Mạo Người Thân',
    },
    category: {
      en: 'AI/Deepfake Fraud',
      vi: 'Gian Lận AI/Deepfake',
    },
    description: {
      en: 'Scammers use AI to clone the voice of a family member (e.g., child, parent) to create a sense of urgency, claiming to be in trouble and needing immediate money transfer. Always verify with a code word or by calling back on a known number.',
      vi: 'Kẻ lừa đảo sử dụng AI để nhân bản giọng nói của người thân (ví dụ: con cái, cha mẹ) để tạo cảm giác khẩn cấp, tuyên bố đang gặp rắc rối và cần chuyển tiền ngay lập tức. Luôn xác minh bằng mật khẩu hoặc gọi lại theo số điện thoại đã biết.',
    },
    keywords: ['AI', 'voice cloning', 'deepfake', 'impersonation', 'urgent', 'money transfer', 'AI scam'],
    era: 'AI Era',
    lastUpdated: '2025-06-30',
  },
  {
    id: 'scam004',
    title: {
      en: 'Cryptocurrency Investment Scam: Fake Platforms',
      vi: 'Lừa Đảo Đầu Tư Tiền Điện Tử: Nền Tảng Giả Mạo',
    },
    category: {
      en: 'WEB3/Crypto Fraud',
      vi: 'Gian Lận WEB3/Tiền Điện Tử',
    },
    description: {
      en: 'Scammers promise high, guaranteed returns on cryptocurrency investments through fake platforms or "expert" advice. They often show fabricated profits initially to lure victims into investing more before disappearing with the funds. Often involves fake trading bots or liquidity pools.',
      vi: 'Kẻ lừa đảo hứa hẹn lợi nhuận cao, được đảm bảo từ các khoản đầu tư tiền điện tử thông qua các nền tảng giả mạo hoặc lời khuyên "chuyên gia". Họ thường hiển thị lợi nhuận giả tạo ban đầu để dụ dỗ nạn nhân đầu tư nhiều hơn trước đó trước khi biến mất cùng số tiền. Thường liên quan đến bot giao dịch hoặc nhóm thanh khoản giả mạo.',
    },
    keywords: ['crypto', 'investment', 'bitcoin', 'ethereum', 'returns', 'fake platform', 'WEB3 scam', 'blockchain'],
    era: 'Modern Era',
    lastUpdated: '2025-06-20',
  },
  {
    id: 'scam005',
    title: {
      en: 'NFT Rug Pull: Project Abandons Buyers',
      vi: 'Lừa Đảo NFT Rug Pull: Dự Án Bỏ Rơi Người Mua',
    },
    category: {
      en: 'WEB3/NFT Fraud',
      vi: 'Gian Lận WEB3/NFT',
    },
    description: {
      en: 'Developers of an NFT project suddenly abandon it after collecting funds from buyers, leaving investors with worthless NFTs. This often happens with promises of future utility, metaverse integration, or exclusive access that never materialize.',
      vi: 'Các nhà phát triển dự án NFT đột ngột từ bỏ dự án sau khi thu tiền từ người mua, khiến các nhà đầu tư sở hữu NFT vô giá trị. Điều này thường xảy ra với những lời hứa hẹn về tiện ích trong tương lai, tích hợp metaverse hoặc quyền truy cập độc quyền không bao giờ thành hiện thực.',
    },
    keywords: ['NFT', 'rug pull', 'web3', 'crypto', 'blockchain', 'worthless assets', 'smart contract'],
    era: 'AI Era',
    lastUpdated: '2025-06-28',
  },
  {
    id: 'scam006',
    title: {
      en: 'AI Chatbot Impersonation: Customer Service Fraud',
      vi: 'Lừa Đảo Chatbot AI: Gian Lận Dịch Vụ Khách Hàng',
    },
    category: {
      en: 'AI/Chatbot Fraud',
      vi: 'Gian Lận AI/Chatbot',
    },
    description: {
      en: 'Scammers deploy AI-powered chatbots on fake websites or messaging apps, impersonating legitimate customer service. They trick users into revealing personal information, passwords, or even performing transactions under false pretenses.',
      vi: 'Kẻ lừa đảo triển khai chatbot do AI cung cấp trên các trang web hoặc ứng dụng nhắn tin giả mạo, mạo danh dịch vụ khách hàng hợp pháp. Chúng lừa người dùng tiết lộ thông tin cá nhân, mật khẩu hoặc thậm chí thực hiện các giao dịch dưới chiêu trò giả mạo.',
    },
    keywords: ['AI', 'chatbot', 'impersonation', 'customer service', 'fake website', 'phishing', 'AI scam'],
    era: 'AI Era',
    lastUpdated: '2025-06-29',
  },
  {
    id: 'scam007',
    title: {
      en: 'DeFi (Decentralized Finance) Exploit: Flash Loan Attacks',
      vi: 'Khai Thác DeFi (Tài Chính Phi Tập Trung): Tấn Công Cho Vay Tức Thời',
    },
    category: {
      en: 'WEB3/DeFi Vulnerability',
      vi: 'Lỗ Hổng WEB3/DeFi',
    },
    description: {
      en: 'While not always a "scam" in the traditional sense, malicious actors exploit vulnerabilities in DeFi protocols (often through flash loan attacks or re-entrancy bugs) to drain liquidity pools or manipulate asset prices for profit. Users lose funds due to these exploits.',
      vi: 'Mặc dù không phải lúc nào cũng là "lừa đảo" theo nghĩa truyền thống, nhưng những kẻ độc hại khai thác các lỗ hổng trong các giao thức DeFi (thường thông qua các cuộc tấn công cho vay tức thời hoặc lỗi tái nhập) để rút cạn nhóm thanh khoản hoặc thao túng giá tài sản để kiếm lời. Người dùng mất tiền do những khai thác này.',
    },
    keywords: ['DeFi', 'flash loan', 'exploit', 'smart contract', 'vulnerability', 'web3', 'crypto', 'liquidity pool'],
    era: 'Modern Era',
    lastUpdated: '2025-06-27',
  },
];


// Language Provider Component
const LanguageProvider = ({ children }) => {
  const [language, setLanguage] = useState('en'); // Default language is English

  const toggleLanguage = () => {
    setLanguage((prevLang) => (prevLang === 'en' ? 'vi' : 'en'));
  };

  const getText = (textObject) => {
    return textObject[language] || textObject['en']; // Fallback to English if translation not available
  };

  return (
    <LanguageContext.Provider value={{ language, toggleLanguage, getText }}>
      {children}
    </LanguageContext.Provider>
  );
};

// Common UI Component for messages
const Message = ({ type, children }) => {
  let bgColor = '';
  let textColor = '';
  switch (type) {
    case 'success':
      bgColor = 'bg-green-100';
      textColor = 'text-green-800';
      break;
    case 'error':
      bgColor = 'bg-red-100';
      textColor = 'text-red-800';
      break;
    case 'info':
      bgColor = 'bg-blue-100';
      textColor = 'text-blue-800';
      break;
    default:
      bgColor = 'bg-gray-100';
      textColor = 'text-gray-800';
  }
  return (
    <div className={`p-3 my-4 rounded-lg shadow-md ${bgColor} ${textColor}`}>
      {children}
    </div>
  );
};

// Main App Component
const App = () => {
  const { language, toggleLanguage, getText } = useContext(LanguageContext);
  const [scams, setScams] = useState([]);
  const [loading, setLoading] = useState(false);
  const [message, setMessage] = useState(null); // { type: 'success' | 'error' | 'info', text: string }
  const [showReportForm, setShowReportForm] = useState(false);

  useEffect(() => {
    fetchScams();
  }, []);

  // Function to fetch scams (mocked API call)
  const fetchScams = async () => {
    setLoading(true);
    setMessage(null);
    try {
      // Simulate API call delay
      await new Promise((resolve) => setTimeout(resolve, 1000));
      setScams(mockScams); // Using mock data
      setMessage({ type: 'success', text: getText({en: 'Scams loaded successfully!', vi: 'Đã tải thành công các chiêu lừa đảo!'}) });
    } catch (error) {
      console.error('Error fetching scams:', error);
      setMessage({ type: 'error', text: getText({en: 'Failed to load scams. Please try again.', vi: 'Không thể tải các chiêu lừa đảo. Vui lòng thử lại.'}) });
    } finally {
      setLoading(false);
    }
  };

  // Function to handle scam report submission (mocked API call)
  const handleReportScam = async (scamData) => {
    setLoading(true);
    setMessage(null);
    try {
      // Simulate API call to POST /report-scam
      await new Promise((resolve) => setTimeout(resolve, 1500));

      // In a real scenario, the Lambda function would process and store this.
      // For this mock, we'll just add it to the local state.
      const newScam = {
        id: `scam${Date.now()}`,
        title: { en: scamData.title, vi: scamData.title }, // Assume title is sent in default lang for simplicity
        category: { en: scamData.category, vi: scamData.category },
        description: { en: scamData.description, vi: scamData.description },
        keywords: scamData.keywords.split(',').map(k => k.trim()),
        era: 'User Reported / AI Era',
        lastUpdated: new Date().toISOString().split('T')[0],
      };
      setScams((prevScams) => [newScam, ...prevScams]); // Add new scam to the top

      setMessage({ type: 'success', text: getText({en: 'Scam reported successfully! Thank you for your contribution.', vi: 'Đã báo cáo lừa đảo thành công! Cảm ơn bạn đã đóng góp.'}) });
      setShowReportForm(false); // Hide form after submission
    } catch (error) {
      console.error('Error reporting scam:', error);
      setMessage({ type: 'error', text: getText({en: 'Failed to report scam. Please try again.', vi: 'Không thể báo cáo lừa đảo. Vui lòng thử lại.'}) });
    } finally {
      setLoading(false);
    }
  };

  return (
    <div className="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 font-inter text-gray-800 p-4 sm:p-6 lg:p-8">
      <div className="max-w-4xl mx-auto bg-white rounded-xl shadow-lg p-6 sm:p-8">
        {/* Header */}
        <header className="mb-8 flex flex-col sm:flex-row justify-between items-center">
          <h1 className="text-3xl sm:text-4xl font-bold text-indigo-700 mb-4 sm:mb-0">
            <i className="fas fa-shield-alt mr-2 text-blue-500"></i>
            ScamGuard AI
          </h1>
          <div className="flex items-center space-x-4">
            <button
              onClick={toggleLanguage}
              className="px-4 py-2 bg-indigo-500 text-white rounded-lg shadow hover:bg-indigo-600 transition duration-300 ease-in-out text-sm font-medium"
            >
              {language === 'en' ? 'Tiếng Việt' : 'English'}
            </button>
            <button
              onClick={() => setShowReportForm(!showReportForm)}
              className="px-4 py-2 bg-green-500 text-white rounded-lg shadow hover:bg-green-600 transition duration-300 ease-in-out text-sm font-medium"
            >
              <i className="fas fa-plus-circle mr-2"></i>
              {getText({en: 'Report a Scam', vi: 'Báo Cáo Lừa Đảo'})}
            </button>
          </div>
        </header>

        {/* Messages */}
        {message && <Message type={message.type}>{message.text}</Message>}

        {/* Report Scam Form */}
        {showReportForm && (
          <ReportScamForm
            onSubmit={handleReportScam}
            onCancel={() => setShowReportForm(false)}
            loading={loading}
          />
        )}

        {/* Scam List */}
        <section className="mt-8">
          <h2 className="text-2xl font-semibold text-indigo-600 mb-6">
            {getText({en: 'Recent Scam Alerts', vi: 'Cảnh Báo Lừa Đảo Gần Đây'})}
          </h2>
          {loading && (
            <div className="flex justify-center items-center py-8">
              <div className="animate-spin rounded-full h-12 w-12 border-b-2 border-indigo-500"></div>
              <p className="ml-4 text-indigo-500">{getText({en: 'Loading scams...', vi: 'Đang tải chiêu lừa đảo...'})}</p>
            </div>
          )}
          {!loading && scams.length === 0 && (
            <Message type="info">
              {getText({en: 'No scams found. Please check back later or report a new one!', vi: 'Không tìm thấy chiêu lừa đảo nào. Vui lòng kiểm tra lại sau hoặc báo cáo chiêu mới!'})}
            </Message>
          )}
          <div className="grid gap-6">
            {scams.map((scam) => (
              <ScamCard key={scam.id} scam={scam} />
            ))}
          </div>
        </section>
      </div>

      {/* Font Awesome for icons (loaded globally) */}
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />
    </div>
  );
};

// Scam Card Component
const ScamCard = ({ scam }) => {
  const { getText } = useContext(LanguageContext);
  const [expanded, setExpanded] = useState(false);

  return (
    <div className="bg-white border border-gray-200 rounded-lg shadow-md p-5 transition-all duration-300 ease-in-out hover:shadow-lg">
      <h3 className="text-xl font-bold text-gray-900 mb-2">{getText(scam.title)}</h3>
      <div className="flex flex-wrap items-center text-sm text-gray-600 mb-3">
        <span className="mr-3 flex items-center">
          <i className="fas fa-tag mr-1 text-blue-400"></i>
          {getText(scam.category)}
        </span>
        <span className="mr-3 flex items-center">
          <i className="fas fa-clock mr-1 text-purple-400"></i>
          {scam.era}
        </span>
        <span className="flex items-center">
          <i className="fas fa-calendar-alt mr-1 text-green-400"></i>
          {scam.lastUpdated}
        </span>
      </div>
      <p className="text-gray-700 mb-3 text-justify">
        {expanded ? getText(scam.description) : `${getText(scam.description).substring(0, 150)}...`}
      </p>
      {getText(scam.description).length > 150 && (
        <button
          onClick={() => setExpanded(!expanded)}
          className="text-indigo-600 hover:text-indigo-800 text-sm font-medium"
        >
          {expanded ? getText({en: 'Show Less', vi: 'Thu Gọn'}) : getText({en: 'Read More', vi: 'Đọc Thêm'})}
        </button>
      )}
      <div className="mt-3 flex flex-wrap gap-2">
        {scam.keywords.map((keyword, index) => (
          <span
            key={index}
            className="px-3 py-1 bg-gray-100 text-gray-600 text-xs rounded-full border border-gray-300"
          >
            {keyword}
          </span>
        ))}
      </div>
    </div>
  );
};

// Report Scam Form Component
const ReportScamForm = ({ onSubmit, onCancel, loading }) => {
  const { getText } = useContext(LanguageContext);
  const [title, setTitle] = useState('');
  const [category, setCategory] = useState('');
  const [description, setDescription] = useState('');
  const [keywords, setKeywords] = useState('');
  const [errors, setErrors] = useState({});

  const validateForm = () => {
    const newErrors = {};
    if (!title.trim()) newErrors.title = getText({en: 'Title is required.', vi: 'Tiêu đề là bắt buộc.'});
    if (!category.trim()) newErrors.category = getText({en: 'Category is required.', vi: 'Danh mục là bắt buộc.'});
    if (!description.trim()) newErrors.description = getText({en: 'Description is required.', vi: 'Mô tả là bắt buộc.'});
    if (!keywords.trim()) newErrors.keywords = getText({en: 'Keywords are required.', vi: 'Từ khóa là bắt buộc.'});
    setErrors(newErrors);
    return Object.keys(newErrors).length === 0;
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    if (validateForm()) {
      onSubmit({ title, category, description, keywords });
      // Reset form fields after submission attempt
      setTitle('');
      setCategory('');
      setDescription('');
      setKeywords('');
      setErrors({});
    }
  };

  return (
    <div className="bg-blue-50 p-6 rounded-lg shadow-inner mb-8">
      <h3 className="text-xl font-semibold text-blue-700 mb-4">
        {getText({en: 'Report a New Scam', vi: 'Báo Cáo Chiêu Lừa Đảo Mới'})}
      </h3>
      <form onSubmit={handleSubmit}>
        <div className="mb-4">
          <label htmlFor="scamTitle" className="block text-gray-700 text-sm font-bold mb-2">
            {getText({en: 'Scam Title:', vi: 'Tiêu Đề Lừa Đảo:'})}
          </label>
          <input
            type="text"
            id="scamTitle"
            className={`shadow appearance-none border rounded-lg w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-500 ${errors.title ? 'border-red-500' : 'border-gray-300'}`}
            value={title}
            onChange={(e) => { setTitle(e.target.value); setErrors(prev => ({ ...prev, title: '' })); }}
            placeholder={getText({en: 'e.g., Fake Tech Support Call', vi: 'ví dụ: Cuộc Gọi Hỗ Trợ Kỹ Thuật Giả Mạo'})}
          />
          {errors.title && <p className="text-red-500 text-xs italic mt-1">{errors.title}</p>}
        </div>
        <div className="mb-4">
          <label htmlFor="scamCategory" className="block text-gray-700 text-sm font-bold mb-2">
            {getText({en: 'Category (e.g., Phishing, WEB3/Crypto Fraud, AI/Deepfake Fraud):', vi: 'Danh Mục (ví dụ: Lừa Đảo, Gian Lận WEB3/Tiền Điện Tử, Gian Lận AI/Deepfake):'})}
          </label>
          <input
            type="text"
            id="scamCategory"
            className={`shadow appearance-none border rounded-lg w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-500 ${errors.category ? 'border-red-500' : 'border-gray-300'}`}
            value={category}
            onChange={(e) => { setCategory(e.target.value); setErrors(prev => ({ ...prev, category: '' })); }}
            placeholder={getText({en: 'e.g., WEB3/Crypto Fraud', vi: 'ví dụ: Gian Lận WEB3/Tiền Điện Tử'})}
          />
          {errors.category && <p className="text-red-500 text-xs italic mt-1">{errors.category}</p>}
        </div>
        <div className="mb-4">
          <label htmlFor="scamDescription" className="block text-gray-700 text-sm font-bold mb-2">
            {getText({en: 'Detailed Description:', vi: 'Mô Tả Chi Tiết:'})}
          </label>
          <textarea
            id="scamDescription"
            rows="4"
            className={`shadow appearance-none border rounded-lg w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-500 ${errors.description ? 'border-red-500' : 'border-gray-300'}`}
            value={description}
            onChange={(e) => { setDescription(e.target.value); setErrors(prev => ({ ...prev, description: '' })); }}
            placeholder={getText({en: 'Describe the scam: how it works, what to look for, etc.', vi: 'Mô tả chiêu lừa đảo: cách thức hoạt động, những dấu hiệu nhận biết, v.v.'})}
          ></textarea>
          {errors.description && <p className="text-red-500 text-xs italic mt-1">{errors.description}</p>}
        </div>
        <div className="mb-6">
          <label htmlFor="scamKeywords" className="block text-gray-700 text-sm font-bold mb-2">
            {getText({en: 'Keywords (comma-separated):', vi: 'Từ Khóa (ngăn cách bằng dấu phẩy):'})}
          </label>
          <input
            type="text"
            id="scamKeywords"
            className={`shadow appearance-none border rounded-lg w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:ring-2 focus:ring-blue-500 ${errors.keywords ? 'border-red-500' : 'border-gray-300'}`}
            value={keywords}
            onChange={(e) => { setKeywords(e.target.value); setErrors(prev => ({ ...prev, keywords: '' })); }}
            placeholder={getText({en: 'e.g., crypto, phishing, wallet, AI, deepfake', vi: 'ví dụ: tiền điện tử, lừa đảo, ví, AI, deepfake'})}
          />
          {errors.keywords && <p className="text-red-500 text-xs italic mt-1">{errors.keywords}</p>}
        </div>
        <div className="flex items-center justify-end space-x-3">
          <button
            type="button"
            onClick={onCancel}
            className="px-5 py-2 border border-gray-300 text-gray-700 rounded-lg shadow-sm hover:bg-gray-100 transition duration-300 ease-in-out font-medium"
            disabled={loading}
          >
            {getText({en: 'Cancel', vi: 'Hủy'})}
          </button>
          <button
            type="submit"
            className={`px-5 py-2 rounded-lg shadow-md font-medium transition duration-300 ease-in-out ${
              loading ? 'bg-blue-300 cursor-not-allowed' : 'bg-blue-600 text-white hover:bg-blue-700'
            }`}
            disabled={loading}
          >
            {loading ? (
              <i className="fas fa-spinner fa-spin mr-2"></i>
            ) : (
              <i className="fas fa-paper-plane mr-2"></i>
            )}
            {getText({en: 'Submit Report', vi: 'Gửi Báo Cáo'})}
          </button>
        </div>
      </form>
    </div>
  );
};

// Root component for rendering
const RootApp = () => (
  <LanguageProvider>
    <App />
  </LanguageProvider>
);

export default RootApp;
     
Proactive, AI-native defense. We shield you from evolving online scams—from phishing to deepfakes—across all digital channels. Our adaptive AI constantly learns, ensuring future-proof protection and restoring trust in your phy/digital world.
ScamGuardAI: Your Shield Against the Evolving Digital Threat
1. The Problem: A Pervasive & Evolving Threat
Online scams and fraudulent activities are a global epidemic, causing billions in financial losses annually, immense emotional distress, and a severe erosion of trust in digital platforms.

Financial Impact: Individuals, businesses, and governments suffer staggering monetary damages.

Emotional Toll: Victims experience stress, anxiety, and a sense of violation.

Erosion of Trust: The digital landscape becomes a minefield, hindering genuine online engagement.

Reactive & Outdated Defenses: Traditional rule-based systems and first-generation AI solutions are easily outsmarted by sophisticated, rapidly evolving scam tactics, especially those leveraging advanced AI.

2. The Solution: Proactive, AI-Native Digital Protection
ScamGuardAI is an advanced AI-powered solution engineered to proactively detect and prevent online scams across all digital communication channels. We leverage cutting-edge machine learning and natural language processing to identify and neutralize threats before they cause harm.

Our solution moves beyond reactive measures, offering a dynamic, intelligent defense that adapts to the ever-changing landscape of digital fraud, from classic phishing to AI-generated deepfakes.

3. Market Opportunity: A Growing Need for Advanced Security
The digital economy is expanding rapidly, and with it, the surface area for scams. As more of our lives move online – from banking and shopping to social interaction – the demand for robust, intelligent protection is skyrocketing.

Massive User Base: Billions of internet users worldwide are potential targets.

Increasing Sophistication: AI is empowering fraudsters to create highly convincing and scalable attacks.

Regulatory Pressure: Growing awareness and legislative efforts push for stronger consumer protection.

4. Technology: The Power of Adaptive Intelligence
ScamGuardAI is built on a robust, scalable architecture integrating state-of-the-art AI/ML frameworks:

AI/ML Core: TensorFlow, PyTorch, Scikit-learn for Deep Learning, Machine Learning, and Unsupervised Learning.

Natural Language Processing (NLP): Hugging Face Transformers, NLTK/SpaCy for sophisticated text analysis, deceptive language detection, and AI-generated content identification.

Computer Vision (CV): OpenCV, Pillow for analyzing images, videos, detecting fake visuals, and deepfakes.

Behavioral Analytics: Identifying anomalous user patterns and interactions.

Data Streaming: Apache Kafka, Apache Flink/Spark Streaming for real-time data ingestion and processing.

Cloud Infrastructure: Leveraging scalable compute (Kubernetes, Serverless), storage (NoSQL, Graph DBs), and networking from leading cloud providers.

5. Key Features: Comprehensive Multi-Layered Protection
Real-time Threat Analysis: Instant scanning of emails, messages, social media, and web content.

Multi-Modal AI Engine: Combines NLP, CV, and behavioral analytics for holistic detection.

Deceptive Language & Impersonation Detection: Flags suspicious linguistic patterns and identity spoofing.

Fake Visuals & Deepfake Analysis: Identifies manipulated images, videos, and website designs.

Anomalous Behavior Flagging: Detects unusual user activity indicative of compromise.

Malicious URL & Link Verification: Scans and verifies links for phishing and malware.

AI-Generated Content Identification: Specifically targets scams created by generative AI.

Proactive Mitigation: Auto-blocking malicious content, quarantining suspicious communications.

Real-time Alerts & Advice: Instant notifications with actionable recommendations.

Continuous Model Updates: Our AI constantly learns from new threats, staying ahead of fraudsters.

6. Competitive Advantage: AI-Native, Omni-Channel, Future-Proof
ScamGuardAI stands apart with its "AI-Native, Omni-Channel, and Future-Proof Adaptive Defense against All Scam Evolution."

AI-Native: Not just an add-on, AI is the core, enabling detection of novel threats without prior explicit training.

Omni-Channel Coverage: Protects across all digital communication vectors – a truly unified shield.

Future-Proof Adaptive Defense: Designed to combat current tactics and rapidly adapt to, and even predict, the next generation of AI-driven fraud. We're building for tomorrow's threats, today.

7. Business Model (Hypothetical)
Subscription-based Service: Tiered plans for individuals, families, and small businesses.

Enterprise Solutions: Customized deployments and API integrations for larger organizations (e.g., financial institutions, social media platforms).

Freemium Model: Basic protection offered for free, with advanced features requiring a premium subscription.

8. Our Team (Placeholder)
A dedicated team of AI researchers, cybersecurity experts, software engineers, and product specialists committed to building a safer digital world.

9. Vision: A Safer Digital Future for Everyone
ScamGuardAI aims to become the leading standard for proactive digital scam protection, empowering individuals and organizations to navigate the online world with confidence and trust, and envisioning a future where the sophistication of defense always outpaces the ingenuity of deception.

Join us in building the next generation of digital security.
