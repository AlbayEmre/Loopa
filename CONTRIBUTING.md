# Katkıda Bulunma Rehberi

Loopa projesine katkıda bulunmak istediğiniz için teşekkür ederiz! 🎉

## 🚀 Nasıl Katkıda Bulunabilirim?

### 1. Issue Oluşturma

Bir hata buldunuz veya yeni bir özellik öneriniz mi var?

- 🐛 **Bug Report**: [Hata bildirin](https://github.com/EnesMalik02/hsd-proje-backend/issues/new)
- ✨ **Feature Request**: Yeni özellik önerin
- 📝 **Documentation**: Dokümantasyon iyileştirmeleri

### 2. Pull Request Süreci

1. **Fork edin**: Projeyi kendi hesabınıza fork edin
2. **Branch oluşturun**: 
   ```bash
   git checkout -b feature/amazing-feature
   # veya
   git checkout -b fix/bug-fix
   ```
3. **Değişiklik yapın**: Kodunuzu yazın ve test edin
4. **Commit edin**: Anlamlı commit mesajları kullanın
   ```bash
   git commit -m "feat: Add amazing feature"
   git commit -m "fix: Resolve login issue"
   ```
5. **Push edin**: Branch'inizi push edin
   ```bash
   git push origin feature/amazing-feature
   ```
6. **Pull Request açın**: GitHub'da PR oluşturun

## 📝 Commit Mesaj Formatı

Conventional Commits formatını kullanıyoruz:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Commit Tipleri

- `feat`: Yeni özellik
- `fix`: Hata düzeltme
- `docs`: Dokümantasyon değişikliği
- `style`: Kod formatı (kod mantığını değiştirmeyen)
- `refactor`: Kod iyileştirme (ne bug fix ne de feature)
- `test`: Test ekleme veya düzeltme
- `chore`: Build process veya yardımcı araç değişiklikleri

### Örnekler

```bash
feat(auth): Add Google OAuth login
fix(listings): Resolve image upload issue
docs(readme): Update installation instructions
style(frontend): Format code with prettier
refactor(api): Optimize database queries
test(auth): Add unit tests for login
chore(deps): Update dependencies
```

## 🎨 Kod Standartları

### Python (Backend)

- **PEP 8** standartlarına uyun
- **Type hints** kullanın
- **Docstrings** yazın (Google style)
- **Black** ile formatla: `black app/`
- **Flake8** ile lint: `flake8 app/`

```python
def create_listing(
    listing_data: ListingCreate,
    user_id: str
) -> ListingResponse:
    """
    Create a new listing.
    
    Args:
        listing_data: Listing creation data
        user_id: ID of the user creating the listing
        
    Returns:
        Created listing response
        
    Raises:
        ValueError: If listing data is invalid
    """
    # Implementation
    pass
```

### TypeScript (Frontend)

- **ESLint** kurallarına uyun
- **TypeScript strict mode** kullanın
- **Prettier** ile formatla
- **Anlamlı değişken isimleri** kullanın

```typescript
interface ListingCardProps {
  listing: ListingResponse;
  onClick: () => void;
}

export const ListingCard: React.FC<ListingCardProps> = ({ 
  listing, 
  onClick 
}) => {
  // Implementation
};
```

## 🧪 Test Yazma

### Backend Tests

```python
# tests/test_listings.py
import pytest
from app.models.listing import ListingCreate

def test_create_listing():
    """Test listing creation."""
    listing_data = ListingCreate(
        title="Test Listing",
        description="Test description",
        # ...
    )
    # Test implementation
```

### Frontend Tests

```typescript
// __tests__/ListingCard.test.tsx
import { render, screen } from '@testing-library/react';
import { ListingCard } from '@/components/ListingCard';

describe('ListingCard', () => {
  it('renders listing title', () => {
    // Test implementation
  });
});
```

## 🔍 Code Review Süreci

Pull Request'iniz şu kriterlere göre incelenecektir:

- ✅ Kod standartlarına uygunluk
- ✅ Test coverage
- ✅ Dokümantasyon
- ✅ Performans etkisi
- ✅ Güvenlik kontrolleri
- ✅ Breaking changes kontrolü

## 🐛 Bug Report Template

```markdown
**Bug Açıklaması**
Hatanın kısa ve net açıklaması.

**Nasıl Tekrarlanır**
1. '...' sayfasına git
2. '...' butonuna tıkla
3. Aşağı kaydır
4. Hatayı gör

**Beklenen Davranış**
Ne olmasını bekliyordunuz?

**Ekran Görüntüleri**
Varsa ekran görüntüleri ekleyin.

**Ortam:**
 - OS: [örn. Windows 11]
 - Browser: [örn. Chrome 120]
 - Version: [örn. 1.0.0]

**Ek Bilgi**
Başka bir bilgi eklemek isterseniz.
```

## ✨ Feature Request Template

```markdown
**Özellik İsteği**
Özelliğin kısa açıklaması.

**Sorun**
Bu özellik hangi sorunu çözüyor?

**Önerilen Çözüm**
Nasıl çözülebileceğini düşünüyorsunuz?

**Alternatifler**
Düşündüğünüz alternatif çözümler.

**Ek Bilgi**
Mockup, screenshot, vb.
```

## 📚 Kaynaklar

- [Next.js Dokümantasyonu](https://nextjs.org/docs)
- [FastAPI Dokümantasyonu](https://fastapi.tiangolo.com/)
- [Firebase Dokümantasyonu](https://firebase.google.com/docs)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [PEP 8 Style Guide](https://pep8.org/)

## 💬 İletişim

Sorularınız için:
- GitHub Issues kullanın
- Pull Request'lerde yorum yapın

## 🙏 Teşekkürler

Loopa projesine katkıda bulunduğunuz için teşekkür ederiz! Her katkı, platformu daha iyi hale getiriyor. 🌱
