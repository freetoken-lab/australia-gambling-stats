/* =============================================
   BETTING IN AUSTRALIA — MAIN JS
   - Counter animations
   - Chart.js charts
   - Interactive map
   - Sortable table
   - Mobile nav
============================================= */

document.addEventListener('DOMContentLoaded', function () {

  // ============ YEAR ============
  const yearEl = document.getElementById('year');
  if (yearEl) yearEl.textContent = new Date().getFullYear();

  // ============ MOBILE NAV ============
  const toggle = document.getElementById('nav-toggle');
  const nav = document.getElementById('main-nav');
  if (toggle && nav) {
    toggle.addEventListener('click', function () {
      const open = nav.classList.toggle('open');
      toggle.setAttribute('aria-expanded', open);
    });
    // Dropdown toggles on mobile
    document.querySelectorAll('.has-dropdown > a').forEach(function (link) {
      link.addEventListener('click', function (e) {
        if (window.innerWidth <= 768) {
          e.preventDefault();
          link.parentElement.classList.toggle('open');
        }
      });
    });
  }

  // ============ COUNTER ANIMATION ============
  function animateCounter(el, target, prefix, suffix, duration) {
    const start = performance.now();
    const isDecimal = String(target).includes('.');
    function step(now) {
      const progress = Math.min((now - start) / duration, 1);
      const eased = 1 - Math.pow(1 - progress, 3);
      const current = target * eased;
      let display;
      if (isDecimal) {
        display = prefix + current.toFixed(1) + suffix;
      } else {
        display = prefix + Math.round(current).toLocaleString() + suffix;
      }
      el.textContent = display;
      if (progress < 1) requestAnimationFrame(step);
    }
    requestAnimationFrame(step);
  }

  // Intersection observer to trigger counters when hero is visible
  const statCards = document.querySelectorAll('.stat-card[data-target]');
  if (statCards.length && 'IntersectionObserver' in window) {
    const observer = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          const card = entry.target;
          const valEl = card.querySelector('.stat-value');
          const target = parseFloat(card.dataset.target);
          const prefix = card.dataset.prefix || '';
          const suffix = card.dataset.suffix || '';
          animateCounter(valEl, target, prefix, suffix, 1800);
          observer.unobserve(card);
        }
      });
    }, { threshold: 0.3 });
    statCards.forEach(function (card) { observer.observe(card); });
  }

  // ============ CHART: EXPENDITURE BAR ============
  const expCtx = document.getElementById('expenditureChart');
  if (expCtx) {
    new Chart(expCtx, {
      type: 'bar',
      data: {
        labels: ['2018–19', '2019–20', '2020–21', '2021–22', '2022–23'],
        datasets: [
          {
            label: 'Total Net Losses (AUD Billions)',
            data: [25.9, 24.1, 24.0, 27.0, 31.5],
            backgroundColor: [
              'rgba(26,92,52,0.75)',
              'rgba(26,92,52,0.55)',
              'rgba(26,92,52,0.55)',
              'rgba(26,92,52,0.75)',
              'rgba(242,201,76,0.9)',
            ],
            borderColor: [
              '#1a5c34','#1a5c34','#1a5c34','#1a5c34','#d4a900'
            ],
            borderWidth: 2,
            borderRadius: 6,
          }
        ]
      },
      options: {
        responsive: true,
        maintainAspectRatio: true,
        plugins: {
          legend: { display: false },
          tooltip: {
            callbacks: {
              label: function (ctx) {
                return ' AUD $' + ctx.parsed.y.toFixed(1) + 'B';
              },
              afterLabel: function (ctx) {
                if (ctx.dataIndex === 1) return '⬇ COVID-19 impact';
                if (ctx.dataIndex === 4) return '⬆ Post-pandemic high';
                return '';
              }
            }
          }
        },
        scales: {
          y: {
            beginAtZero: false,
            min: 20,
            max: 35,
            ticks: {
              callback: function (val) { return '$' + val + 'B'; },
              color: '#5a7a65'
            },
            grid: { color: 'rgba(0,0,0,0.05)' }
          },
          x: {
            ticks: { color: '#5a7a65' },
            grid: { display: false }
          }
        }
      }
    });
  }

  // ============ CHART: ONLINE vs VENUE DONUT ============
  const onlineCtx = document.getElementById('onlineVenueChart');
  if (onlineCtx) {
    new Chart(onlineCtx, {
      type: 'doughnut',
      data: {
        labels: ['Mainly Online', 'Mainly Venue-based', 'Mixed / Other'],
        datasets: [{
          data: [56.1, 28.6, 15.3],
          backgroundColor: ['#144B2C', '#F2C94C', '#a8c5b5'],
          borderColor: ['#F9F9F9', '#F9F9F9', '#F9F9F9'],
          borderWidth: 3,
          hoverOffset: 8
        }]
      },
      options: {
        responsive: true,
        cutout: '68%',
        plugins: {
          legend: {
            position: 'bottom',
            labels: {
              color: '#0D3D22',
              padding: 16,
              font: { size: 13 }
            }
          },
          tooltip: {
            callbacks: {
              label: function (ctx) {
                return ' ' + ctx.label + ': ' + ctx.parsed + '%';
              }
            }
          }
        }
      }
    });
  }

  // ============ CHART: ACTIVITY HORIZONTAL BAR ============
  const actCtx = document.getElementById('activityChart');
  if (actCtx) {
    new Chart(actCtx, {
      type: 'bar',
      data: {
        labels: [
          'Lottery tickets',
          'Scratch tickets',
          'EGMs (Pokies)',
          'Race betting',
          'Sports betting',
          'Keno',
          'Casino table games',
          'Poker'
        ],
        datasets: [{
          label: '% of Australian adults participating (2025)',
          data: [41.3, 19.4, 14.9, 12.6, 9.1, 6.2, 4.1, 2.4],
          backgroundColor: [
            '#144B2C','#1a5c34','#F2C94C','#1a5c34',
            '#F2C94C','#1a5c34','#144B2C','#a8c5b5'
          ],
          borderRadius: 5,
          borderSkipped: false
        }]
      },
      options: {
        indexAxis: 'y',
        responsive: true,
        plugins: {
          legend: { display: false },
          tooltip: {
            callbacks: {
              label: function (ctx) { return ' ' + ctx.parsed.x + '% of adults'; }
            }
          }
        },
        scales: {
          x: {
            ticks: { callback: function (v) { return v + '%'; }, color: '#5a7a65' },
            grid: { color: 'rgba(0,0,0,0.05)' }
          },
          y: {
            ticks: { color: '#0D3D22', font: { size: 13 } },
            grid: { display: false }
          }
        }
      }
    });
  }

  // ============ CHART: HARM TREND LINE ============
  const harmCtx = document.getElementById('harmTrendChart');
  if (harmCtx) {
    new Chart(harmCtx, {
      type: 'line',
      data: {
        labels: ['2019', '2020', '2021', '2023', '2024', '2025'],
        datasets: [
          {
            label: 'Risky gambling rate (%)',
            data: [10.2, 9.8, 10.1, 11.6, 13.7, 19.4],
            borderColor: '#F2C94C',
            backgroundColor: 'rgba(242,201,76,0.12)',
            borderWidth: 3,
            pointBackgroundColor: '#F2C94C',
            pointBorderColor: '#144B2C',
            pointBorderWidth: 2,
            pointRadius: 6,
            pointHoverRadius: 9,
            fill: true,
            tension: 0.35
          },
          {
            label: 'Overall participation (%)',
            data: [65.6, 58.0, 60.2, 62.1, 60.3, 58.8],
            borderColor: '#1a5c34',
            backgroundColor: 'rgba(26,92,52,0.08)',
            borderWidth: 2.5,
            borderDash: [6, 4],
            pointBackgroundColor: '#1a5c34',
            pointBorderColor: '#F9F9F9',
            pointBorderWidth: 2,
            pointRadius: 5,
            pointHoverRadius: 8,
            fill: false,
            tension: 0.35
          }
        ]
      },
      options: {
        responsive: true,
        plugins: {
          legend: {
            position: 'bottom',
            labels: { color: '#0D3D22', padding: 16, font: { size: 13 } }
          },
          tooltip: {
            callbacks: {
              label: function (ctx) { return ' ' + ctx.dataset.label + ': ' + ctx.parsed.y + '%'; }
            }
          }
        },
        scales: {
          y: {
            ticks: { callback: function (v) { return v + '%'; }, color: '#5a7a65' },
            grid: { color: 'rgba(0,0,0,0.05)' }
          },
          x: {
            ticks: { color: '#5a7a65' },
            grid: { display: false }
          }
        }
      }
    });
  }

  // ============ INTERACTIVE MAP TOOLTIP ============
  const tooltip = document.getElementById('map-tooltip');
  const mapEl = document.getElementById('aus-map');

  if (tooltip && mapEl) {
    const stateLinks = {
      'WA': '/states/wa.html',
      'NT': '/states/nt.html',
      'QLD': '/states/qld.html',
      'SA': '/states/sa.html',
      'NSW': '/states/nsw.html',
      'VIC': '/states/vic.html',
      'TAS': '/states/tas.html',
      'ACT': '/states/act.html',
    };

    function buildTooltip(el) {
      const state = el.dataset.state;
      return `
        <strong>${el.dataset.name}</strong>
        <div class="tip-row"><span>Turnover</span><span>${el.dataset.turnover}</span></div>
        <div class="tip-row"><span>Net Losses</span><span>${el.dataset.losses}</span></div>
        <div class="tip-row"><span>Tax / Rate</span><span>${el.dataset.tax}</span></div>
        <div class="tip-note">${el.dataset.note}</div>
        <a class="tip-link" href="${stateLinks[state] || '#'}">View full ${state} data →</a>
      `;
    }

    document.querySelectorAll('.state-path').forEach(function (path) {
      path.addEventListener('mouseenter', function (e) {
        tooltip.innerHTML = buildTooltip(path);
        tooltip.classList.add('visible');
        positionTooltip(e);
      });
      path.addEventListener('mousemove', function (e) { positionTooltip(e); });
      path.addEventListener('mouseleave', function () { tooltip.classList.remove('visible'); });
      path.addEventListener('click', function () {
        const state = path.dataset.state;
        const link = stateLinks[state];
        if (link) window.location.href = link;
      });
      path.setAttribute('tabindex', '0');
      path.addEventListener('focus', function () {
        const rect = path.getBoundingClientRect();
        const mapRect = mapEl.getBoundingClientRect();
        tooltip.innerHTML = buildTooltip(path);
        tooltip.classList.add('visible');
        tooltip.style.left = (rect.left - mapRect.left + rect.width / 2) + 'px';
        tooltip.style.top = (rect.top - mapRect.top - 10) + 'px';
      });
      path.addEventListener('blur', function () { tooltip.classList.remove('visible'); });
    });

    function positionTooltip(e) {
      const mapRect = mapEl.closest('.map-container').getBoundingClientRect();
      let x = e.clientX - mapRect.left + 14;
      let y = e.clientY - mapRect.top - 10;
      // Keep inside container
      if (x + 250 > mapRect.width) x = e.clientX - mapRect.left - 260;
      if (y < 0) y = 10;
      tooltip.style.left = x + 'px';
      tooltip.style.top = y + 'px';
    }
  }

  // ============ SORTABLE TABLE ============
  const table = document.getElementById('stateTable');
  if (table) {
    const headers = table.querySelectorAll('th.sortable');
    headers.forEach(function (th) {
      th.addEventListener('click', function () {
        const col = parseInt(th.dataset.col);
        const asc = !th.classList.contains('sort-asc');
        // Clear all
        headers.forEach(function (h) { h.classList.remove('sort-asc', 'sort-desc'); });
        th.classList.add(asc ? 'sort-asc' : 'sort-desc');
        const tbody = table.querySelector('tbody');
        const rows = Array.from(tbody.querySelectorAll('tr'));
        rows.sort(function (a, b) {
          const aCell = a.cells[col];
          const bCell = b.cells[col];
          const aVal = aCell.dataset.val !== undefined ? parseFloat(aCell.dataset.val) : aCell.textContent.trim();
          const bVal = bCell.dataset.val !== undefined ? parseFloat(bCell.dataset.val) : bCell.textContent.trim();
          if (typeof aVal === 'number' && typeof bVal === 'number') {
            return asc ? aVal - bVal : bVal - aVal;
          }
          return asc ? String(aVal).localeCompare(String(bVal)) : String(bVal).localeCompare(String(aVal));
        });
        rows.forEach(function (row) { tbody.appendChild(row); });
      });
    });
  }

  // ============ SCROLL REVEAL ============
  if ('IntersectionObserver' in window) {
    const revealEls = document.querySelectorAll('.section-block, .author-card, .sports-tile, .state-card, .news-card');
    const revealObs = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          entry.target.style.animation = 'fadeUp 0.5s ease both';
          revealObs.unobserve(entry.target);
        }
      });
    }, { threshold: 0.08 });
    revealEls.forEach(function (el) { revealObs.observe(el); });
  }

});
