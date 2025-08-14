# Product Images Directory

This directory contains product images that will be automatically matched with product names using the Intelligent Image Service.

## Naming Convention

The system will automatically match product names with image files using various naming patterns:

### Examples:

**Product Name: "Chicken Biryani Cut"**
- `chicken_biryani_cut.png`
- `chicken-biryani-cut.jpg`
- `chickenbiriyanicut.jpeg`
- `biryani_cut.png`
- `chicken_biryani.webp`

**Product Name: "Fresh Boneless Chicken"**
- `fresh_boneless_chicken.png`
- `boneless_chicken.jpg`
- `boneless.png`
- `chicken_boneless.jpeg`

**Product Name: "Mutton Curry Cut"**
- `mutton_curry_cut.png`
- `curry_cut.jpg`
- `mutton_curry.png`
- `mutton.jpeg`

## Supported Formats
- PNG (.png)
- JPEG (.jpg, .jpeg)
- WebP (.webp)

## Recommended Image Specifications
- **Resolution**: 512x512 pixels minimum
- **Aspect Ratio**: 1:1 (square) preferred
- **File Size**: Under 500KB for optimal performance
- **Background**: Clean, preferably white or transparent

## Sample Images to Add

### Chicken Products
- `chicken.png` - General chicken
- `boneless_chicken.png` - Boneless chicken pieces
- `chicken_legs.png` - Chicken legs/drumsticks
- `chicken_breast.png` - Chicken breast
- `chicken_wings.png` - Chicken wings
- `whole_chicken.png` - Whole chicken
- `chicken_biryani_cut.png` - Chicken cut for biryani
- `chicken_curry_cut.png` - Chicken curry cut
- `chicken_fry.png` - Chicken fry pieces
- `chicken_tikka.png` - Chicken tikka
- `marinated_chicken.png` - Marinated chicken

### Mutton Products
- `mutton.png` - General mutton
- `mutton_curry_cut.png` - Mutton curry cut
- `mutton_biryani_cut.png` - Mutton biryani cut
- `goat_meat.png` - Goat meat
- `mutton_chops.png` - Mutton chops

### Fish & Seafood
- `fish.png` - General fish
- `fish_fillet.png` - Fish fillet
- `prawns.png` - Prawns/shrimp
- `fresh_fish.png` - Fresh fish
- `fish_curry_cut.png` - Fish curry cut

### Ready to Cook
- `ready_to_cook.png` - General ready to cook
- `marinated.png` - Marinated items
- `chicken_sausage.png` - Chicken sausage
- `chicken_kebab.png` - Chicken kebab

### Eggs
- `eggs.png` - Chicken eggs
- `farm_eggs.png` - Farm fresh eggs

## How It Works

1. **Admin adds product**: "Chicken Biryani Cut"
2. **System generates variations**: 
   - chicken_biryani_cut
   - chicken-biryani-cut
   - biryani_cut
   - chicken_biryani
   - etc.
3. **System checks for files**:
   - `assets/images/products/chicken_biryani_cut.png` ✓
   - `assets/images/products/chicken_biryani_cut.jpg`
   - `assets/images/products/biryani_cut.png`
   - etc.
4. **First match found is used**

## Fallback System

If no specific product image is found, the system will:
1. Try category-based images (chicken.png, mutton.png, etc.)
2. Use category fallback images from `assets/images/categories/`
3. Show default icon as last resort

## Adding New Images

1. Save images in this directory (`assets/images/products/`)
2. Use descriptive names matching your products
3. Follow the naming conventions above
4. Update `pubspec.yaml` if needed:
   ```yaml
   flutter:
     assets:
       - assets/images/products/
   ```
5. Run `flutter pub get` and restart the app

## Performance Tips

- Keep image files optimized
- Use WebP format for better compression
- Consider using different resolutions for different screen densities
- The system caches image lookups for better performance
