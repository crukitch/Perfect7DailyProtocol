# Perfect7DailyProtocol
index.html
<!DOCTYPE html>

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Perfect7Daily Implementation Protocol</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

```
    body {
        font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
        line-height: 1.6;
        color: #333;
        background: #f8fffe;
        padding-bottom: 80px;
    }
    
    .container {
        max-width: 600px;
        margin: 0 auto;
        padding: 20px;
    }
    
    .header {
        background: linear-gradient(135deg, #16a085 0%, #2d8f47 100%);
        color: white;
        padding: 30px 20px;
        text-align: center;
        margin: -20px -20px 30px -20px;
        border-radius: 0 0 20px 20px;
    }
    
    .header h1 {
        font-size: 28px;
        margin-bottom: 10px;
        font-weight: 700;
    }
    
    .header p {
        font-size: 16px;
        opacity: 0.9;
    }
    
    .section {
        background: white;
        border-radius: 15px;
        padding: 25px;
        margin-bottom: 20px;
        box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        border-left: 5px solid #16a085;
    }
    
    .section h2 {
        color: #2d8f47;
        font-size: 20px;
        margin-bottom: 20px;
        display: flex;
        align-items: center;
        gap: 10px;
    }
    
    .disclaimer {
        background: #fff3cd;
        border: 2px solid #ffc107;
        border-radius: 10px;
        padding: 20px;
        margin-bottom: 30px;
        font-size: 14px;
    }
    
    .disclaimer h3 {
        color: #856404;
        margin-bottom: 15px;
        font-size: 16px;
    }
    
    .assessment-card {
        background: #f8f9fa;
        border: 2px solid #e9ecef;
        border-radius: 12px;
        padding: 20px;
        margin-bottom: 15px;
        transition: all 0.3s ease;
        cursor: pointer;
    }
    
    .assessment-card:hover {
        border-color: #16a085;
        transform: translateY(-2px);
        box-shadow: 0 4px 15px rgba(22, 160, 133, 0.2);
    }
    
    .assessment-card.selected {
        border-color: #16a085;
        background: linear-gradient(135deg, #f0f9f0 0%, #e8f5e8 100%);
    }
    
    .level-title {
        color: #2d8f47;
        font-weight: bold;
        font-size: 18px;
        margin-bottom: 8px;
    }
    
    .pain-description {
        font-weight: bold;
        color: #e74c3c;
        margin-bottom: 10px;
    }
    
    .checkbox-item {
        display: flex;
        align-items: flex-start;
        gap: 12px;
        margin-bottom: 12px;
        padding: 12px;
        background: #f8f9fa;
        border-radius: 8px;
        cursor: pointer;
        transition: all 0.2s ease;
    }
    
    .checkbox-item:hover {
        background: #e9ecef;
    }
    
    .checkbox-item.checked {
        background: linear-gradient(135deg, #e8f5e8 0%, #d4edda 100%);
        border-left: 4px solid #16a085;
    }
    
    .checkbox {
        width: 20px;
        height: 20px;
        border: 2px solid #16a085;
        border-radius: 4px;
        display: flex;
        align-items: center;
        justify-content: center;
        flex-shrink: 0;
        background: white;
        margin-top: 2px;
    }
    
    .checkbox.checked {
        background: #16a085;
    }
    
    .checkbox.checked::after {
        content: '✓';
        color: white;
        font-size: 14px;
        font-weight: bold;
    }
    
    .vegetable-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
        gap: 15px;
        margin: 20px 0;
    }
    
    .vegetable-card {
        background: linear-gradient(135deg, #f8fff8 0%, #e8f5e8 100%);
        border: 2px solid #a8e6cf;
        border-radius: 12px;
        padding: 15px;
        text-align: center;
        transition: transform 0.2s ease;
    }
    
    .vegetable-card:hover {
        transform: translateY(-3px);
    }
    
    .vegetable-emoji {
        font-size: 32px;
        margin-bottom: 8px;
        display: block;
    }
    
    .vegetable-name {
        color: #2d8f47;
        font-weight: bold;
        font-size: 14px;
        margin-bottom: 5px;
    }
    
    .vegetable-desc {
        font-size: 12px;
        color: #666;
    }
    
    .schedule-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
        gap: 15px;
        margin: 20px 0;
    }
    
    .schedule-card {
        background: #f8f9fa;
        padding: 15px;
        border-radius: 10px;
        border-left: 4px solid #16a085;
    }
    
    .schedule-card.night {
        background: #fff3cd;
        border-left-color: #f39c12;
    }
    
    .schedule-title {
        font-weight: bold;
        color: #2d8f47;
        margin-bottom: 10px;
    }
    
    .important-box {
        background: #fff5f5;
        border: 2px solid #e74c3c;
        border-radius: 10px;
        padding: 20px;
        margin: 20px 0;
    }
    
    .important-title {
        color: #c0392b;
        font-weight: bold;
        margin-bottom: 10px;
    }
    
    .faq-item {
        background: #f8f9fa;
        border-radius: 10px;
        margin-bottom: 15px;
        overflow: hidden;
        border-left: 4px solid #16a085;
    }
    
    .faq-question {
        background: #16a085;
        color: white;
        padding: 15px;
        font-weight: bold;
        cursor: pointer;
        transition: background 0.3s ease;
    }
    
    .faq-question:hover {
        background: #138d75;
    }
    
    .faq-answer {
        padding: 15px;
        display: none;
        line-height: 1.6;
    }
    
    .faq-answer.active {
        display: block;
    }
    
    .bottom-nav {
        position: fixed;
        bottom: 0;
        left: 0;
        right: 0;
        background: white;
        border-top: 1px solid #e9ecef;
        padding: 10px;
        display: flex;
        justify-content: space-around;
        box-shadow: 0 -2px 10px rgba(0,0,0,0.1);
    }
    
    .nav-btn {
        background: none;
        border: none;
        padding: 8px 12px;
        border-radius: 8px;
        cursor: pointer;
        transition: all 0.2s ease;
        font-size: 12px;
        text-align: center;
        min-width: 60px;
    }
    
    .nav-btn.active {
        background: #16a085;
        color: white;
    }
    
    .nav-btn:hover {
        background: #e9ecef;
    }
    
    .nav-btn.active:hover {
        background: #138d75;
    }
    
    .hidden {
        display: none;
    }
    
    .contact-info {
        text-align: center;
        margin-top: 30px;
        padding: 20px;
        background: linear-gradient(135deg, #e8f5e8 0%, #d4edda 100%);
        border-radius: 15px;
    }
    
    .contact-info h3 {
        color: #2d8f47;
        margin-bottom: 10px;
    }
    
    .contact-info p {
        color: #2d8f47;
    }
    
    @media (max-width: 768px) {
        .vegetable-grid,
        .schedule-grid {
            grid-template-columns: 1fr;
        }
        
        .container {
            padding: 15px;
        }
    }
</style>
```

<div class="container">
    <div class="disclaimer">
        <h3>ABOUT THE CREATOR & DISCLAIMER</h3>
        <p><strong>ABOUT THE CREATOR:</strong><br>
        I am a registered magnetic resonance imaging (MRI) technologist and formerly trained DEXA technologist who developed the Perfect7Daily system after being diagnosed with osteoarthritis. My results are based on scientific research and consistent application of this nutritional protocol.</p>
        
        <p style="margin-top: 15px;"><strong>INFORMATIONAL PURPOSE:</strong><br>
        This protocol is an informational system based on science-backed research demonstrating that cruciferous vegetables contain beneficial nutrients and compounds that support human health and may help reduce inflammation.</p>
        
        <p style="margin-top: 15px;"><strong>MEDICAL DISCLAIMER:</strong><br>
        This assessment and protocol are not intended to diagnose, treat, cure, or prevent any disease or medical condition. The information provided is for educational purposes only and should not be considered medical advice.</p>
        
        <p style="margin-top: 10px;">Always consult with a qualified healthcare professional before making significant dietary changes, especially if you have existing medical conditions, are taking medications, or are pregnant or nursing.</p>
        
        <p style="margin-top: 10px; font-style: italic;">Individual results may vary. The creator's personal experience does not guarantee similar outcomes for others.</p>
    </div>

    <div class="section" id="assessment">
        <h2>Inflammation Level Assessment</h2>
        <p style="margin-bottom: 20px; font-weight: bold;">Answer: Is/Does your body pain:</p>
        
        <div class="assessment-card" onclick="selectLevel(3, this)">
            <div class="level-title">LEVEL 3 (High Inflammation): 3 cups daily</div>
            <div class="pain-description">Constant and spreading</div>
            <ul style="margin-left: 20px;">
                <li>Pain is always present and affecting multiple areas</li>
                <li>Daily activities significantly impacted</li>
                <li>Protocol: 3 cups daily across 7 servings</li>
            </ul>
        </div>
        
        <div class="assessment-card" onclick="selectLevel(2, this)">
            <div class="level-title">LEVEL 2 (Moderate Inflammation): 2 cups daily</div>
            <div class="pain-description">Wake you up in the middle of the night</div>
            <ul style="margin-left: 20px;">
                <li>Pain disrupts your sleep regularly</li>
                <li>Moderate impact on daily life</li>
                <li>Protocol: 2 cups daily across 7 servings</li>
            </ul>
        </div>
        
        <div class="assessment-card" onclick="selectLevel(1, this)">
            <div class="level-title">LEVEL 1 (Low Inflammation): 1 cup daily</div>
            <div class="pain-description">Come and go, not always present</div>
            <ul style="margin-left: 20px;">
                <li>Occasional discomfort or mild symptoms</li>
                <li>Minimal impact on daily activities</li>
                <li>Protocol: 1 cup daily across 7 servings</li>
            </ul>
        </div>
        
        <div class="important-box">
            <div class="important-title">BACKUP ASSESSMENT:</div>
            <p style="margin-bottom: 15px;">If you don't have body pain, rate your energy level:</p>
            <div class="assessment-card" onclick="selectEnergyLevel('tired', this)" style="margin-bottom: 10px;">
                <strong>Always tired = Level 3</strong> - Each serving = 1/2 cup or large handful
            </div>
            <div class="assessment-card" onclick="selectEnergyLevel('sometimes', this)" style="margin-bottom: 10px;">
                <strong>Sometimes tired = Level 2</strong> - Each serving = 1/3 cup or medium handful
            </div>
            <div class="assessment-card" onclick="selectEnergyLevel('energetic', this)">
                <strong>Generally energetic = Level 1</strong> - Each serving = 2-3 tablespoons or small handful
            </div>
        </div>
        
        <div id="selectedLevel" style="display: none; background: #e8f5e8; padding: 15px; border-radius: 10px; margin-top: 20px;">
            <h3 style="color: #2d8f47; margin-bottom: 10px;">Your Selected Level:</h3>
            <p id="levelDisplay" style="font-weight: bold; color: #2d8f47;"></p>
        </div>
    </div>

    <div class="section" id="schedule">
        <h2>Daily Protocol Schedule</h2>
        <p style="margin-bottom: 20px; font-weight: bold;">FOR ALL INFLAMMATION LEVELS:</p>
        
        <div class="schedule-grid">
            <div class="schedule-card">
                <div class="schedule-title">Morning</div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Small serving before breakfast</span>
                </div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Small serving after breakfast</span>
                </div>
            </div>
            
            <div class="schedule-card">
                <div class="schedule-title">Midday</div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Small serving before lunch</span>
                </div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Small serving after lunch</span>
                </div>
            </div>
            
            <div class="schedule-card">
                <div class="schedule-title">Evening</div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Small serving before dinner</span>
                </div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Small serving after dinner</span>
                </div>
            </div>
            
            <div class="schedule-card night">
                <div class="schedule-title">Night (MOST IMPORTANT)</div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>FINAL nighttime serving</span>
                </div>
                <small style="display: block; margin-top: 10px;">
                    This should be your largest serving<br>
                    Minimum 1/2 cup regardless of level<br>
                    Let your brain say "do that again!"
                </small>
            </div>
        </div>
        
        <div class="important-box">
            <div class="important-title">DAILY TOTALS:</div>
            <div class="checkbox-item" onclick="toggleCheck(this)">
                <div class="checkbox"></div>
                <span><strong>Level 1:</strong> 1 cup total across 7 servings</span>
            </div>
            <div class="checkbox-item" onclick="toggleCheck(this)">
                <div class="checkbox"></div>
                <span><strong>Level 2:</strong> 2 cups total across 7 servings</span>
            </div>
            <div class="checkbox-item" onclick="toggleCheck(this)">
                <div class="checkbox"></div>
                <span><strong>Level 3:</strong> 3 cups total across 7 servings</span>
            </div>
        </div>
    </div>

    <div class="section" id="vegetables">
        <h2>The 6 Healing Vegetables</h2>
        <p style="margin-bottom: 20px;">REQUIRED VEGETABLES (use all 6 daily):</p>
        
        <div class="vegetable-grid">
            <div class="vegetable-card">
                <span class="vegetable-emoji">🥬</span>
                <div class="vegetable-name">Collard Greens</div>
                <div class="vegetable-desc">The foundation vegetable<br>Highest in glucosinolates</div>
            </div>
            
            <div class="vegetable-card">
                <span class="vegetable-emoji">🍃</span>
                <div class="vegetable-name">Mustard Greens</div>
                <div class="vegetable-desc">Highest beneficial content<br>Powerful anti-inflammatory</div>
            </div>
            
            <div class="vegetable-card">
                <span class="vegetable-emoji">🌿</span>
                <div class="vegetable-name">Turnip Greens</div>
                <div class="vegetable-desc">Rich in anti-inflammatory compounds<br>Supports cellular detoxification</div>
            </div>
            
            <div class="vegetable-card">
                <span class="vegetable-emoji">🥬</span>
                <div class="vegetable-name">Romaine Lettuce</div>
                <div class="vegetable-desc">Perfect salad base<br>Digestive support properties</div>
            </div>
            
            <div class="vegetable-card">
                <span class="vegetable-emoji">🟣</span>
                <div class="vegetable-name">Red Cabbage</div>
                <div class="vegetable-desc">Antioxidant powerhouse<br>Vibrant healing nutrition</div>
            </div>
            
            <div class="vegetable-card">
                <span class="vegetable-emoji">🔴</span>
                <div class="vegetable-name">Radicchio</div>
                <div class="vegetable-desc">Bitter healing compounds<br>Liver detox support</div>
            </div>
        </div>
        
        <div style="background: #fff3cd; padding: 20px; border-radius: 10px; border-left: 4px solid #f39c12;">
            <h4 style="color: #856404; margin-bottom: 10px;">STORAGE TIP FOR GREENS:</h4>
            <p style="color: #856404;">Remove excess air from bags and use a chip clip to seal remaining contents. This keeps greens fresh longer.</p>
        </div>
        
        <div style="background: #fff3cd; padding: 20px; border-radius: 10px; border-left: 4px solid #f39c12; margin-top: 15px;">
            <h4 style="color: #856404; margin-bottom: 10px;">SUBSTITUTIONS:</h4>
            <ul style="color: #856404;">
                <li><strong>Red cabbage → Green cabbage</strong> (only substitute allowed)</li>
                <li><strong>Can't find a vegetable?</strong> Simply leave it out, no other substitutes</li>
            </ul>
        </div>
    </div>

    <div class="section" id="preparation">
        <h2>Preparation Instructions</h2>
        
        <h3 style="color: #2d8f47; margin-bottom: 15px;">DAILY PREP METHOD:</h3>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>RINSE all vegetables thoroughly under cold running water</span>
        </div>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>SHAKE or pat dry with clean towel</span>
        </div>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>CHOP finely - small, bite-sized pieces for easier digestion</span>
        </div>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>MIX all 6 vegetables in equal portions</span>
        </div>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>STORE in airtight container in refrigerator</span>
        </div>
        
        <h3 style="color: #2d8f47; margin: 25px 0 15px;">CHOPPING TIPS:</h3>
        <ul style="margin-left: 20px; line-height: 1.8;">
            <li><strong>Collard Greens:</strong> Remove thick stems, chop leaves</li>
            <li><strong>Mustard/Turnip Greens:</strong> Chop entire leaf (stems included)</li>
            <li><strong>Romaine:</strong> Chop entire leaf, including lighter parts</li>
            <li><strong>Red/Green Cabbage:</strong> Remove first few discolored outer leaves, chop inner head</li>
            <li><strong>Radicchio:</strong> Remove first few discolored outer leaves, chop remaining head</li>
        </ul>
        
        <h3 style="color: #2d8f47; margin: 25px 0 15px;">TIMING:</h3>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>Prep fresh each morning for best potency</span>
        </div>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>OR prep every 2-3 days maximum</span>
        </div>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>Never store chopped mix longer than 3 days</span>
        </div>
        
        <h3 style="color: #2d8f47; margin: 25px 0 15px;">SERVING SUGGESTIONS:</h3>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>Use high quality fat, low sugar salad dressing: ranch, caesar, olive oil, quality balsamic</span>
        </div>
        <div class="checkbox-item" onclick="toggleCheck(this)">
            <div class="checkbox"></div>
            <span>Add lemon or lime juice for enhanced absorption</span>
        </div>
        
        <div class="important-box">
            <div class="important-title">IMPORTANT:</div>
            <ul style="margin-top: 10px;">
                <li>Consume as a cold salad or as close to raw as possible for most nutritional benefits</li>
                <li>Chew thoroughly to activate nutritional compounds</li>
                <li>Start with smaller amounts if new to raw greens</li>
            </ul>
        </div>
    </div>

    <div class="section" id="faq">
        <h2>Troubleshooting FAQ</h2>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                What if I can't find all 6 vegetables?
            </div>
            <div class="faq-answer">
                Use what you can find. Only substitute green cabbage for red cabbage. If missing other vegetables, simply leave them out - no other substitutes allowed.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                Can I eat them cooked instead of raw?
            </div>
            <div class="faq-answer">
                Yes, but only lightly sautéed in butter or oil. Consume as a cold salad or as close to raw as possible for most nutritional benefits.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                The taste is too strong/bitter for me
            </div>
            <div class="faq-answer">
                Lightly sauté, add lemon or lime juice, or create your own salad dressing. Start with smaller portions and gradually increase.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                I'm traveling - how do I maintain the protocol?
            </div>
            <div class="faq-answer">
                Look for pre-washed salad mixes containing these vegetables, or visit local grocery stores. I use a chip clip to seal prepackaged items.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                What if I miss a serving or day?
            </div>
            <div class="faq-answer">
                Simply resume the protocol. Don't try to "catch up" by doubling servings. Consistency over perfection.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                I'm experiencing digestive bloating
            </div>
            <div class="faq-answer">
                I started with smaller amounts and increase gradually. Chew thoroughly. The digestive system is collecting toxins & needs time to adjust to raw vegetables and create a sustainable gut environment.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                How long until I see results?
            </div>
            <div class="faq-answer">
                For me and most people notice increased energy within 3-5 days. Inflammation reduction typically occurs within 2-3 weeks of consistent use.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                Can I take this with my medications?
            </div>
            <div class="faq-answer">
                Always consult your healthcare provider before making dietary changes, especially if taking blood thinners or other medications. This protocol is based on experience backed by science.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                What if I forget the nighttime serving?
            </div>
            <div class="faq-answer">
                The nighttime serving is the most important. Set a phone reminder. This final serving helps your body process the compounds overnight.
            </div>
        </div>
        
        <div class="faq-item">
            <div class="faq-question" onclick="toggleFAQ(this)">
                Can I prep more than 3 days ahead?
            </div>
            <div class="faq-answer">
                No. The nutritional compounds degrade over time. Fresh preparation maintains maximum potency.
            </div>
        </div>
    </div>

    <div class="section" id="reference">
        <h2>Quick Reference</h2>
        
        <div style="background: linear-gradient(135deg, #f0f9f0 0%, #e8f5e8 100%); padding: 20px; border-radius: 15px;">
            <h3 style="color: #2d8f47; margin-bottom: 15px;">THE 6 VEGETABLES:</h3>
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 10px; margin-bottom: 20px;">
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Collard Greens (remove stems)</span>
                </div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Mustard Greens</span>
                </div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Turnip Greens</span>
                </div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Romaine Lettuce</span>
                </div>
                <div class="checkbox-item" onclick="toggleCheck(this)">
                    <div class="checkbox"></div>
                    <span>Red Cabbage (or Green)</span>
                </div>
                <div class="
```

<script>
        function toggleFAQ(questionElement) {
            const answer = questionElement.nextElementSibling;
            const isActive = answer.classList.contains('active');
            
            document.querySelectorAll('.faq-answer').forEach(faq => {
                faq.classList.remove('active');
            });
            
            if (!isActive) {
                answer.classList.add('active');
            }
        }
        
        function toggleCheck(element) {
            const checkbox = element.querySelector('.checkbox');
            const isChecked = checkbox.classList.contains('checked');
            
            if (isChecked) {
                checkbox.classList.remove('checked');
                element.classList.remove('checked');
            } else {
                checkbox.classList.add('checked');
                element.classList.add('checked');
            }
        }
        
        function selectLevel(level, element) {
            document.querySelectorAll('.assessment-card').forEach(card => {
                card.classList.remove('selected');
            });
            element.classList.add('selected');
            
            const selectedLevelDiv = document.getElementById('selectedLevel');
            const levelDisplay = document.getElementById('levelDisplay');
            selectedLevelDiv.style.display = 'block';
            levelDisplay.textContent = `Level ${level}: ${level} cup${level > 1 ? 's' : ''} daily across 7 servings`;
        }
        
        function selectEnergyLevel(energyType, element) {
            const energyCards = element.parentElement.querySelectorAll('.assessment-card');
            energyCards.forEach(card => {
                card.classList.remove('selected');
            });
            element.classList.add('selected');
            
            let level;
            switch(energyType) {
                case 'tired': level = 3; break;
                case 'sometimes': level = 2; break;
                case 'energetic': level = 1; break;
            }
            
            const selectedLevelDiv = document.getElementById('selectedLevel');
            const levelDisplay = document.getElementById('levelDisplay');
            selectedLevelDiv.style.display = 'block';
            levelDisplay.textContent = `Level ${level} (Energy-based): ${level} cup${level > 1 ? 's' : ''} daily across 7 servings`;
        }
    </script>
</body>
</html>
