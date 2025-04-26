<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mentor Cards</title>
    <style>
        :root {
            --bg-color: #f8f9fa;
            --card-bg: #ffffff;
            --accent: #2563eb;
            --text-primary: #1f2937;
            --text-secondary: #6b7280;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            background-color: var(--bg-color);
            padding: 2rem;
        }

        .mentor-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .mentor-card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 1.5rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s ease;
            position: relative;
        }

        .mentor-card:hover {
            transform: translateY(-5px);
        }

        .new-mentor-badge {
            position: absolute;
            top: -10px;
            right: -10px;
            background: #10b981;
            color: white;
            padding: 0.25rem 0.75rem;
            border-radius: 20px;
            font-size: 0.875rem;
            font-weight: 500;
        }

        .mentor-header {
            margin-bottom: 1rem;
        }

        .mentor-header>img {
            width: 340px;
            border-radius: 8px;
        }

        .mentor-name {
            font-size: 1.25rem;
            font-weight: 600;
            color: var(--text-primary);
        }

        .mentor-position {
            color: var(--text-secondary);
            font-size: 0.875rem;
            margin: 0.25rem 0;
        }

        .mentor-company {
            color: var(--accent);
            font-weight: 500;
            font-size: 0.875rem;
        }

        .mentor-stats {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin: 1rem 0;
        }

        .rating {
            display: flex;
            align-items: center;
            gap: 0.25rem;
            color: #f59e0b;
        }

        .reviews {
            color: var(--text-secondary);
            font-size: 0.875rem;
        }

        .pricing {
            margin: 1rem 0;
        }

        .price {
            font-size: 1.5rem;
            font-weight: 600;
            color: var(--text-primary);
        }

        .action-button {
            width: 100%;
            padding: 0.75rem;
            background-color: var(--accent);
            color: white;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 500;
            transition: opacity 0.2s ease;
        }

        .action-button:hover {
            opacity: 0.9;
        }
    </style>
</head>

<body>
    <div class="mentor-grid">
        <!-- Andrew Lupien -->
        <div class="mentor-card">
            <div class="mentor-header">
                <img src="jonathan-borba-8l8Yl2ruUsg-unsplash.jpg" alt="">
                <div class="mentor-name">Andrew Lupien</div>
                <div class="mentor-position">Quality Assurance Engineer</div>
                <div class="mentor-company">@ Microsoft | 5 yrs Exp.</div>
            </div>
            <div class="mentor-stats">
                <div class="rating">★ 4.5</div>
                <div class="reviews">(2 Reviews)</div>
            </div>
            <div class="pricing">
                <div class="price">$35.00/month</div>
            </div>
            <button class="action-button">Book Free Trial</button>
        </div>

        <!-- Bernice Perry -->
        <div class="mentor-card">
            <div class="new-mentor-badge">New Mentor</div>
            <div class="mentor-header">
                <img src="jonathan-borba-8l8Yl2ruUsg-unsplash.jpg" alt="">
                <div class="mentor-name">Bernice Perry</div>
                <div class="mentor-position">Senior Business Analyst</div>
                <div class="mentor-company">@ Amazon | 5 yrs Exp.</div>
            </div>
            <div class="mentor-stats">
                <div class="rating">★ 0.0</div>
                <div class="reviews">(0 Reviews)</div>
            </div>
            <div class="pricing">
                <div class="price">$40.00/month</div>
            </div>
            <button class="action-button">Book Sessions</button>
        </div>

        <!-- Patrice Long -->
        <div class="mentor-card">
            <div class="mentor-header">
                <img src="jonathan-borba-8l8Yl2ruUsg-unsplash.jpg" alt="">
                <div class="mentor-name">Patrice Long</div>
                <div class="mentor-position">Senior Data Engineer</div>
                <div class="mentor-company">@ InstaCart | 5 yrs Exp.</div>
            </div>
            <div class="mentor-stats">
                <div class="rating">★ 4.5</div>
                <div class="reviews">(10 Reviews)</div>
            </div>
            <div class="pricing">
                <div class="price">$60.00/month</div>
            </div>
            <button class="action-button">Book Sessions</button>
        </div>

        <!-- Add other mentor cards following the same structure -->
    </div>

    <script>
        // Add click handlers for booking buttons
        document.querySelectorAll('.action-button').forEach(button => {
            button.addEventListener('click', function () {
                const mentorName = this.closest('.mentor-card').querySelector('.mentor-name').textContent;
                alert(`Booking session with ${mentorName}`);
            });
        });
    </script>
</body>

</html>
